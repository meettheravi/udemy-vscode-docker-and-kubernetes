# Use an existing docker image as a base
FROM alpine

# Download and install a dependency
RUN apk add --update gcc
RUN apk add --update redis

# Tell the image what to do when it starts as a container
CMD ["redis-server"]

# Instead of using dockerfile, manually same can be achieved by modifying container. Same can be committed and pushed to preserve.
# E.g.:
# docker run -it alpine sh
# apk add --update redis
# In other terminal or after stopping the container, get the container id by docker ps
# docker commit -c 'CMD ["redis-server"]' container_id
# -c - provides startup command