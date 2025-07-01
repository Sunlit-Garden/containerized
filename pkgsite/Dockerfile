FROM golang:1.24.4-alpine3.22

ARG VERSION=v0.0.0-20250624191723-ae590d8f0828

LABEL org.opencontainers.image.source="https://github.com/Sunlit-Garden/containerized"
LABEL org.opencontainers.image.version=${VERSION}
LABEL org.opencontainers.image.description="Image of https://pkg.go.dev/golang.org/x/pkgsite"

ENV GOPROXY=https://proxy.golang.org
RUN go install golang.org/x/pkgsite/cmd/pkgsite@${VERSION}

EXPOSE 8080
ENTRYPOINT ["pkgsite", "-proxy", "-http", ":8080"]
