# Images docker réutilisables

![Docker Automated build](https://img.shields.io/docker/automated/srault95/dockerimages)
![Docker Build Status](https://img.shields.io/docker/build/srault95/dockerimages)

## Utilisation

```bash
docker run -it --rm srault95/python3 bash

docker run -it --rm -v $PWD:/code -e DJANGO_SETTINGS_MODULE=myproject.settings srault95/django ./manage.py check
```

## Personnalisation

```
FROM srault95/django:latest

ADD requirements.txt /code/

RUN pip3 install -r requirements.txt
```

```bash
docker build -t myimage .
```

## Build

```bash
cd python3
docker build -t srault95/python3 .

cd django
docker build -t srault95/django .
```
