FROM node:12.16-alpine AS dev-stage
WORKDIR /usr/src
COPY package.json ./
RUN npm install

COPY . .
CMD ["npm", "run", "serve"]


FROM dev-stage as build-stage
RUN npm run build


FROM nginx:1.17-alpine as deploy-stage
COPY --from=build-stage /usr/src/dist /usr/share/nginx/html
