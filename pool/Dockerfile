FROM golang:1.10.0

WORKDIR /go/src/app
RUN git config --global http.https://gopkg.in.followRedirects true
RUN git clone https://github.com/Cminers/core-pool.git

WORKDIR /go/src/app/core-pool
RUN make

COPY config.json .

CMD ["./build/bin/core-pool", "config.json"]
