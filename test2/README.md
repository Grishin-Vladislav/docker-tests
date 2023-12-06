## django + nginx + postgres in docker
#### with debug = False and staticfiles serving

### instructions:
`root will be smart_home/ dir`
#### 1) create .env file and fill it like in .env-example
#### 2) run docker compose:
```bash
docker compose up --build -d
```
#### 3) enter django-app container:
```bash
docker exec -it django_app /bin/sh
```
#### 4) run migrations and collect statics:
```bash
python3 manage.py migrate
python3 manage.py collectstatic
```
now you can access it through 0.0.0.0:<APP_PORT>/
and check that statics is served in /admin