FROM golang

WORKDIR home

VOLUME ["/go/home", .]

COPY hello.go hello.go

ENTRYPOINT ["go","build"]
CMD [ "hello.go" ]
