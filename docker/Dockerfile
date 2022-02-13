FROM python:3.10-slim@sha256:ca2a31f21938f24bab02344bf846a90cc2bff5bd0e5a53b24b5dfcb4519ea8a3

# LABEL about the custom image
LABEL maintainer="vaikas@chainguard.dev"
LABEL version="0.1"
LABEL description="Hello World Python container"

WORKDIR /

ADD ./source/my_script.py .
COPY venv .
RUN echo "Doing LS"
RUN ls -R .
RUN echo "Done running LS"

RUN echo "setting up the venv!!!!!!!"
ENV VIRTUAL_ENV="./venv"
RUN echo "Really setting up the venv"
RUN which python
RUN python -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

RUN echo "Listing virtual env"
RUN ls -R $VIRTUAL_ENV

RUN echo "CURRENT:"
RUN ls -R .
RUN echo $PATH
CMD [ "python", "./my_script.py" ]

