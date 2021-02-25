## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:f8aa3bcee0d52f8101d2179ed61d34141d263bf2320ceef88ff77e986025a791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:0dcaa21539f6a679eeec2235ef295bf52dc618802a2b86c2bd8f54fb0f918a66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24606031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a53b1b425aa4bbaea25bf86763df668237f6261464995a72d1f413b6b8b23ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 03:23:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 25 Feb 2021 03:23:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 25 Feb 2021 03:23:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 25 Feb 2021 03:23:56 GMT
EXPOSE 80
# Thu, 25 Feb 2021 03:23:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 03:23:57 GMT
CMD ["traefik"]
# Thu, 25 Feb 2021 03:23:57 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7caf618c71a94b64d99880ac96da93c76a3931b35dffe57842d5baa964afbb3`  
		Last Modified: Thu, 25 Feb 2021 03:24:54 GMT  
		Size: 674.1 KB (674094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86caf1517f080a3c9e8645f69c08191a124a38c59e3c657ecee9dd847a1dcc3`  
		Last Modified: Thu, 25 Feb 2021 03:25:16 GMT  
		Size: 21.1 MB (21116257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dabb83fefe1e371ad0ad76ea6523ffd2a4e4884a2a88f7e7254bc52dca0000`  
		Last Modified: Thu, 25 Feb 2021 03:25:10 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f3ab2c547fbc76d59301ed2f0464b796b57b4f5373ab9dfef877a1bc58464bbd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23066669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ff9159190f81182f781e4191b0558c229fb328121a58e6e9254409ddf3fae4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 24 Feb 2021 23:33:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 24 Feb 2021 23:33:53 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 24 Feb 2021 23:33:54 GMT
EXPOSE 80
# Wed, 24 Feb 2021 23:33:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:33:57 GMT
CMD ["traefik"]
# Wed, 24 Feb 2021 23:33:59 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95c78170691d118707d7ee1e0fde756aca169be42fe54416c614386b5d73e82`  
		Last Modified: Wed, 24 Feb 2021 23:35:10 GMT  
		Size: 677.0 KB (677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7f44cfea47b86361203a25aa879b8217da817bae7fd6dded70220a2fdf0ad7`  
		Last Modified: Wed, 24 Feb 2021 23:35:57 GMT  
		Size: 19.8 MB (19768227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ae25bca5f8bb1dbf5672bf0cea027f288f0b2a7f7fd9df3f07c5e2bfb5e2bb`  
		Last Modified: Wed, 24 Feb 2021 23:35:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7b6485e1c472dbbe4929740278ebd3a6102f89e5208ad98094f13d366cd7759c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22887723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e433192bfcd73af95a95a11e410a94b1e7792f903ed5b5f89bffd264c1dce2e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 04:18:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 25 Feb 2021 04:18:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 25 Feb 2021 04:18:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 25 Feb 2021 04:18:47 GMT
EXPOSE 80
# Thu, 25 Feb 2021 04:18:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Feb 2021 04:18:48 GMT
CMD ["traefik"]
# Thu, 25 Feb 2021 04:18:48 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4961a79823a93d7b581d0d755b544c7ad8e44d35dec7296a3663c7815c9b8e5`  
		Last Modified: Thu, 25 Feb 2021 04:24:33 GMT  
		Size: 675.5 KB (675506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef006d431cee79db31d7d17cf98839851ea3b97f23cff779428c0d801f2e0669`  
		Last Modified: Thu, 25 Feb 2021 04:24:57 GMT  
		Size: 19.5 MB (19486033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a229f0ffeea6995923cfa28b4aa3137adb96ed94f63f8e7fd861c35b76785e2c`  
		Last Modified: Thu, 25 Feb 2021 04:24:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
