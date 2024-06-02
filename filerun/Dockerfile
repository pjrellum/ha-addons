#################
# 1 Build Image #
#################

ARG BUILD_FROM
FROM ${BUILD_FROM}



ENV HEALTH_PORT="8182" \
    HEALTH_URL=""
HEALTHCHECK \
    --interval=5s \
    --retries=5 \
    --start-period=30s \
    --timeout=25s \
    CMD curl --fail "http://127.0.0.1:${HEALTH_PORT}${HEALTH_URL}" &>/dev/null || exit 1