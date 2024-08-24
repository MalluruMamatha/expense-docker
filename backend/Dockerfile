## used alpine 20 / official image 
FROM node:20.15.0-alpine3.20
EXPOSE 8080
ENV DB_HOST=mysql
### i have user alpine image here ,so adding user the command will vary from image to image
RUN addgroup -S expense && adduser -S expense -G expense \
    && mkdir /opt/server \
    &&chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
USER expense
CMD [ "node", "index.js" ]

