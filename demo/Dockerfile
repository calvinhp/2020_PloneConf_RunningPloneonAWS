FROM sixfeetup/dietplonedocker:latest

COPY requirements /tmp/
RUN set -x \
    && pip --no-cache-dir --disable-pip-version-check install -r /tmp/main.txt

EXPOSE 8080