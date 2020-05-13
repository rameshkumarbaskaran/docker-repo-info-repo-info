## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:8064896ecb59611c75ba2e56fbf58ee1be7c626f09592d7592dd2363cbf4f114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:a819a655ed409cc72af24b783f54ab867117e2b56bd19e17716106707fae7e09
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.0 MB (650964614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f98570e46ce583b66b9855771f30d06c41ac9e1ef8c7a189bd1a476c1e965c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 13 May 2020 21:23:35 GMT
ADD file:82e0eb87c6ff97b66f86c9fee44884c4cf1b08f5721f36878fc7a15a125b5079 in / 
# Wed, 13 May 2020 21:23:35 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:57:35 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:57:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Wed, 13 May 2020 22:57:41 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 13 May 2020 22:59:16 GMT
RUN apt-get update && apt-get install -q -y     gazebo9=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:59:17 GMT
EXPOSE 11345
# Wed, 13 May 2020 22:59:18 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 13 May 2020 22:59:18 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 13 May 2020 22:59:19 GMT
CMD ["gzserver"]
# Wed, 13 May 2020 23:01:19 GMT
RUN apt-get update && apt-get install -q -y     libgazebo9-dev=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6ce7b04634a37b5c20274b3cc1469490cb28f734448d2c84d01454465418e1f`  
		Last Modified: Wed, 13 May 2020 21:29:57 GMT  
		Size: 45.4 MB (45375936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd6e0de393cd7e52810770a6548f8be29255adc03d76db87d4b07224c16ca44`  
		Last Modified: Wed, 13 May 2020 23:02:23 GMT  
		Size: 21.1 MB (21094962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18cd9b10c2660083b95bde5e4b5a6859cf215d229e6a435cf3f2709311696e7`  
		Last Modified: Wed, 13 May 2020 23:02:15 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040a402e42e0fdeed81bb2b23a1f9469687f21496a4ba1c8f7055558eb02eea2`  
		Last Modified: Wed, 13 May 2020 23:02:15 GMT  
		Size: 5.0 KB (4980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39191b463c30897f095864e45d1ef2eaa9283f9299ff5d1a1997255df0967081`  
		Last Modified: Wed, 13 May 2020 23:03:11 GMT  
		Size: 279.9 MB (279871568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc70d0cf82b8076009229b1a5bcec2aadcb142ae65f9cece13a227876e9d5c6`  
		Last Modified: Wed, 13 May 2020 23:02:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd223394b49e784925c167f56fded0be4fd6da0b528e58fecc2011d630bcd867`  
		Last Modified: Wed, 13 May 2020 23:04:10 GMT  
		Size: 304.6 MB (304615562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
