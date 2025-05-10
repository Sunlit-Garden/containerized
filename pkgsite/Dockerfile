FROM golang:1.24.3-alpine3.21

ARG VERSION=v0.0.0-20250508150449-e476b3e60948

LABEL org.opencontainers.image.source="https://github.com/anesthetised/containerized"
LABEL org.opencontainers.image.version=${VERSION}
LABEL org.opencontainers.image.description="Image of https://pkg.go.dev/golang.org/x/pkgsite"

ENV GOPROXY=https://proxy.golang.org
RUN go install golang.org/x/pkgsite/cmd/pkgsite@${VERSION}

EXPOSE 8080
ENTRYPOINT ["pkgsite", "-proxy", "-http", ":8080"]
