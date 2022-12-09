## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:55ee7964f5077c99e6c574414b1a6f331c08177f4129cbcf9bc19bbb52952ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:1b9e230df69a5a86b176dbfc616f07bcbceaf4a2022610e09894d5beda30de51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277826450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de3137cac266ec8a75d069e95f9e46d1314aa987addd23521282df339b42e88`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:56:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:56:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:56:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 09 Dec 2022 01:56:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 09 Dec 2022 02:03:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:03:23 GMT
EXPOSE 11345
# Fri, 09 Dec 2022 02:03:24 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 09 Dec 2022 02:03:24 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 09 Dec 2022 02:03:24 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45265e2e7c48feafb38d0b16636d20d32043625dc345459a4518d1d7a29dae6`  
		Last Modified: Fri, 09 Dec 2022 02:14:58 GMT  
		Size: 820.1 KB (820060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1883b837265d80159eb0376d2e42f443112bb88276d8642cba372dff88ae7b77`  
		Last Modified: Fri, 09 Dec 2022 02:14:58 GMT  
		Size: 14.7 MB (14710047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19eb5dbd8ec5dabf4d8b6bd67b83d6278a595c0b698720498d3fa03f6e6ff39d`  
		Last Modified: Fri, 09 Dec 2022 02:14:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f0aaed8562434899431865a8814e155bcfe50166ccbe4c07ab9dd096c70538`  
		Last Modified: Fri, 09 Dec 2022 02:14:56 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43178ae06fe763555c89b2e8770b52a5751b587de134d65d34dc191244bf832b`  
		Last Modified: Fri, 09 Dec 2022 02:16:38 GMT  
		Size: 235.6 MB (235577793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cd08995a70281e368812b0d6f76e528ba0366e61a870485a67f53f41779ec4`  
		Last Modified: Fri, 09 Dec 2022 02:16:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
