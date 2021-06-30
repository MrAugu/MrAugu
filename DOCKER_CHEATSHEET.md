# Listing containers
**Running containers**

```
docker container ls
```

**All containers**

```
docker container ls -a
```

**Old shorthand for running containers**

```
docker ps
```

**Old shorthand for all containers**

```
docker ps -a
```

# Removing containers
**One container**

```
docker container rm [container_id/name] -f
```

**All in bulk**

```
docker container rm $(docker ps -aq) -f
```

# Pulling images

```
docker pull [image_name]
```

# Listing images

```
docker images
```

# Deleting images

```
docker image rm [image_id]
```

# Starting containers
**Starting in normal mode**

```
docker container run -p [inside_container_port]:[outside_container_port] --name [custom_name_for_container] [image_name]
```

**Starting in detached mode**

```
docker container run -d -p [inside_container_port]:[outside_container_port] --name [custom_name_for_container] [image_name]
```

**Starting with environment variables from command**

```
docker container run -d -p [inside_container_port]:[outside_container_port] --name [custom_name_for_container] --env [variable_name]=[variable_content] [image_name]
```

**Starting with environment variables from file**

```
docker container run -d -p [inside_container_port]:[outside_container_port] --name [custom_name_for_container] --env-file [environment_file_name/path] [image_name]
```

**Starting with volume**

```
docker docker container run -d -p [inside_container_port]:[outside_container_port] --name [custom_name_for_container] --env-file [environment_file_name/path] -v [absolute_folder_path_outside_container]:[absolute_folder_path_inside_container] [image_name]
```

# Stopping containers

```
docker container stop [container_id/name]
```

# Bashing into container
**Entering container**

```
docker container exec -it [container_id/name] bash
```

**Exiting container**

```
exit
```

# Building images

```
docker image build -t [username]/[image_name] .
```

# Pushing images

```
docker push [username]/[image_name]
```
