# Behat Docker Image


A self-contained Docker image to run Behat with no external dependencies.

This image is part of the [Docksal](http://docksal.io) project.

Features:

- PHP7, Composer
- Behat 3.x

## Added REST API testing functionality.


## Usage

 

Use this image as if you were using a binary.  
Working directory is expected to be mounted at `/src` in the container.

```
$ docker run --rm -v $(pwd):/src docksal/behat --version
behat version 3.1.0
```

You can also add a shell alias (in `.bashrc`, `.zshrc`, etc.) for convenience.

```
alias behat='docker run --rm -v $(pwd):/src docksal/behat --colors "$@"'
```

Restart your shell or open a new one, then

```
$ behat --version
behat version 3.1.0
```


## Sample setup

Sample setup and tests can be found in the [example](example) folder.
 
Features:

- Sample tests

## Debugging

The following command will start a bash session in the container.

```
docker run --rm -v $(pwd):/src -it --entrypoint=bash docksal/behat
```
