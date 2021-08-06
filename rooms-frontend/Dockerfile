FROM node:latest as build
WORKDIR /usr/local/app
COPY ./ /usr/local/app/
RUN --mount=type=cache,target=/root/.m2 npm install
RUN --mount=type=cache,target=/root/.m2 npm run build
FROM nginx:latest
COPY --from=build /usr/local/app/dist/rooms-frontend /usr/share/nginx/html
EXPOSE 80