# A Simple Flask App

---

```sh
docker-compose up -d
docker-compose up -d --build

docker-compose down
```

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

docker-compose up doesn't rebuild image although Dockerfile has changed · Issue #1487 · docker/compose
https://github.com/docker/compose/issues/1487

> A bind mount is another type of mount, which lets you share a directory from the host’s filesystem into the container. When working on an application, you can use a bind mount to mount source code into the container. The container sees the changes you make to the code immediately, as soon as you save a file. This means that you can run processes in the container that watch for filesystem changes and respond to them.

Use bind mounts | Docker Documentation
https://docs.docker.com/get-started/06_bind_mounts/

Bind mounts | Docker Documentation
https://docs.docker.com/storage/bind-mounts/#use-a-bind-mount-with-compose

Docker volumes vs. bind mounts - LogRocket Blog
https://blog.logrocket.com/docker-volumes-vs-bind-mounts/

---

##### About Ruff

charliermarsh/ruff: An extremely fast Python linter, written in Rust.
https://github.com/charliermarsh/ruff

Configuration - Ruff
https://beta.ruff.rs/docs/configuration/#command-line-interface

Ruff: one Python linter to rule them all
https://blog.jerrycodes.com/ruff-the-python-linter/

charliermarsh/ruff-vscode: A Visual Studio Code extension with support for the Ruff linter.
https://github.com/charliermarsh/ruff-vscode

---
