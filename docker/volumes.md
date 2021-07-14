# Make Volumes
`docker volume create <volume_name>`
# List Volumes
`docker volume ls`
# Inspect Volume
`docker volume inspect <volume_name>`
# Remove Volume
`docker volume rm <volume_name>`

# Volume Location

# Start a container with a volume
# e.g. mounting volume to container's /app folder
`--mount source=<volume_name>, target=/app`
`docker inspect <container>` can be used to check if the volume is mounted
to the Mounts section

# Remove volume from container
Note, this doesn't remove the volume itself. Just the link to container
`docker stop <container>`
`docker container rm <container>`


