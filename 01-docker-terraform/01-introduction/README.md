## Run container
- docker run image/ docker run -it image

## Managing containers
List containers: docker ps -a
Stop container: docker stop < container_id/name >
Start container: docker start < container_id/name>
* Not a good practice to restart container as they take space
Delete containers: docker rm `docker ps -aq`
            automatically delete: docker run -it --rm

## Volumes
Volume mapping.
    Without volumes:
        - you install things, save data, or run your app
        - destroy container -> everything is gone
    With volumes:
        - keep data safe
        - separate storage from containers
        - can rebuild and replace containers freely
    - docker run -it -v [bind mounts or named volumes]