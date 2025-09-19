# Reverse Proxy with nginx in docker

This project is an example to allow many containers to be accessed from single entry point by using reverse proxy
with nginx.

In this example case, there are two website projects that need to be accessed from the same entry point and through `https`
to test cookie sharing between the two instance: 
- Web A is a regular vue3 which has `Dockerfile` set to expose port at 80.
- Web B is a nuxt3 project which by defaults expose port 3000.

Both webs located in different location and build as container separately. As such, the `docker-compose.yaml` references existing image instead of running build script for each web project.


### Running the project

```bash
docker compose up -d
```
