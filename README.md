## Requirements
### The recommended way
It is recommended to use our official Docker image for building. To do so, run
```bash
docker run -it --rm --name flecs-build -v $(pwd):$(pwd) -w $(pwd) flecspublic.azurecr.io/flecs-build:v4.0.0-snowhare
```

from the repository's root directory.

If you intend to build Docker images as well (such as our System Apps), make sure to mount yout local Docker socket:
```bash
docker run -it --rm --name flecs-build -v $(pwd):$(pwd) -v /run/docker.sock:/run/docker.sock -w $(pwd) flecspublic.azurecr.io/flecs-build:v4.0.0-snowhare
```