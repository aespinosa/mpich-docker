FROM aespinosa/mpich:latest

ADD hello.f90 /hello.f90
RUN mpif90 /hello.f90 -o /hello
