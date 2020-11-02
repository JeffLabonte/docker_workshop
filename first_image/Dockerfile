FROM python
LABEL maintainer=jflabonte@poka.io

# Only for documentation
EXPOSE 5000
# Everything will be in /opt/app from now on
WORKDIR /opt/app/

COPY docker-entrypoint.sh docker-entrypoint.sh

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY app.py app.py

ENTRYPOINT ["./docker-entrypoint.sh"]
