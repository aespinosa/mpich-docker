FROM aespinosa/mpich:latest

RUN apt-get --no-install-recommends install -y \
    libmpich-dev make\
    && apt-get clean
RUN mkdir -p /mpich/src/app
WORKDIR /mpich/src/app
ENV MPIEXEC_PORT_RANGE 1000:1000
EXPOSE 1000

ONBUILD COPY Makefile /mpich/src/app/
ONBUILD COPY . /mpich/src/app
ONBUILD RUN make
