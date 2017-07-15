FROM httpd:2.4

# Replace shell with bash so we can source files
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

EXPOSE 80 35729

RUN apt-get update \
    && apt-get install -y curl \
    && apt-get -y autoclean

# setup nvm environment variables
ENV NVM_DIR /usr/local/nvm
ENV NODE_VERSION 8.4.0

# install nvm
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.4/install.sh | bash

#install node and npm
RUN source $NVM_DIR/nvm.sh \
    && nvm install $NODE_VERSION \
    && nvm alias default $NODE_VERSION \
    && nvm use default

# update PATH
ENV NODE_PATH $NVM_DIR/v$NODE_VERSION/lib/node_modules
ENV PATH $NVM_DIR/versions/node/v$NODE_VERSION/bin:$PATH

RUN node -v
RUN npm -v

RUN npm install -g livereload
RUN livereload /usr/local/apache2/htdocs

LABEL maintainer="zoltan.nz"