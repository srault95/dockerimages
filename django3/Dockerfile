FROM srault95/python3:latest

WORKDIR /code

ADD requirements.txt /code/

RUN apk add -U --no-cache \
    postgresql-dev \
    graphviz-dev

RUN pip3 install -U pip \
    && pip3 install -r requirements.txt

RUN rm -rf /tmp/* /var/cache/apk/* \
    && rm -rf ~/.cache/pip


