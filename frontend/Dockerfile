FROM node:lts-alpine
WORKDIR /app
ENV PATH /app/node_modules/.bin:$PATH
EXPOSE 8080

COPY package.json /app/
RUN npm install @vue/cli@3.7.0 -g
RUN npm install --silent

COPY . /app/
CMD ["npm", "run", "serve"]