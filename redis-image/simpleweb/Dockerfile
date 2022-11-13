# Specify a base image
# Also updated this to alpine now as previously run would fail with newer versions without 'WORKDIR'
FROM node:alpine
WORKDIR /usr/app

# Install some dependencies
# copy everything from current context (active directory to current work dir inside container)
COPY ./ ./
RUN npm install

# Default command
CMD ["npm", "start"]