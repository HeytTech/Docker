FROM golang:alpine

RUN apk --update add git
RUN go get github.com/ekanite/ekanite
RUN go install github.com/ekanite/ekanite/cmd/ekanited
RUN ["/usr/bin/install", "-o", "root", "-g", "root", "-m", "0700", "-d", "/srv/ekanited"]

EXPOSE 514/tcp 514/udp 8080/tcp 9950/tcp 9951/tcp

VOLUME ["/srv/ekanited"]

ENTRYPOINT ["/go/bin/ekanited"]
CMD ["-datadir", "/srv/ekanited", "-diag", "0.0.0.0:9951", "-query", "0.0.0.0:9950", "-queryhttp", "0.0.0.0:8080", "-tcp", "0.0.0.0:514", "-udp", "0.0.0.0:514"]