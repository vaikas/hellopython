FROM python:3.10-slim@sha256:ca2a31f21938f24bab02344bf846a90cc2bff5bd0e5a53b24b5dfcb4519ea8a3

# LABEL about the custom image
LABEL maintainer="vaikas@chainguard.dev"
LABEL version="0.1"
LABEL description="Hello World Python container"


WORKDIR /app

ADD ./source/my_script.py .
COPY venv .
ENV VIRTUAL_ENV="./"
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"
ENV PYTHONPATH=./lib/python3.10/site-packages
CMD [ "python", "./my_script.py" ]

