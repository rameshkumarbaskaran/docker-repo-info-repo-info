## `docker:24-git`

```console
$ docker pull docker@sha256:6d9d3ff6304cbfb9812d0ed9933dd48df46591c4147f6c5bab9f52a6135401a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:24-git` - linux; amd64

```console
$ docker pull docker@sha256:55e735a3b67768c81a0db521a1627503af7e281e5d028751382b4b532de88d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120304792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0882d577c3b0f82e8f1aee25a081da754aaac4099b96833c1bd627a42fd7c8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 May 2023 23:05:37 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:05:37 GMT
VOLUME [/var/lib/docker]
# Wed, 17 May 2023 23:05:37 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 May 2023 23:05:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 May 2023 23:05:37 GMT
CMD []
# Wed, 17 May 2023 23:05:37 GMT
RUN apk add --no-cache git # buildkit
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
	-	`sha256:a8713c9e17f1bda859deaec5d06c4a350a5cff6f925c08973e87631fb6f44f1a`  
		Last Modified: Thu, 18 May 2023 19:20:52 GMT  
		Size: 7.0 MB (7025225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5041f73272dbecc893b1e455234d4244d5d1978263f4007b880ae18651c6aa6`  
		Last Modified: Thu, 18 May 2023 19:20:51 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30fe88f2a20635e3f757c08c65f81f490706a673c1aca19bb7f7710ecfac986`  
		Last Modified: Thu, 18 May 2023 19:20:59 GMT  
		Size: 54.1 MB (54148004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e82cb361a3e698f01dc72f561aacca39d4c75355ce9cbac1efb4fe35be4050a`  
		Last Modified: Thu, 18 May 2023 19:20:51 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac69f4349859d4be8bdf323e59c67d57d8b1ea71cdab3e50e71db2ed2fe7ff8`  
		Last Modified: Thu, 18 May 2023 19:20:51 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae8ceb57f2897ccad83edcc2ba67ac922bd57fd12e8668993a76651053bed5a`  
		Last Modified: Thu, 18 May 2023 19:21:43 GMT  
		Size: 4.9 MB (4936123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c5399d09733a39da2c17503924482d522b7c8b2b4ff264ea1616b6aeba2e310d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111822073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451d0d089813185d070631d2bbe60dc638569b1ee7b456c836302f4c73e35ce5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

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
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 May 2023 23:05:37 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Wed, 17 May 2023 23:05:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 May 2023 23:05:37 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:05:37 GMT
VOLUME [/var/lib/docker]
# Wed, 17 May 2023 23:05:37 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 May 2023 23:05:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 May 2023 23:05:37 GMT
CMD []
# Wed, 17 May 2023 23:05:37 GMT
RUN apk add --no-cache git # buildkit
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
	-	`sha256:029e87f5c7fbf9a7c6a26c52b64f36b8239898442b39fa4aa52d9362d76b063f`  
		Last Modified: Thu, 18 May 2023 19:40:37 GMT  
		Size: 7.2 MB (7245105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d809f51f3bd977adf1067e75215f01cc3020fcf8b34a4ec52ce19929be89ba6`  
		Last Modified: Thu, 18 May 2023 19:40:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a641fd29ce99b8cd8d23739d8f70c1376d540b4622d00b07cf03f690dad5d9fc`  
		Last Modified: Thu, 18 May 2023 19:40:41 GMT  
		Size: 49.5 MB (49455390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8993dca65d1cb645400600017dd82b24c46f6065157e5b01e8806f76412398`  
		Last Modified: Thu, 18 May 2023 19:40:36 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45deb50ebb752b2c5972acd4b68a6773c64ae4f4074a5c072c288de0fa71a3de`  
		Last Modified: Thu, 18 May 2023 19:40:36 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9867f92b106f8032ea0d37febaa9c11a28b1f2869cbf361a1f62570c1895c29f`  
		Last Modified: Thu, 18 May 2023 19:41:24 GMT  
		Size: 5.0 MB (5021940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
