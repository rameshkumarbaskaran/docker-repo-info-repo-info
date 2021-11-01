## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:6d0b0378a2d6c7c5fb0b31323fe0938dc43d4ff424f757f07c195c83056064c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:021210e95f415dcad1e37af2be9b4a00ba0ebd2a5ed62c845b661aa6270439c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277488453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6cd3b9f0487cde0a019d32b5ec17a0127e98baf0caceacf78dad4894df78b2`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 04:52:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:53:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:53:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 01 Oct 2021 04:53:10 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 01 Nov 2021 22:49:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.9.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Nov 2021 22:49:27 GMT
EXPOSE 11345
# Mon, 01 Nov 2021 22:49:27 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 01 Nov 2021 22:49:28 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 01 Nov 2021 22:49:28 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be57c60580131e55159e03672358dbc415078de9b8d6b73691837b848489424`  
		Last Modified: Fri, 01 Oct 2021 05:12:47 GMT  
		Size: 840.7 KB (840739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385846ca0d15120a037d2cc3a853015e25edde30cd5be1a40ef2fb7d9f8c2a11`  
		Last Modified: Fri, 01 Oct 2021 05:12:47 GMT  
		Size: 14.7 MB (14703032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd8248f6f5fe1f59e4c79a671cb199bc9da0529b1e7c7549dc978c92eb93d81`  
		Last Modified: Fri, 01 Oct 2021 05:12:44 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ff515e08b456436e1bc3aec3fc5de6c8300bdc9ed65a4c3dbf8cc01b1e0ad7`  
		Last Modified: Fri, 01 Oct 2021 05:12:44 GMT  
		Size: 5.5 KB (5454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91276f17c794b6b9be7736072f91f695180dd165cb4fd3ab6998d3782ed2521e`  
		Last Modified: Mon, 01 Nov 2021 23:04:39 GMT  
		Size: 235.2 MB (235232526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ca01fc45b5d4325a3ecd0480af14d5210274a7be99fde5007e05d984bdec53`  
		Last Modified: Mon, 01 Nov 2021 23:04:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
