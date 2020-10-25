FROM ubuntu

WORKDIR /app

ENV DENO_INSTALL=/root/.deno
ENV PATH=$DENO_INSTALL/bin:$PATH

RUN apt-get -y update \
  && apt-get -y upgrade \
  && apt-get -y install curl unzip git \
  && curl -fsSL https://deno.land/x/install/install.sh | sh \
  && apt-get -y remove curl unzip \
  && apt-get -y autoremove \
  && apt-get clean

EXPOSE 3000
