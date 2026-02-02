FROM python:3.10

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
RUN pip install flask==3.1.0 uWSGI==2.0.30 requests==2.32.5 redis==7.1.0


WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 9090 9191 5000

USER uwsgi


CMD ["/cmd.sh"]
