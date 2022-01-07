## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:693c80f8f8058334870a0e54a9b0d754a7f14f258e1f50833d13b80b4791958b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:9f33d41654dc357375a94955d70a6a7c2052639334ce69ded44e09d6e344e34f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605607699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79aba037f5ce6b6eeb70327ffdb3d62ca1138fb1643b7c4ac1c4367bc0a2e4a1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:09:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:15:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:15:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 07 Jan 2022 05:15:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 07 Jan 2022 05:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.9.1-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 05:17:56 GMT
EXPOSE 11345
# Fri, 07 Jan 2022 05:17:56 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 07 Jan 2022 05:17:56 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 07 Jan 2022 05:17:57 GMT
CMD ["gzserver"]
# Fri, 07 Jan 2022 05:22:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.9.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d6b806a5eae974734f3df21a5799c46db4c8dc12ffc6bab4a8ca2f802d1b5`  
		Last Modified: Fri, 07 Jan 2022 04:34:49 GMT  
		Size: 1.2 MB (1182238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c0bba77aa7d24282d153e2a02032e5484ee8a5ca1879eb9ff0e473a7f3ff7c`  
		Last Modified: Fri, 07 Jan 2022 05:25:43 GMT  
		Size: 16.2 MB (16169890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fadef1dc985611b2e7adc1e486b110f8d89368e6e69b7393a4f7581b354ef6`  
		Last Modified: Fri, 07 Jan 2022 05:25:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae5a366fc56bde9f5c014cd333b5cd60218fddd6d1d1f03bb707df6c5acb7f`  
		Last Modified: Fri, 07 Jan 2022 05:25:41 GMT  
		Size: 5.5 KB (5502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e6d00f35c5d4f64a6fc38d5b86853b8f26cb52738de296057404122e6936bc`  
		Last Modified: Fri, 07 Jan 2022 05:26:13 GMT  
		Size: 275.0 MB (275014164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7862e44a45abdb1b277b25cfdda380a11e65729fd3fe63bf5dd1ea5a11a748`  
		Last Modified: Fri, 07 Jan 2022 05:25:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0740bffba65fefe86313957b7ae1b671d8ddeb163f542f77f78b9ab372ef6a63`  
		Last Modified: Fri, 07 Jan 2022 05:27:11 GMT  
		Size: 284.7 MB (284667852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
