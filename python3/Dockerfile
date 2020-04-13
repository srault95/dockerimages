FROM alpine:3.10

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
ENV LC_ALL en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV TZ Europe/Paris

RUN mkdir /code

WORKDIR /code

ADD requirements.txt /code/

RUN apk add -U --no-cache \
    python3 \
    bash \
    curl \
    libpq \
    git \
    cairo \
    cairo-gobject \
    pango \
    libjpeg \
    openjpeg \
    tiff \
    graphviz \
    gcc \
    build-base \
    linux-headers \
    ca-certificates \
    python3-dev \
    libffi-dev \
    libressl-dev \
    jpeg-dev \
    zlib-dev \
    freetype-dev \
    lcms2-dev \
    openjpeg-dev \
    tiff-dev \
    tk-dev \
    tcl-dev \
    harfbuzz-dev \
    fribidi-dev

RUN pip3 install -U pip \
    && pip3 install -r requirements.txt

RUN rm -rf /tmp/* /var/cache/apk/* \
    && rm -rf ~/.cache/pip \
    && echo "" > /root/.ash_history \
    && sed -i -e "s/bin\/ash/bin\/bash/" /etc/passwd


