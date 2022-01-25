# hello-world

Sample docker image to test docker deployments
Created from original `tutum` repo for my own demonstrations.

## Usage

To create the image `<USERNAME>/hello-world`, execute the
following command on the hello-world folder:

```sh
docker build -t <USERNAME>/hello-world .
```

You can now push your new image to the registry:

```sh
docker push <USERNAME>/hello-world
```

## Running your Hello World docker image

Start your image:

```sh
docker run -d -p 80 <USERNAME>/hello-world
```

It will print the new container ID (like `d35bf1374e88`).
Get the allocated external port:

```sh
docker port d35bf1374e88 80
```

It will print the allocated port (like 4751). Test your deployment:

```sh
curl http://localhost:4751/
```

Hello world!
