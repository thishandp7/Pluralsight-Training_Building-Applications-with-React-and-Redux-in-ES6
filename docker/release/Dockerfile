FROM node:alpine

RUN mkdir -p /app
WORKDIR /app

COPY target/package.json /app
RUN npm install --production && npm install -g babel-cli

COPY target /app

ENV NODE_ENV production
ENV PORT 3000

EXPOSE 3000

CMD ["babel-node", "tools/distServer" ]
