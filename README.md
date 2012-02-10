Nodemailer
==========

This is a project for a new version of Nodemailer, built from scratch.

## Well known services for SMTP

If you want to use a well known service as the SMTP host, you do not need
to enter the hostname or port number, just use the 'service' parameter.

Currently cupported services are: 

  * **"Gmail"** for Google Mail
  * **"hot.ee"** for www.hot.ee
  * **"Hotmail"** for Microsoft Live Hotmail
  * **"iCloud"** for Apple iCloud
  * **"mail.ee"** for www.mail.ee
  * **"Postmark"** for Postmark App
  * **"SendGrid"** for SendGrid
  * **"SES"** for Amazon SES
  * **"Yahoo"** for Yahoo Mail
  * **"Zoho"** for Zoho Mail

Predefined service data covers 'host', 'port' and secure connection settings, 
any other parameters (ie. auth) need to be set separately.

For example:

    var transport = new nodemailer.Transport("SMTP", {
            service: "Gmail",
            auth: {
                user: "gmail.user@gmail.com",
                pass: "password"
            }
        });