## `traefik:rocamadour`

```console
$ docker pull traefik@sha256:146ce13c95c17a579b38e670187aee573172dc2c7fecec1555fbede0005ad72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:rocamadour` - linux; amd64

```console
$ docker pull traefik@sha256:aea2c8e5de38fac4809aa0d29e88499a0ba0b242153750ff7a5925dbfeeeb690
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30199589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5123c1f74c4052ea5a0cbf9eca3658e29c561c1ca2f98b89a3b27db322f332`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 12 Jan 2022 20:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc2/traefik_v2.6.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 12 Jan 2022 20:21:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 12 Jan 2022 20:21:21 GMT
EXPOSE 80
# Wed, 12 Jan 2022 20:21:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Jan 2022 20:21:21 GMT
CMD ["traefik"]
# Wed, 12 Jan 2022 20:21:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a2d2049905f4b50434829ffae40127986fd6c04ad290ffd4da5d1388432b37`  
		Last Modified: Wed, 12 Jan 2022 20:22:00 GMT  
		Size: 26.7 MB (26698416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82d00ba7763921139508297a5692e461f886b850946d57e61a495f464c634e`  
		Last Modified: Wed, 12 Jan 2022 20:21:55 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm variant v6

```console
$ docker pull traefik@sha256:10f9c30bf7950ebbbb2f476062eb0570cf32c12d801cf75303e5cd33039bd854
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28375430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a9f20b9360a20dbba406ece9f0d283521d4467beb17046a192dfd72ac91f5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 12 Jan 2022 19:50:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc2/traefik_v2.6.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 12 Jan 2022 19:50:25 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 12 Jan 2022 19:50:25 GMT
EXPOSE 80
# Wed, 12 Jan 2022 19:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Jan 2022 19:50:26 GMT
CMD ["traefik"]
# Wed, 12 Jan 2022 19:50:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6112e3ff4f28b7cf953a0c66e0213df70b0ce0e5371fa0d839a0ac7feea1c2`  
		Last Modified: Wed, 12 Jan 2022 19:53:14 GMT  
		Size: 25.1 MB (25056698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4430a8f26bf95d223d9d6441932969dfe6f91c54ae4f455e891812075c2761af`  
		Last Modified: Wed, 12 Jan 2022 19:52:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d1962fe48671163636bedddf92fdf81d5c0da16533591b931800715d31516a95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27747702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12aea62ff64b3b203114d0a53776825cc8ded9c9c2ca3b79ca3364dd57e6d51e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 12 Jan 2022 19:40:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc2/traefik_v2.6.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 12 Jan 2022 19:40:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 12 Jan 2022 19:40:49 GMT
EXPOSE 80
# Wed, 12 Jan 2022 19:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Jan 2022 19:40:51 GMT
CMD ["traefik"]
# Wed, 12 Jan 2022 19:40:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6140a82546cc3013c03a1a41dec43b7364bf5702f3ed2a7abdfa83ce12b616`  
		Last Modified: Wed, 12 Jan 2022 19:42:01 GMT  
		Size: 24.3 MB (24349626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e83ade38035c9baedb2657db35393c09770083f4adde5c722d1a26c1982f2c0`  
		Last Modified: Wed, 12 Jan 2022 19:41:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
