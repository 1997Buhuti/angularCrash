#stage 1

FROM node:latest as node 
WORKDIR /app
COPY ..
RUN nmp install
RUN npm run build --prod

#stage 2
FROM nginx:alpaine 
COPY --from=node /app/dist/angular-app /usr/share/nginx/html