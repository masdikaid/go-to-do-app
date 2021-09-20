FROM node:13.12.0-alpine as build
WORKDIR /code
COPY . .
RUN npm install
RUN npm run build

FROM nginx:stable-alpine
COPY --from=build /code/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]