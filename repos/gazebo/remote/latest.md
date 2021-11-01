## `gazebo:latest`

```console
$ docker pull gazebo@sha256:b93644ac182cd6d7d48b7db117b625cf8619ca675e2b2d3dfb3783bc287f9ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:e7d9493b73c22134cad9eaf139947150adad0fbf194774a9480507ad8919cc89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605585720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c718c8045650962e902b165dd4db98af588e3bfcd89b6d6c1882b2fb97202c62`
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
# Mon, 01 Nov 2021 22:58:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.9.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Nov 2021 22:58:23 GMT
EXPOSE 11345
# Mon, 01 Nov 2021 22:58:24 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 01 Nov 2021 22:58:24 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 01 Nov 2021 22:58:24 GMT
CMD ["gzserver"]
# Mon, 01 Nov 2021 23:03:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.9.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:3b5d09d08119a5c2da7141c5c9e73699dded59c76eee2e31cf3418e97d0d8b18`  
		Last Modified: Mon, 01 Nov 2021 23:06:03 GMT  
		Size: 275.0 MB (275002821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fa2021d4df1f6be12d1c96e1ffeb9dcbfbfdb6db3f5c2c676a1e4b3de10d07`  
		Last Modified: Mon, 01 Nov 2021 23:05:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33afca74bdf207adb9e7172a92b73958a0a5e2535286547e784cda72122d10b3`  
		Last Modified: Mon, 01 Nov 2021 23:06:58 GMT  
		Size: 284.7 MB (284653446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
