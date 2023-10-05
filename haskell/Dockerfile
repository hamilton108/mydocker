FROM haskell:9.4 as builder

RUN stack setup 

RUN stack install hpack

FROM haskell:9.4

MAINTAINER Hamilton 

RUN mkdir -p /root/.local/bin

COPY --from=builder /root/.local/bin/hpack /root/.local/bin/hpack

ENTRYPOINT ["/bin/bash"]

