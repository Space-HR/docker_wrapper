FROM python:3.11-alpine

WORKDIR /usr/src/app
RUN mkdir -p $WORKDIR/static

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev libffi-dev

RUN pip install --upgrade pip

ARG DEPENDENCIES_DIR
COPY $DEPENDENCIES_DIR/requirements.txt .
RUN pip install -r requirements.txt

COPY . .

ARG SCRIPT_DIR
COPY $SCRIPT_DIR/entrypoint.sh /usr/local/bin/docker-entrypoint
RUN chmod +x /usr/local/bin/docker-entrypoint

ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
