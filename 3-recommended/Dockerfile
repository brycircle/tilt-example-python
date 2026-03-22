FROM python:3.15-rc-alpine3.22

# Default value; will be overridden by build-args, if passed
ARG flask_debug=False

ENV FLASK_DEBUG $flask_debug

WORKDIR /app

ADD requirements.txt .
RUN pip install -r requirements.txt

ADD . .

ENTRYPOINT ["python", "/app/app.py"]
