$ docker build --no-cache  -t hello-go . -f Dockerfile-without-multistage --load
Result:
hello-go        latest            036fdbd1b561   17 seconds ago   849MB

$ docker build --no-cache  -t hello-go . -f Dockerfile-with-multi-stage --load
Result:
hello-go        latest            aadfd70ec6d0   5 seconds ago        10MB

Observation:
* Using multistage, image size can be reduced