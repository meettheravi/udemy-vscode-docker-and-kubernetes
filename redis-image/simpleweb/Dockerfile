# Specify a base image
FROM node:14-alpine

# Install some dependencies
# copy everything from current context (active directory to current work dir inside container)
COPY ./ ./
RUN npm install

# Default command
CMD ["npm", "start"]