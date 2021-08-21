## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:d36c0f9025a59263de4e3674422e97168d047ca9163990ce3b1f42adbc216a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:ee78a154c8ab0bb485982d459416f24f90778364f2cae4c79de117b33c2b8ba9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.2 MB (607190630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5621378174a87acabe210f6d3e288a538cee15bb671ada853ff9c5807c409db8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:49:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:49:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Mon, 26 Jul 2021 23:49:33 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 21 Aug 2021 01:32:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.8.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 21 Aug 2021 01:32:41 GMT
EXPOSE 11345
# Sat, 21 Aug 2021 01:32:41 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 21 Aug 2021 01:32:41 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 21 Aug 2021 01:32:41 GMT
CMD ["gzserver"]
# Sat, 21 Aug 2021 01:38:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.8.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52fa7f2bbaf9fdabe2f4f44c9c14e354edb50cbf9d14d543c25068e3bac43f3`  
		Last Modified: Tue, 27 Jul 2021 00:03:13 GMT  
		Size: 16.2 MB (16166865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82b78dfba60e8c933ef391fb029a1696247906bdb721ab7b16f27384a190896`  
		Last Modified: Tue, 27 Jul 2021 00:03:11 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc640b65e76d09c20486b01253367703fec36621d99d69308307a3e4d62531f`  
		Last Modified: Tue, 27 Jul 2021 00:03:10 GMT  
		Size: 5.5 KB (5500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516d184d78c23d92702313ef507846152078de35a0fbf04c896ea667a5d0c7a4`  
		Last Modified: Sat, 21 Aug 2021 01:40:31 GMT  
		Size: 274.9 MB (274928248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1bd582604eedb2f69534435dade79181d8c66a66a89535fbb66250f1b2dc34`  
		Last Modified: Sat, 21 Aug 2021 01:39:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a8f5a90fa8dac7d7cdb22566ed63dbf3cccc059a5373dc71e90b62aaa12692`  
		Last Modified: Sat, 21 Aug 2021 01:41:27 GMT  
		Size: 286.3 MB (286337967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
