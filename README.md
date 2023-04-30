# A Simple Flask App

---

```sh
docker build -t flask-simple-app .
```

> `docker build` command uses the Dockerfile to build a new container image
> the -t flag tags your image. Think of this simply as a human-readable name for the final image.
> `.` at the end of the docker build command tells Docker that it should look for the Dockerfile in the current directory

```sh
docker run -dp 5000:5000 --name flask-simple-app flask-simple-app
```

> You use the -d flag to run the new container in “detached” mode (in the background). You also use the -p flag to create a mapping between the host’s port 3000 to the container’s port 3000. Without the port mapping, you wouldn’t be able to access the application.
> `--name` https://docs.docker.com/engine/reference/commandline/run/

---

Best practices for writing Dockerfiles | Docker Documentation
https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

The best Docker base image for your Python application (March 2023)
https://pythonspeed.com/articles/base-image-python-docker-images/

Docker Best Practices for Python Developers | TestDriven.io
https://testdriven.io/blog/docker-best-practices/#use-unprivileged-containers
