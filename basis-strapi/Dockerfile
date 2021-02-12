FROM strapi/base

WORKDIR /srv/app

COPY ./package.json ./
COPY ./yarn.lock ./
COPY ./favicon.ico ./

RUN yarn install

COPY api /srv/app/api/

COPY config /srv/app/config/

RUN mkdir -p /srv/app/extensions

ENV NODE_ENV production

RUN yarn build

EXPOSE 1337

CMD ["yarn", "start"]
