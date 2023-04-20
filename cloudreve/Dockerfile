ARG VERSION=latest
FROM cloudreve/cloudreve:$VERSION AS builder

FROM alpine:3.17
RUN apk update && apk add --no-cache tzdata curl
COPY --from=builder /cloudreve/cloudreve /cloudreve
CMD ["/cloudreve", "-c", "/config/cloudreve.ini"]

