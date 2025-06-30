# Build React app using Node
FROM node:18 AS build

WORKDIR /app
COPY . .

# Install dependencies and build the app
RUN npm install
RUN npm run build

# Serve the build using Nginx
FROM nginx:stable-alpine

COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 3000

CMD ["nginx", "-g", "daemon off;"]

