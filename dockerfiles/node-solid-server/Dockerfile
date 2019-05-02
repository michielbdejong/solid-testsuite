FROM node
RUN git clone https://github.com/solid/node-solid-server
WORKDIR node-solid-server
RUN npm install
ADD ./runtime /runtime
WORKDIR /runtime
EXPOSE 8443/tcp
CMD ../node-solid-server/bin/solid start
