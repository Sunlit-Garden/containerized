FROM golang:1.23.0-alpine3.20
LABEL org.opencontainers.image.source="https://github.com/anesthetised/containerized"
ENV GOPROXY=https://proxy.golang.org
RUN go install golang.org/x/pkgsite/cmd/pkgsite@v0.0.0-20240824135812-676c19eae995
EXPOSE 8080
ENTRYPOINT ["pkgsite", "-proxy", "-http", ":8080"]
