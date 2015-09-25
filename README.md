# pldistro-build

Dockerfiles for building various flavors of the PlanetLab distribution.  Example usage:

```
$ docker build -t mlab mlab-centos6-i386
$ docker run --privileged=true -ti mlab
[root@ad4bbcd6071c /]# cd build
[root@ad4bbcd6071c build]# ./build-pldistro.sh
```

The resulting RPM files can be found in /build/RPMS/ inside the container.
