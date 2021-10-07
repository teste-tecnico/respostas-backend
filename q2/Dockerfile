FROM golang

WORKDIR home

# Compartilhamento de pasta com binário ao host
VOLUME ["/home"]

COPY hello.go hello.go

# comando para criação de executável
ENTRYPOINT ["go","build"]
CMD ["hello.go"]
