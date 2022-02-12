FROM python:3

RUN ls -R /

ADD ./source/my_script.py /

COPY venv .
ENV VIRTUAL_ENV=./venv
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"


CMD [ "python", "./my_script.py" ]

