FROM node:14 as build-stage
WORKDIR /bezkoder-ui
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx:1.17.0-alpine
COPY --from=build-stage /bezkoder-ui/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
