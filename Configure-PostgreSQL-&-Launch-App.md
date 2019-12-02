## Installing PostgresSQL

For simplicity, we will be using Docker to run our Postgres database.

First, you will need to [install Docker](https://docs.docker.com/install/) before proceeding.

After installing Docker, you can pull the latest Postgres image by doing the following

```bash
sudo docker pull postgres:10 # we want the latest of v10
```

We can then launch an instance Postgres on port `5432` with the username, password, database configured like so:
```bash
sudo docker run -p 5432:5432 \
  -e POSTGRES_PASSWORD=homefinder-dev \
  -e POSTGRES_USER=homefinder \
  --restart always \
  -d postgres:10
```

## Django
After having Postgres setup, we can launch the backend using the following:
```bash
pip install -r requirements/base.txt
pip install -r requirements/local.txt
pip install -r requirements/production.txt

DJANGO_READ_DOT_ENV_FILE=True ./manage.py runserver_plus --cert local 0.0.0.0:8000 --settings=config.settings.local
```
where the contents of the `.env` file is something such as the following:
```env
SENDGRID_API_KEY="<SOME_API_KEY>"
DJANGO_EMAIL_BACKEND="anymail.backends.sendgrid.EmailBackend"
DATABASE_URL=postgres://homefinder:homefinder-dev@10.1.9.54/homefinder # the URI of the postgres DB
DJANGO_READ_DOT_ENV_FILE=True
DJANGO_SECRET_KEY="SOME RANDOM GARBAGE"
DJANGO_ADMIN_URL="admin/"
DJANGO_ALLOWED_HOSTS="development.com,rentwhiz.com"
```

