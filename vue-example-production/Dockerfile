# build
FROM node:lts-alpine as build
WORKDIR /app
COPY example-project/package*.json ./
RUN npm install
COPY example-project .
RUN npm run build

# production
FROM nginx:stable-alpine as prod
COPY --from=build /app/dist /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]