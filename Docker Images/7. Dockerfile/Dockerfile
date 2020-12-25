FROM centos as stage

RUN fallocate -l 10M /opt/file1

RUN fallocate -l 20M /opt/test2

RUN fallocate -l 30M /opt/test3

FROM alpine

COPY --from=stage /opt/test2 /opt/myfile