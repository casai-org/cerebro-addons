ARG BUILD_ARCH
ARG BUILD_FROM
FROM casai/amd64-ngrok_client:latest AS ngrok_base

FROM $BUILD_FROM AS homeassistant_base

RUN apk update && apk upgrade && apk add --no-cache curl
RUN mkdir /app

COPY --from=ngrok_base /app /app

COPY rootfs /