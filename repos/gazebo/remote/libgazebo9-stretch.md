## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:baeb2eb65468f08feb9b8f61aade4941a4fe9a9d0769cb383ebbe1139ce35e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:a13fbf037e70b309400386e3c6c37c0d5824a5239b1c2a67004a221a7c7e17d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.0 MB (650963090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9302d6d61c0961120df68d546908cf6377b1ab3857df3af4acfe9ec4b069c1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 15 May 2020 06:33:25 GMT
ADD file:13031623172f5c5857e27de93553adedf17d955fa370882f850bb6ed6fb8cee7 in / 
# Fri, 15 May 2020 06:33:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:04:46 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 18:04:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 15 May 2020 18:04:51 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 15 May 2020 18:06:03 GMT
RUN apt-get update && apt-get install -q -y     gazebo9=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 18:06:03 GMT
EXPOSE 11345
# Fri, 15 May 2020 18:06:03 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 15 May 2020 18:06:04 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 15 May 2020 18:06:04 GMT
CMD ["gzserver"]
# Fri, 15 May 2020 18:07:42 GMT
RUN apt-get update && apt-get install -q -y     libgazebo9-dev=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c6172af85ee14a8db5a3a51d406b768dfa94d196c06d0d06d591507cf8199f0`  
		Last Modified: Fri, 15 May 2020 06:40:31 GMT  
		Size: 45.4 MB (45375207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f684dbb5f629f5ce0b56765cd7161ce2645c141401afa653f5c2d426ba326d18`  
		Last Modified: Fri, 15 May 2020 18:08:20 GMT  
		Size: 21.1 MB (21095295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b38d56feb50c06103aa9e19f6a4427d12c89e509ba0a2fe33b9bea02b873e80`  
		Last Modified: Fri, 15 May 2020 18:08:16 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cd9fbf9cedd0747ace71037a3a562bcab93cc96b8e1a7578046cc6ea86dd3d`  
		Last Modified: Fri, 15 May 2020 18:08:16 GMT  
		Size: 5.0 KB (4981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23116030240f77ab8e381511617bdd649aa1c9d58061dddaacca0abee71bdbb4`  
		Last Modified: Fri, 15 May 2020 18:09:28 GMT  
		Size: 279.9 MB (279870488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78b0fa6b2248502bd1e0b14ade6d05d55e4a703faa2d762d180c42e6697fa1e`  
		Last Modified: Fri, 15 May 2020 18:08:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce2151a721950578bd0b1340e0f494e3c26ac116cc4d85f96a6bd3cde5b3e20`  
		Last Modified: Fri, 15 May 2020 18:10:22 GMT  
		Size: 304.6 MB (304615509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
