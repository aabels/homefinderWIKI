## Facebook

As per the requirements, we have a third party integration with Facebook to enable users to login and signup using their facebook account. Before access to the Facebook API, and even for our authentication system to work, we need to add our Facebook App ID and secret to our database. This can be done through the admin console.

Social Applications -> New -> Info from `https://developers.facebook.com`. The `Key` field does not need to be filled, but the `Provider`, `Name`, `Client ID`, and `Secret Key` are mandatory

## Sendgrid

For the email provider, we decided to go with SendGrid as they have a good reputation, fair pricing, and it integrates well with Django. To use the SendGrid mailing service, the appropriate configuration needs to be passed. Particularly the following:

```.env
SENDGRID_API_KEY="<SUPER_SECRET_API_KEY>"
DJANGO_EMAIL_BACKEND="anymail.backends.sendgrid.EmailBackend"
```
