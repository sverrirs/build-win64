# build-win64

Build a libvips binary for 64-bit Windows. This produces a binary that seems
to work, at least at a basic level.  More testing required!

See the README in the 8.1 subdirectory for instructions for building directly
in `jhbuild`.

### Build with docker

You can also build inside a docker container. Docker will make a light-weight
virtual machine containing all the tools you need and build inside that. You
won't need to install any extra stuff on the host machine, and everything is
automated.

First, install docker:

```
sudo apt-get install docker.io
```

Then pass the build instructions to the docker service. You have to run this
as root.

```
sudo ./build.sh 8.1
```

At the end of the build, the script will display the paths of all the zip
files it created, ready to be uploaded to the server. Be patient, this process
can take an hour, even on a powerful machine. 

### TODO

- do a native linux build as well, so we get a typelib

  we wouldn't need any of the optional components, just a minimal build

- try installing win32 python and running it under wine so we can run the test
  suite? who knows, it could work


