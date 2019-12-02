## How to setup SendGrid for emails

1. Create an account on SendGrid (if you don't have one)
2. Create an API Key
3. Create a file in the root of the project directory called `.env`
4. Inside `.env`, place the API Key from SendGrid and the email backend you would like to use:
```text
SENDGRID_API_KEY="YOUR_API_KEY"
DJANGO_EMAIL_BACKEND="anymail.backends.sendgrid.EmailBackend"
```
5. Launch the app, specifying to use the `.env` file and the `local` config.
```bash
DJANGO_READ_DOT_ENV_FILE=True ./manage.py runserver_plus --cert local --settings=config.settings.local
```
6. Create and account or do some other event that would cause an email to be sent. (It may end up in your Junk folder)