FROM node:8.11.4-alpine

RUN npm config set registry https://registry.npm.taobao.org/ \
&& npm i -g code-push-server@0.4.3 pm2@latest --no-optional

COPY ./process.json /process.json

EXPOSE 3000

CMD ["pm2-docker", "start", "/process.json"]
