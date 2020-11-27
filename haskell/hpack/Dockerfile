FROM haskell:8.6.5

MAINTAINER Hamilton 

RUN apt-get update 

# RUN apt-get -y install libblas-dev libatlas-dev liblapack-dev libgsl0-dev libghc-postgresql-libpq-dev libicu-dev libtinfo-dev curl
# RUN apt-get -y install libblas-dev libatlas-dev liblapack-dev libgsl0-dev libghc-postgresql-libpq-dev libicu-dev libssl-dev openssl wget

# RUN curl -sSL https://get.haskellstack.org/ | sh

# RUN wget -qO- https://get.haskellstack.org/ | sh

# RUN cabal update

# RUN cabal install hmatrix hunit containers xml mtl postgresql-simple utf8-string ccmdlib cmdargs


RUN stack --system-ghc install hpack

ENTRYPOINT ["/bin/bash"]

