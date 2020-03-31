FROM thewykiki/matlab:r2017b-debian-9 as matlab

FROM maven:3.6-jdk-11

COPY --from=matlab /opt/mcr /opt/mcr

ENV LD_LIBRARY_PATH /opt/mcr/v93/runtime/glnxa64
