## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:dc2ec6ad1afe11bf60b3ea8a9aa35ff48089d4a7eb72268ec868eea5f8298772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:f61260f9d1bbc72aefb3710f5b8ead778ac64c2bd39cbbdf615ca4be66d5e72e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268421154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5f47a011a580f3b3b5ab86ea6d9fb01b28382c082fc9df7f18ecdecfe39e45`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:55:10 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:05:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:05:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 07 Jan 2022 05:05:13 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 07 Jan 2022 05:08:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:08:18 GMT
EXPOSE 11345
# Fri, 07 Jan 2022 05:08:18 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 07 Jan 2022 05:08:18 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 07 Jan 2022 05:08:18 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf856ad4adc3f793ce064ea3fda7e4706e6e0d4b80ca4fe027d96f13a87dab`  
		Last Modified: Fri, 07 Jan 2022 04:32:02 GMT  
		Size: 839.5 KB (839500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e39ad1cd95a6a9236e02bc7188b3acac78be1475ea13458896d01b3296ef056`  
		Last Modified: Fri, 07 Jan 2022 05:23:12 GMT  
		Size: 14.7 MB (14703672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a6fe6051f98d6e615884b5d822331b7502cde48a872ca80b2cc9d91111252b`  
		Last Modified: Fri, 07 Jan 2022 05:23:09 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d38dbdf3b3c21808795be688481ccf72f34a05a1986b77ca056e180ff79e27`  
		Last Modified: Fri, 07 Jan 2022 05:23:09 GMT  
		Size: 5.5 KB (5464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cf6a0dc06c32c424c737618b1ef596c719ad240b321cd0011e730427ae88c`  
		Last Modified: Fri, 07 Jan 2022 05:23:35 GMT  
		Size: 226.2 MB (226165862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8176503f278a106332481b8007f0889182f2d1c35d51137b2a361f53a93c151`  
		Last Modified: Fri, 07 Jan 2022 05:23:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
