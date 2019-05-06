FROM node
RUN git clone https://github.com/inrupt/wac-ldp
WORKDIR wac-ldp
RUN npm install
RUN npm run build
EXPOSE 8080/tcp
ENV DEBUG *
CMD npm start
