## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:99e4e303f52f992e48d4a8215b0cbd02d6268becb51ce308b2862f886f99eae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:e1f098bda96f9be58d669f218ab762d98ffbd332a4e03bbd5c55f8a97443b02f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25647623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90633955b99f30af3762137bd90ee3f45bff7c7229cc5d37e2f6147faae42d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:35:19 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 20 Jul 2022 03:35:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 20 Jul 2022 03:35:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 20 Jul 2022 03:35:23 GMT
EXPOSE 80
# Wed, 20 Jul 2022 03:35:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 03:35:24 GMT
CMD ["traefik"]
# Wed, 20 Jul 2022 03:35:24 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7159927569cf09b404d7e14851c4c19f4a6fdeb2c0606583f55fd742020da10b`  
		Last Modified: Wed, 20 Jul 2022 03:36:14 GMT  
		Size: 666.7 KB (666680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5375964b35aff2edd1db31d3d719d017b8dacbfc9791a03b1cf724147cae171f`  
		Last Modified: Wed, 20 Jul 2022 03:36:18 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a237afab9f6966bc048222d3062d43672bd3c44fb8d6abbc0763a5f5269a32`  
		Last Modified: Wed, 20 Jul 2022 03:36:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:837130323599fa8f99627f91ab37b5bf9bb1bf784808668efd56c1e326df5167
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23922970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeba8ad6631f1c772caa4da654b0f1df85c44021bb05a54462bd068f60f5880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 19 Jul 2022 22:50:02 GMT
ADD file:5a22b2130f6fbe534730df1f47715641a45e55845be7f35c3183e2b74ec43397 in / 
# Tue, 19 Jul 2022 22:50:03 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:49:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 20 Jul 2022 06:49:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 20 Jul 2022 06:49:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 20 Jul 2022 06:49:41 GMT
EXPOSE 80
# Wed, 20 Jul 2022 06:49:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 06:49:41 GMT
CMD ["traefik"]
# Wed, 20 Jul 2022 06:49:42 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dc1cbfb63ac7071e143ce96f0f140dc30282039f8d0770eaa7ab97eba515639`  
		Last Modified: Tue, 19 Jul 2022 22:51:41 GMT  
		Size: 2.6 MB (2626632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9f45eadef186a799e85d948ea9258246a9ae95d563e5c0067166d1fefa0fcc`  
		Last Modified: Wed, 20 Jul 2022 06:52:06 GMT  
		Size: 672.5 KB (672538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96062d011005096435bb76fedfb5c41ba2741d4b6cdd51e8b9dbe02e4dbf3141`  
		Last Modified: Wed, 20 Jul 2022 06:52:19 GMT  
		Size: 20.6 MB (20623431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c572fc2c74bdeec8ec036310eb2a96c8fa03098e1b3a62bf068e7aef725f14`  
		Last Modified: Wed, 20 Jul 2022 06:52:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ebae6d48b459b3990d32899b0fbeadf111bb480e49877f448ecbf362933e4004
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23517764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdcb44c6a57458adc68a2789d539c39ce250a18d01e117a59d1c464dcc9c01c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:51 GMT
ADD file:bb30934245445dabbe698387b5d454c2360d05055f7ab1bcaaffefea5aefb539 in / 
# Tue, 19 Jul 2022 22:39:51 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 05:51:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 20 Jul 2022 05:51:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 20 Jul 2022 05:51:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 20 Jul 2022 05:51:33 GMT
EXPOSE 80
# Wed, 20 Jul 2022 05:51:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Jul 2022 05:51:35 GMT
CMD ["traefik"]
# Wed, 20 Jul 2022 05:51:36 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4bf3852c6ccaad2dedd57347d310f084247a2e202c2fc20f5fa88d921e8510e`  
		Last Modified: Tue, 19 Jul 2022 22:40:44 GMT  
		Size: 2.7 MB (2717747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5079d318fad3c7be381c97f94f105a4babfae18c70c36eb1acfe84f135b5ae30`  
		Last Modified: Wed, 20 Jul 2022 05:52:49 GMT  
		Size: 668.3 KB (668285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa33afa4e3af817b4216ea216e13b5b9c9e80a2c17f1ae919bb25c3d454930e3`  
		Last Modified: Wed, 20 Jul 2022 05:52:52 GMT  
		Size: 20.1 MB (20131363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6655cd6b23d83f08c07cad8e9a9eefa4e8a182c83edf40516e2dbd0e3a753bd`  
		Last Modified: Wed, 20 Jul 2022 05:52:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
