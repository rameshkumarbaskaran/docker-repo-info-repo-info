## `gazebo:latest`

```console
$ docker pull gazebo@sha256:9c98672e1d8a1d54b179203f5ef61cb4c7dede1d92ee4e44523ff8e156be54d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:b1dbda9a6bcdb133c20108094d2eae770b7575dd91882431daab1e8d0df74070
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.7 MB (615699501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7fd6616b1ca70921ad61b562bd64b340ffd377d5d7fb35332c6aeadee4ca2a`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:53:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:53:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:53:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 16 Oct 2021 02:53:35 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 17 Dec 2021 19:14:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.9.1-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Dec 2021 19:14:14 GMT
EXPOSE 11345
# Fri, 17 Dec 2021 19:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 17 Dec 2021 19:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 17 Dec 2021 19:14:15 GMT
CMD ["gzserver"]
# Fri, 17 Dec 2021 19:20:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.9.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3c993d4c25d2ec8adbe5b497acc2226d8b6b602f68679037b8993f53617e2b`  
		Last Modified: Sat, 16 Oct 2021 03:02:27 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f063abb73e10805d2ce88263411405ffb32082608644c3d370a371c08dd6dd4`  
		Last Modified: Sat, 16 Oct 2021 03:02:28 GMT  
		Size: 16.2 MB (16169048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a180d646a584a0bc397aab545307b4db9745d4486ffce857d810c9638cd3f6c2`  
		Last Modified: Sat, 16 Oct 2021 03:02:24 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba0dd022182c042a1f9be8465aeb11cac4821d860a6fbbca9c2505b4768738`  
		Last Modified: Sat, 16 Oct 2021 03:02:24 GMT  
		Size: 5.5 KB (5500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b189de8ec072652c777e70d243709918673f1704b69a2d44eabec0fbc88c7`  
		Last Modified: Fri, 17 Dec 2021 19:22:42 GMT  
		Size: 275.0 MB (275014561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdafcb874ddb38a48f2fbcd17e1c1d90514403fee115839987b16563b74e30ee`  
		Last Modified: Fri, 17 Dec 2021 19:22:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d6f340d8584b1859af50c1c34913caf79f3b48c50995add04cd767ef989b2b`  
		Last Modified: Fri, 17 Dec 2021 19:23:40 GMT  
		Size: 294.8 MB (294755486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
