## `traefik:latest`

```console
$ docker pull traefik@sha256:51be0ada0b77afff110eab4c7cb76a2d362a63beb8f8cab220ac199759538975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b7dd3ca7e9a83ca3f57af46d949fe08fe15a02235e10f48f387e2df12a4e43e9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeb1e5a15f4f0baea5b04444c3361480d221c2d6518eccb0c1673102d793bae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 20:27:15 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 02:07:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 02:07:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 02:07:05 GMT
EXPOSE 80
# Wed, 22 Jan 2020 02:07:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 02:07:08 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 02:07:09 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75226f24cf5fc4e2d56fbb31d8daf122273d120792aff22dee3a970a5419ee9`  
		Last Modified: Mon, 21 Oct 2019 20:28:17 GMT  
		Size: 697.8 KB (697821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9685e4e3c2d176d8cf28f1cc958c628e8b1ab289aedc3eb0c6faffcf9252bb8`  
		Last Modified: Wed, 22 Jan 2020 02:07:42 GMT  
		Size: 18.3 MB (18303633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b81ee3443fca2dc98d09455bcd09190f22f077c9cf56ce84c21369fbabc7c3`  
		Last Modified: Wed, 22 Jan 2020 02:07:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
