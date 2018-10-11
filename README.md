# Matlab Runtime

We provide the Matlab Runtime built on a Debian 9.

## Usage

You can use it in other Dockerfile as follow :

```
# For a Java project
FROM thewykiki/matlab:r2017b-debian-9 as matlab

FROM openjdk:10-jre

COPY --from=matlab /opt/mcr /opt/mcr

ENV LD_LIBRARY_PATH /opt/mcr/v93/runtime/glnxa64

# Further Dockerfile instructions ...
```
