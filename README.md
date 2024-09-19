# VisualVibe
This is a sample application trying out things.

To build the docker image move into the VisualVibe folder and run the following command (. is important at the ind):
```
docker build -f VisualVibe.Api/Dockerfile --force-rm -t visualvibeapp .
```
* `-f VisualVibe.Api/Dockerfile:`
`-f` option allows you to specify the path to the Dockerfile.
In this case, the Dockerfile is located in the VisualVibe.Api directory.
If you don't specify the -f option, Docker will look for a Dockerfile in the current directory.

* `--force-rm:`
This option forces Docker to remove intermediate containers (used during the build process) even if the build fails.
Normally, Docker only removes intermediate containers after a successful build. By using --force-rm, it ensures that these containers are cleaned up whether the build succeeds or not.

* `-t visualvibeapp:`
The -t option is used to tag the built image with a name (visualvibeapp in this case).
This makes it easier to refer to the image later (e.g., when running it with docker run).

* `. (dot):`
The dot at the end specifies the build context, which is the directory that Docker will use to copy files into the image. In this case, the context is the current directory (.).
Docker sends the contents of this directory (and subdirectories) to the Docker daemon, but it only uses the files specified in the Dockerfile.
