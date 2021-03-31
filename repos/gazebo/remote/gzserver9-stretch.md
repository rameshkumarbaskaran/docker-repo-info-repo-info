## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:6621ceb376268c624c83fec5b54181c3b77ecb9d3c9ce5e959a410dcba8a78e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:f1529df89322451c34c52d369f46254b2aa7aa2b034663b46e1e3d53f5530657
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266182479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7899914a6ba0b7a30de366452dd72ef9a72fba8a3d13fcb543713657ac8590`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 03:33:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 03:33:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 31 Mar 2021 03:33:53 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 31 Mar 2021 03:34:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 03:34:57 GMT
EXPOSE 11345
# Wed, 31 Mar 2021 03:34:57 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 31 Mar 2021 03:34:58 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 31 Mar 2021 03:34:58 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41ca9d8f5ccc550383d5b850579cfcab16de8d76ec68e1fbc117c268f46a9db`  
		Last Modified: Wed, 31 Mar 2021 03:37:49 GMT  
		Size: 18.5 MB (18512491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04a7cddf5407eb864ae0cdf17198422d7bc5c91bf6203c2e76dec3754876c75`  
		Last Modified: Wed, 31 Mar 2021 03:37:42 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101b38b8461b6d92ef426595eb0dc5d0153e1912006f6acd3df1aa9b0a794d0a`  
		Last Modified: Wed, 31 Mar 2021 03:37:42 GMT  
		Size: 5.0 KB (5014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b699405ab5ac695b29dbf1be7dabba389a1e1d817a53d29edb8192283b7aeab4`  
		Last Modified: Wed, 31 Mar 2021 03:38:19 GMT  
		Size: 202.3 MB (202283416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0afb371ba889815985e4c238a9fefc5b5d77e26654021e03cb93e295b8e111`  
		Last Modified: Wed, 31 Mar 2021 03:37:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
