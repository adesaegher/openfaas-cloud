FROM arm64v8/python:3.6-alpine

ADD https://github.com/openfaas/faas/releases/download/0.8.2/fwatchdog-arm64 /usr/bin/fwatchdog
RUN chmod +x /usr/bin/fwatchdog

RUN apk add --no-cache figlet

# Populate example here
ENV fprocess="figlet"

HEALTHCHECK --interval=5s CMD [ -e /tmp/.lock ] || exit 1
CMD ["fwatchdog"]

