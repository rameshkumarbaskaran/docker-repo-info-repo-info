## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:4a5339049510afd6806267a48258839f603ede41ec6d426811826f0258bd140c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:05441001611c12a4888ac1ef83ebe6fbba5c7c9ccf7765b862899be4a69f7cd4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346356190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91145a2f12fee2e48e43879e2cb88e8f8f0d36c96bf51529c23427e275979e0`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:41 GMT
ADD file:8a9218592e5d736a05a1821a6dd38b205cdd8197c26a5aa33f6fc22fbfaa1c4d in / 
# Sat, 01 Feb 2020 17:23:41 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:31:04 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:31:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 01 Feb 2020 18:31:10 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 04 Feb 2020 23:33:01 GMT
RUN apt-get update && apt-get install -q -y     gazebo9=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Feb 2020 23:33:01 GMT
EXPOSE 11345
# Tue, 04 Feb 2020 23:33:02 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 04 Feb 2020 23:33:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 04 Feb 2020 23:33:02 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:3192219afd04f93d90f0af7f89cb527d1af2a16975ea391ea8517c602ad6ddb6`  
		Last Modified: Sat, 01 Feb 2020 17:28:49 GMT  
		Size: 45.4 MB (45380658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b329f82d766c69e9f5f8cd45d02345d8712d15f06c0ff372b1e004cf21ca32a3`  
		Last Modified: Tue, 04 Feb 2020 23:43:20 GMT  
		Size: 21.1 MB (21095020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9a30b34d65d7bb558fa6a1bd00c831a4018362f0f7226e9fcdc1e3d54880d9`  
		Last Modified: Tue, 04 Feb 2020 23:43:15 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b248d8d631a3f33400d84c85843d3a06935e6f106c3a937bab4a7ff8cff2ff`  
		Last Modified: Tue, 04 Feb 2020 23:43:15 GMT  
		Size: 5.0 KB (4977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49613c271c71ec656721624c63b3638377811fe6034138679b0e5f1d6d37ddb`  
		Last Modified: Tue, 04 Feb 2020 23:44:39 GMT  
		Size: 279.9 MB (279873927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c83b31a341fc2ed88d67c58482c3b3ca0eee800cd52ec72c123e88009424c7`  
		Last Modified: Tue, 04 Feb 2020 23:43:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
