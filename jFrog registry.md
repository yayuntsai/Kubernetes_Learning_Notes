1. Get images ID 
```$ docker image ls```


2. Login to Docker Repository
```$ docker login <registry link>```

3. Push Docker Images to Docker Repository
```$ docker tag <imageid>  <registry path>/<main_directory>/<sub_directory>/<app_name> ```

4. ```$ docker push <imageid>  <registry path>/<main_directory>/<sub_directory>/<app_name> ```
