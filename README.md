# Dockerized UD-Demo-TIGA-Morphogenese

This container wraps the [morphogenese](https://github.com/VCityTeam/UD-Demo-TIGA-Morphogenese-Lyon) demo.

Build the docker image with

```bash
docker build -t vcity:morpho .
```

no cache options :

```bash
docker build --no-cache -t vcity:morpho .
```

If you want specify a branch name or commit name for UD-Demo-TIGA-Morphogenese-Lyon use this

```bash
docker build -t vcity:morpho --build-arg checkoutName=name .
```

no cache options :

```bash
docker build --no-cache -t vcity:morpho --build-arg checkoutName=name .
```

Then run the container e.g. with

```bash
docker run [--detach] --rm -t vcity:morpho
```

Run with redirection of port

```bash
docker run -p 0.0.0.0:8000:80 --detach --rm -t vcity:morpho
```

and open a web browser on URL `http://localhost:8000/`

Note: in the above `docker run` command the optionnal `-d` argument requires the container to run in detached mode
