---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe Target.
title: CNAME and Adobe Target
feature: privacy and security
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
---

# CNAME and Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. To best handle ad blocking issues, or ITP-related cookie policies, a CNAME is used so calls are made to a domain owned by the customer rather than a domain owned by Adobe.

## Request CNAME support

Perform the following steps to request CNAME support in [!DNL Target]:

1. Determine the list of hostnames you need for your SSL certificate (see FAQ).

1. For each hostname, create a CNAME record in your DNS pointing to your regular [!DNL Target] hostname `clientcode.tt.omtrdc.net`. 

   For example, if your client code is "cnamecustomer" and your proposed hostname is `target.example.com`, your DNS CNAME record should look something like this:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >Adobe's certificate authority, DigiCert, cannot issue a certificate until this step is complete. Therefore, Adobe cannot fulfill your request for a CNAME implementation until this step is complete.

1. [Fill out this form](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/assets/FPC_Request_Form.xlsx) and include it when you [open an Adobe Client Care ticket requesting CNAME support](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * Adobe [!DNL Target] client code:
   * SSL certificate hostnames (example: `target.example.com target.example.org`):
   * SSL certificate purchaser (Adobe is highly recommended, see FAQ): Adobe/customer
   * If the customer is purchasing the certificate (aka BYOC), please fill out these additional details:
      * Certificate organization (example: Example Company Inc):
      * Certificate organizational unit (optional, example: Marketing):
      * Certificate country (example: US):
      * Certificate state/region (example: California):
      * Certificate city (example: San Jose):

1. If Adobe is purchasing the certificate, Adobe will work with DigiCert to purchase and deploy your certificate on Adobe's production servers.

   If the customer is purchasing the certificate (BYOC), Adobe Client Care will send you the certificate signing request (CSR), which you will need to use when purchasing the certificate through your certificate authority of choice. After the certificate is issued, you must send a copy of the certificate and any intermediate certificates back to Adobe Client Care for deployment.

   Adobe Client Care will notify you when your implementation is ready.

1. After completing the preceding tasks and Adobe Client Care has notified you that the implementation is ready, you must update the `serverDomain` to the new CNAME in at.js.

## Frequently Asked Questions

The following information answers frequently asked questions about requesting and implementing CNAME support in [!DNL Target]:

### Can I provide my own certificate (aka bring-your-own-certificate or BYOC)?

Yes, you can provide your own certificate; however, it is not recommended. Management of the SSL certificate lifecycle is significantly easier for both Adobe and you when Adobe purchases and controls the certificate. SSL certificates must be renewed every year, which means Adobe Client Care must contact you every year to send Adobe a new certificate in a timely manner. Some customers might have difficulty producing a renewed certificate in a timely manner every year, which jeopardizes their [!DNL Target] implementation because browsers will refuse connections when the certificate expires.

>[!IMPORTANT]
>
>Be aware that if you request a [!DNL Target] bring-your-own-certificate CNAME implementation, you are responsible for providing renewed certificates to Adobe Client Care every year. Allowing your CNAME certificate to expire before Adobe can deploy a renewed certificate will result in an outage for your specific [!DNL Target] implementation.

### How long until my new SSL certificate expires?

Certificates issued before September 1, 2020 will be two-year certificates. Certificates issued on or after September 1, 2020 will be one-year certificates. You can read more about the move to one-year certificates [here](https://www.digicert.com/position-on-1-year-certificates).

### What hostnames should I choose? How many hostnames per domain should I choose?

[!DNL Target] CNAME implementations require only one hostname per domain on the SSL certificate and in the customer's DNS, so that's what we recommend. Some customers might require additional hostnames per domain for their own purposes (testing in staging, for example), which is supported.

Most customers choose a hostname like `target.example.com`, so that's what we recommend, but the choice is ultimately yours. Be sure not to request a hostname of an existing DNS record as that would cause a conflict and delay time to resolution of your [!DNL Target] CNAME request.

### I already have a CNAME implementation for [!DNL Adobe Analytics], can we use the same certificate or hostname?

No, [!DNL Target] requires a separate hostname and certificate.

### Is my current implementation of Target impacted by ITP 2.x?

In a Safari browser, navigate to your website on which you have a Target JavaScript library. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

ITP issues can be resolved for Target with just an Analytics CNAME. You'll need a separate Target CNAME only in the case of ad-blocking scenarios where Target is blocked.

For more information about ITP, see [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### What kind of service disruptions can I expect when my CNAME implementation is deployed?

There is no service disruption when the certificate is deployed (including certificate renewals). However, when you change the hostname in your [!DNL Target] implementation code (`serverDomain` in at.js) to the new CNAME hostname (`target.example.com`), web browsers will treat returning visitors as new visitors and their profile data will be lost because the previous cookie will be inaccessible under the old hostname (`clientcode.tt.omtrdc.net`) due to browser security models. This is a one-time disruption only on the initial cut-over to the new CNAME. Certificate renewals do not have the same effect since the hostname doesn't change.

### What key type and certificate signature algorithm will be used for my CNAME implementation?

All certificates are RSA SHA-256 and keys are RSA 2048-bit, by default. Key sizes larger than 2048-bit are not currently supported.

### How can I validate my CNAME implementation is ready for traffic?

Use the following set of commands (in the MacOs or Linux command-line terminal, using bash and curl 7.49+):

1. First paste this bash function into your terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Next paste this command (replacing `target.example.com` with your hostname):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   If the implementation is ready, you should see output like below. The important part is that all lines show `CN=target.example.com`, which matches our desired hostname. If any of them show `CN=*.tt.omtrdc.net`, the implementation is **not** ready.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge36.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Validate your new DNS CNAME with another curl request, which should also show `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >If this command fails but the `validateEdgeFpsslSni` command above succeeds, you might need to wait for your DNS updates to fully propagate. DNS records have an associated [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) that dictates cache expiration time for DNS replies of those records, so you may need to wait at least as long as your TTLs. You can use the `dig target.example.com` command or [the G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) to look up your specific TTLs.

## Known limitations

* QA mode will not be sticky when you have CNAME and at.js 1.x because it is based on a third-party cookie. The workaround is to add the preview parameters to each URL you navigate to. QA mode is sticky when you have CNAME and at.js 2.x.
* Currently the `overrideMboxEdgeServer` setting doesn't work properly with CNAME. This should be set as `false` in order to avoid failing requests.
* When using CNAME it becomes more likely that the size of the cookie header for Target calls will increase. We recommend keeping the cookie size under 8KB.
