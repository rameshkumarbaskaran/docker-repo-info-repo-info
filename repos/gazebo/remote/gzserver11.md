## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:e809188041869aa766393f32c981542254f29b63f5ee1d36696f9fefcc885682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:d2e0b326450385e5e95a365dece2c7ec31ebe796442fa928b58023daa579003e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321944943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a188b772441e0357de96a5a95c2f7e6aa46341dd44ee7ccb4dc3be7eae634d19`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:00:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:37:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:37:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 18 Apr 2023 01:37:55 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 18 Apr 2023 01:40:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:40:25 GMT
EXPOSE 11345
# Tue, 18 Apr 2023 01:40:25 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 18 Apr 2023 01:40:25 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 18 Apr 2023 01:40:25 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5ff3f6c5dd326a8361d5d9fba50621a210a6b840cadcc97c516817cb8cf8d7`  
		Last Modified: Tue, 18 Apr 2023 01:15:00 GMT  
		Size: 1.2 MB (1157164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86706d42b62d6d5a6bc799d4479e5cfa8ade7c2cba82b80f66513c23a7f587d3`  
		Last Modified: Tue, 18 Apr 2023 01:44:11 GMT  
		Size: 16.2 MB (16179241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7524529b119ab214bf4d1c9991928d331aef1aefeccd007dfdc18a3328c449ad`  
		Last Modified: Tue, 18 Apr 2023 01:44:08 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ed8551e301529f226bf35170053712264067f8e81adad6513e9d9cfaaafcdb`  
		Last Modified: Tue, 18 Apr 2023 01:44:08 GMT  
		Size: 5.5 KB (5496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8dd91972dc975c857536f92325d9f0b5a1b7102146c2494e6ae3472f651d08`  
		Last Modified: Tue, 18 Apr 2023 01:44:39 GMT  
		Size: 276.0 MB (276022850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc219bbaa3f2a4b2d0b1315219fc2cbc3b1b54df78f27171081f8c298ef9f7cd`  
		Last Modified: Tue, 18 Apr 2023 01:44:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
