## `traefik:latest`

```console
$ docker pull traefik@sha256:f7ad75c5386afe73c209b8260a345aaa86a2eb44f0d34881ba34b04ccab74af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:46b47eada57155d07ae3ed78ec3cf6b13d89cdef3476423a79575920d93966b0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35643559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9c4decb28b2cd5eca7f7d89d1c47cd7f858b59871d2b8c7fb8940fa717a97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:00:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 11 Nov 2022 11:00:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 11 Nov 2022 11:00:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 11 Nov 2022 11:00:41 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:00:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Nov 2022 11:00:41 GMT
CMD ["traefik"]
# Fri, 11 Nov 2022 11:00:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249449b90f641a1b63eb9b2d4acd49b56306ca96cff71672364a6b3f00c4987f`  
		Last Modified: Fri, 11 Nov 2022 11:01:22 GMT  
		Size: 663.1 KB (663136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5111fc37be5708458e05759cf8596109a32407c29344acd771bcbe06fc0fd1`  
		Last Modified: Fri, 11 Nov 2022 11:01:25 GMT  
		Size: 32.3 MB (32261615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3f610da225e22ce0082237728f5181abb40a4c45562edd1449ea17613a345`  
		Last Modified: Fri, 11 Nov 2022 11:01:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cdf710f5b7ee39c5124c50c753228dc9b8b1c1c0a1a38f1413487548565445c3`  
		Last Modified: Tue, 09 Aug 2022 17:42:56 GMT  
		Size: 2.6 MB (2606087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1ec6f28225d3ff13bc2defe049a19ceecab6d949a0e69884c44e7e28279b`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 677.5 KB (677512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
