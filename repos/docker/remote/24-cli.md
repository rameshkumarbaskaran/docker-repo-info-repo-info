## `docker:24-cli`

```console
$ docker pull docker@sha256:d26b8d3d5ce9b37c6f00a79da81098a9dee5ed1e0265199a408a15557bde5e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-cli` - linux; amd64

```console
$ docker pull docker@sha256:05c2df45a161e6b2da176f067af85f1599aa984b5fe76cdc85e37be62e3c4de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54190273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7244e446861082a4f58d472ff62c93e9bd87a260a3e84ee346043caadb6d53d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:05:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 May 2023 23:05:37 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_VERSION=24.0.0
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 May 2023 23:05:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 May 2023 23:05:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:05:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f03c789ea9a32e8735d4de3ee5a8815764b54fc67b009d5f605e73c75b1201`  
		Last Modified: Wed, 17 May 2023 00:45:57 GMT  
		Size: 16.4 MB (16375868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665194951830ca18f0f0d8a5c718ad69e32422c26ec6fe90a4d20eafd5c220ca`  
		Last Modified: Wed, 17 May 2023 00:45:56 GMT  
		Size: 16.0 MB (16001754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb88c12231d442fb0a0705a289c649708bd22dda99529f9538f69d2b059cfe`  
		Last Modified: Thu, 18 May 2023 19:20:37 GMT  
		Size: 16.4 MB (16398971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f079d166ba0d16ce78a57a051a894eee338b60101435a795660de69289c952`  
		Last Modified: Thu, 18 May 2023 19:20:31 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decdf5128eca562b3ebbd6cd2dd521a5510d87c0fce525eead4f51b0d10a12d9`  
		Last Modified: Thu, 18 May 2023 19:20:31 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda4c10956c394ef9e8ab0eb92dee2b88feac48fdcca15b5e8ee0edaab600b55`  
		Last Modified: Thu, 18 May 2023 19:20:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:367e8f8ea016dc502df3da70c3b1d68a3c5cad9b70c1d049c1bb52bc3116008d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50094472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12089beb4818dbbb500049df880c61d868df65ae7de52c4a3362920b847c0387`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:05:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 May 2023 23:05:37 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_VERSION=24.0.0
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 May 2023 23:05:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 May 2023 23:05:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:05:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a803316fb129ab772964c94e9e7e7736e81a0ad9f233ae92b462ade7ac585b55`  
		Last Modified: Wed, 17 May 2023 00:03:53 GMT  
		Size: 15.4 MB (15422540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afab67718187f66bed185c88b7259f9a99d1d17b4ddd0e1c1c6f63eeb9ffc8`  
		Last Modified: Wed, 17 May 2023 00:03:51 GMT  
		Size: 14.4 MB (14441524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c3899a01170bda38d2a6aaa638fbde1a4d3617b202ec3fa1bfd21894353c01`  
		Last Modified: Thu, 18 May 2023 19:40:23 GMT  
		Size: 14.9 MB (14861194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b05dead2e6489600d4335e4d40854d84d4a7ed14762d0a7b62566c897dbfff`  
		Last Modified: Thu, 18 May 2023 19:40:21 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4e07c5c8338327936f9de4703987ce66a112a3976c70c0b6de558adeee2993`  
		Last Modified: Thu, 18 May 2023 19:40:21 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5e4b947289d40342c1b63f15d3f36d5a3370d63e7c3ce526638ce280a1f7b`  
		Last Modified: Thu, 18 May 2023 19:40:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
