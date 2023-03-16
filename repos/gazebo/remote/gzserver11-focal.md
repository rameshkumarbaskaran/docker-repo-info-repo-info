## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:36165f8285fa8671cb892bfa571761b0f3c4194bcc820f4cc8b35a061f491e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:bfa91f6895f15e3aa123e54538d6db75934a8de21046a48db2e6114201d9cb9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321936156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fa698d1631023479a67c9fa63ad10a54ee447514ec764705685531a6caf0c9`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:03:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:03:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:03:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 16 Mar 2023 03:03:59 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 16 Mar 2023 03:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:06:57 GMT
EXPOSE 11345
# Thu, 16 Mar 2023 03:06:57 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 16 Mar 2023 03:06:57 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 16 Mar 2023 03:06:57 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03a3bf9c2e8661d0de58d4a85390b5a17d80f3abf64250efc0769650aa9ab69`  
		Last Modified: Thu, 16 Mar 2023 03:13:05 GMT  
		Size: 1.2 MB (1154522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03434b03c3217cb212bd5c39cc9574ff28507208b0ef48aae66a2b52fc74142a`  
		Last Modified: Thu, 16 Mar 2023 03:13:05 GMT  
		Size: 16.2 MB (16177907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6c5c2fcea5e2a2391135525c08cb219f18b85effff8524a8ccdbc404e4b622`  
		Last Modified: Thu, 16 Mar 2023 03:13:03 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383022c5af31d0bc3862605b602168047e44661db9ca84b0da7078485ca8d3c4`  
		Last Modified: Thu, 16 Mar 2023 03:13:03 GMT  
		Size: 5.5 KB (5503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9951aad64747d44e284984efba4afb53367de1822435ed28d2a28abfffcd700c`  
		Last Modified: Thu, 16 Mar 2023 03:13:41 GMT  
		Size: 276.0 MB (276018530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdf93d039c14712fec14f8720cae24b3e3ed2d400d4f580b3d9a92186a05368`  
		Last Modified: Thu, 16 Mar 2023 03:13:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
