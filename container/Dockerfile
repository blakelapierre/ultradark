FROM elixir:alpine

RUN apk update && apk add binutils-libs binutils libgomp pkgconf pkgconfig mpfr3 mpc1 gcc make musl-dbg musl-dev linux-headers libc-dev libgcc g++ git

RUN git clone https://github.com/UltraDark/UltraDark

RUN cd UltraDark && (yes | mix deps.get)
RUN cd UltraDark && (yes | mix compile)

CMD /bin/sh