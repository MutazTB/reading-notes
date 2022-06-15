# SendGrid 

## Create a Twilio SendGrid account
From the Azure portal home page, select Marketplace under Azure services. If you do not see the Marketplace icon, you can search for it by selecting More services. 

The Azure Marketplace provides many services, including the Twilio SendGrid email service. You can find it by searching for "Twilio SendGrid." You will also find it under Software as a Service (SaaS)

## Twilio SendGrid account setup
Before sending your first email, you will need to complete the following Twilio SendGrid account setup. These requirements help secure your account and keep your messages from landing in spam folders.

* Configure Two-factor authentication
* Create an API key
* Complete Sender Authentication

## Two-factor authentication
Twilio SendGrid uses Two-factor authentication (2FA) to help protect your account. To enable 2FA, Navigate to Two-Factor Authentication in the Twilio SendGrid Settings menu, and click Add Two-Factor Authentication.

## API keys
API Keys authenticate your application, mail client, or website with Twilio SendGrid services. Unlike a username and password, API keys are scoped to provide access only to the services you select. You can also delete and create API keys without impacting your other account credentials. For these reasons, Twilio SendGrid requires you to connect to its services using API keys.

 Twilio SendGrid provides three types of API key:

* Full Access
* Restricted Access
* Billing Access

To keep your account secure, you should give each key the least privilege necessary. You can limit a key's capabilities by creating a Restricted Access key and selecting a subset of all the possible permissions.

## Sender Authentication
Twilio SendGrid requires customers to complete Sender Authentication. This requirement protects your domain's reputation as an email sender and helps uphold legitimate sending behavior by Twilio SendGrid customers.
