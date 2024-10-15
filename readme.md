Taibun Request Handler
---

## Why we need this ?
Taibun server is not stable, so we make the structure of the Correction System into microservices. This is the request handler that handles user requests to the corresponding server.
```
front_end(140.116.153.134) => request handler(140.116.245.154)
```
if a request wants to get audio, then
```
redirect request => audio_getter(140.116.153.134)
```

if a request wants to do something else, then
```
redirect request => main_backend(140.116.245.155)
```

#### The Request Handler is running on `140.116.245.154`, the file is currently store at `/home/p76121479/Linux_DATA/KuangFu`, you can move it if you want.

## RUN
```sh
docker compose up --build -d
```

## STOP
```sh
docker compose down
```