### Final image
FROM python:3.8-slim

ARG STATIC_URL
ENV STATIC_URL ${STATIC_URL:-/static/}

COPY . /app
WORKDIR /app

RUN pip install -r requirements.txt

RUN chown -R root:root /app/

EXPOSE 8000
ENV PORT 8000
ENV PYTHONUNBUFFERED 1

CMD ["uwsgi", "--ini", "/app/saleor/wsgi/uwsgi.ini"]
