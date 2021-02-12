FROM strapi/base

WORKDIR /srv/app

COPY basis-strapi/package.json ./
COPY basis-strapi/yarn.lock ./
COPY basis-strapi/favicon.ico ./

RUN yarn install

COPY basis-strapi/api /srv/app/api/

COPY basis-strapi/config /srv/app/config/

RUN mkdir -p /srv/app/extensions

ENV NODE_ENV production

RUN yarn build

EXPOSE 1337

CMD ["yarn", "start"]
