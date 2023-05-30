## `gazebo:latest`

```console
$ docker pull gazebo@sha256:69e885bbdc326bf7c2cbdb34a2fbe9f4a5f26908b131bf91d2ddf0734dff9565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:58c86a1e9bfe5bd5035349679fba796ec4710287b612e18ff96438c620ead6a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.1 MB (612147842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ad241ba12109c0213d356346af82fcf63cc89c767d1bea1ee98d370dfdd26e`
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
# Tue, 30 May 2023 20:33:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 May 2023 20:33:19 GMT
EXPOSE 11345
# Tue, 30 May 2023 20:33:19 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 30 May 2023 20:33:19 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 30 May 2023 20:33:19 GMT
CMD ["gzserver"]
# Tue, 30 May 2023 20:37:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.13.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:93f6e42ae9614142514184e116ba0d99a8c9ebc37ff5abe076fa79ed7ba856f0`  
		Last Modified: Tue, 30 May 2023 20:39:54 GMT  
		Size: 276.0 MB (276018134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447fecdc814f32d47afd2534f0e2d24fd8f9005f09d15a01de1d369174c4a429`  
		Last Modified: Tue, 30 May 2023 20:39:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd43bf1a88b46009880cfb513b12edbaed40c02a9d0cc1b4988907ff5c4045c4`  
		Last Modified: Tue, 30 May 2023 20:40:46 GMT  
		Size: 290.2 MB (290207615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
