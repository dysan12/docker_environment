FROM node:8.4.0

RUN useradd --user-group --create-home --shell /bin/false dysan &&\
    npm install
    
ENV HOME=/home/app

USER dysan

WORKDIR $HOME
