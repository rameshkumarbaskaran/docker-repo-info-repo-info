## `emqx:latest`

```console
$ docker pull emqx@sha256:bcf465c3a3f26bc26cb07b69451e89cd8375b6e523e110a582e649bd5e4da27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:c6f6640ab4ef210e43b87483740e7cb386854e4d5dabb905a00be8597fc0ab24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102391616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297dd3881e69eb7c2e218822233e640774df0d55fe0c9a42d20b079f8e8f7e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 07 Sep 2023 03:15:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 07 Sep 2023 03:15:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 07 Sep 2023 03:15:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:16:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 07 Sep 2023 03:16:03 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:16:03 GMT
USER emqx
# Thu, 07 Sep 2023 03:16:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:16:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:16:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:16:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:16:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d5112089b35d1268c6082d34a44ab9ce581e764d1194577d1f2452ab7978e7`  
		Last Modified: Thu, 07 Sep 2023 03:16:38 GMT  
		Size: 68.0 MB (67981258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c681ce97de0d2ada383664f034724f6e3b356fe796fd04554daf3adce4595c`  
		Last Modified: Thu, 07 Sep 2023 03:16:31 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3e2d6b1ec160923fc9a643c76529f05a2d0036edbdbe33bfb8522aa7e0ab3f4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92695550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c72fc2e6dc9c490372142a99bb0ff0b84daeb9509a94b11c63cd3f8890a667`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:43:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:43:30 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 20 Sep 2023 09:43:41 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 20 Sep 2023 09:43:41 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 20 Sep 2023 09:43:41 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 20 Sep 2023 09:43:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 20 Sep 2023 09:43:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 20 Sep 2023 09:43:50 GMT
WORKDIR /opt/emqx
# Wed, 20 Sep 2023 09:43:50 GMT
USER emqx
# Wed, 20 Sep 2023 09:43:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 20 Sep 2023 09:43:50 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 20 Sep 2023 09:43:50 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 20 Sep 2023 09:43:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 09:43:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad6c853d0601d84f2b531042ce064d5fb3f9aa39d30e074f5673152558f8af7`  
		Last Modified: Wed, 20 Sep 2023 09:43:59 GMT  
		Size: 3.0 MB (3002964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aaa8c587ac603c1fab64204d2a4a4d5d4d9a88f0c1da2c73f487e0605c293b`  
		Last Modified: Wed, 20 Sep 2023 09:43:59 GMT  
		Size: 4.1 KB (4118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede3251ec3661ce2a030991bb4e9aeb51a3127ded8c26fb4ea678800451aa92b`  
		Last Modified: Wed, 20 Sep 2023 09:44:19 GMT  
		Size: 59.6 MB (59624697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7857c3d170ee9aa40624dde89b5a3328f7604a266360b10b52103708404916c6`  
		Last Modified: Wed, 20 Sep 2023 09:44:13 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
