In order to use Facebook Login locally, the application needs to be configured to use it. The following instructions are to set it up.

```bash
# make sure you have the latest package changes
pip install -r requirements/local.txt 
# fill in the fields accordingly depending on your setup
export DATABASE_URL=postgres://<username>:<password>@<host>:<port>/homefinder
# run migrations to ensure database is up to date
python manage.py migrate
# create an admin user (if you don't already have one)
python manage.py createsuperuser
```

Now, you will need to create a pseudo domain to use with fb login. Append the following to your `/etc/hosts` file
```text
127.0.0.1 development.com
```

Finally, run the app with `python manage.py runserver_plus 0.0.0.0:8000 --cert local` to enable local https, as this is required by Facebook when using their login api.

Now, navigate to `https://0.0.0.0:8000/admin/socialaccount/socialapp/`. Chose create new Social App, choose Facebook and get the respective appid and secret key from `developers.facebook.com` for the `homefinder - Test1` app, then choose `All sites` and save.

After adding the Facebook login ability, navigate to `https://development.com:8000`(in a new session - incognito) and login with facebook.
