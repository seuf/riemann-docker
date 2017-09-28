# riemann-docker
Riemann Dockerfile based on alpine

## Build

```
docker build -t seuf/riemann
```

## run

```
docker run --name riemann -d -p 5555:5555 -p 5555:5555/udp -p 5556:5556 seuf/riemann:0.2.14
```

## configure

you can mount your configuration directory to /app/riemann-0.2.14/etc.
Example :

```
docker run --name riemann -d -p 5555:5555 -p 5555:5555/udp -p 5556:5556 -v /home/seuf/riemann/etc:/app/riemann-0.2.14/etc seuf/riemann
```
