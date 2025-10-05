FROM node:22-alpine AS build-stage
WORKDIR /frontend-app
COPY package.json ./
COPY public public
COPY src src

RUN npm install
RUN npm run build

FROM nginx:alpine-slim
ARG APP_ENV=dev
COPY --from=build-stage /frontend-app/build /usr/share/nginx/html

CMD [ "nginx", "-g", "daemon off;" ]

# /frontend-app/build
