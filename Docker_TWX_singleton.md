1. [Install Docker](https://docs.docker.com/compose/install/)
2. Download Thingworx [Docker files](https://support.ptc.com/appserver/auth/it/esd/product.jsp?prodFamily=TWX)
![image](https://user-images.githubusercontent.com/22999436/204716886-d3ec9e0d-5623-4746-ab6d-cf188c385efd.png)

3. Download [Java](https://docs.aws.amazon.com/corretto/latest/corretto-11-ug/downloads-list.html) and put it into staging folder
![image](https://user-images.githubusercontent.com/22999436/204716976-30630c83-e39e-4872-b208-8b8bc306776d.png)

4. Modify build.env with the downloaded Java version/PLATFORM_VERSION
![image](https://user-images.githubusercontent.com/22999436/205849163-809aa72c-66b6-4a0e-9758-6ce31978f0df.png)

5. ```$./build.sh```

6. Update docker-compose-postgres.yml
For postgres, specify TWX_DATABASE_USERNAME, TWX_DATABASE_PASSWORD, and TWX_DATABASE_SCHEMA in both the postgresql and platform sections, and THINGWORX_INITIAL_ADMIN_PASSWORD in the platform section. Ensure you define the variables identically in both postgresql and platform sections for the environment to get started. Additional variables for postgresql and their details can be found at the Docker Hub.

7. ```$docker-compose -f docker-compose-postgres.yml up -d```
