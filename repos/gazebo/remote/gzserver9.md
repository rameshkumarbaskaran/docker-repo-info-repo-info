## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:0c577a62e3a221f5d3d0f413468c053c064e3d5819260d2ce8073c56e5fbf2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:894b99452c2de766d55f59d184c8baf934a2895abecf86ec32a6b1db599fe55f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268453212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a277dfdac90e31d2bc014fe0161e19e01b7a81451052053b7202b76e91cdb9b5`
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
# Fri, 09 Dec 2022 01:59:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.19.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:59:21 GMT
EXPOSE 11345
# Fri, 09 Dec 2022 01:59:21 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 09 Dec 2022 01:59:21 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 09 Dec 2022 01:59:21 GMT
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
	-	`sha256:5f1f4be6d647dec99ed891ac2e75cbc0f4a22d5631b72a8f35cb8c3e56471c18`  
		Last Modified: Fri, 09 Dec 2022 02:15:22 GMT  
		Size: 226.2 MB (226204554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f3cfb9d5548d8e9b751df5636d620c09217a1a388d6b3e4f046b747e8656db`  
		Last Modified: Fri, 09 Dec 2022 02:14:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
