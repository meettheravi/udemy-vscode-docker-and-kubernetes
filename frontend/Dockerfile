FROM node:16-alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
# serves as an instruction for user of the image to open the port when it is run. IT DOES NOTHING.
EXPOSE 80
# refer phase from alias mentioned above
COPY --from=builder /app/build /usr/share/nginx/html

# to run using this dockerfile
# 1. docker build .
# 2. docker run -p 8080:80 <image_id_created>
# nginx port is by default 80 for receiving requests.