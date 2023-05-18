## `docker:23-dind`

```console
$ docker pull docker@sha256:ba302fcfe4734861299f6befec70bf91146fca26ddb1d44c26c4fd0ec906b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:23-dind` - linux; amd64

```console
$ docker pull docker@sha256:976f1ab98876b9777f3e4101ef02146f6dd2b352177cf970fc3b1273df9db334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112753112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e29d28bfdcffa8889bae6bc1fbaa8b33b8b6206f110dbac0b52fb9a407a51d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 May 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 May 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 May 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:04:13 GMT
CMD ["sh"]
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 May 2023 23:04:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:04:13 GMT
VOLUME [/var/lib/docker]
# Wed, 17 May 2023 23:04:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 May 2023 23:04:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 May 2023 23:04:13 GMT
CMD []
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
	-	`sha256:1cd4867cc7bf586ebd914414a5e00dda99b3e26394f16e97a61f2c3fae0510b7`  
		Last Modified: Thu, 11 May 2023 19:24:57 GMT  
		Size: 16.3 MB (16250881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d94ad0c817fb4f64af0ec231ffd173b474d706777160f7af0ebbfcbc8f1aac`  
		Last Modified: Thu, 11 May 2023 19:24:56 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168469b15989d96502f451470fcee881059efd74c4a56deb5a0db224e4dc470`  
		Last Modified: Thu, 18 May 2023 19:21:58 GMT  
		Size: 16.4 MB (16398965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cb83f6ee6cb66052247715b3c422b5af83d6f819bc9cf9ed44ea635d82bfc2`  
		Last Modified: Thu, 18 May 2023 19:21:55 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a4a9eed77778cb38c6934f128c2fd6dc4a295b607bf73987d0b47809eba16`  
		Last Modified: Thu, 18 May 2023 19:21:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ce391d6cc95f0b338a8757cddcffff10eee3fb0bd9ca5364926f13b06fc2b8`  
		Last Modified: Thu, 18 May 2023 19:21:56 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847a9ae7596e4c24b564330aa9a6baea68509bc7ebad4144f373e93d25b7a795`  
		Last Modified: Thu, 18 May 2023 19:22:12 GMT  
		Size: 7.0 MB (7025225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180b978753cd6df17aff59313045389a25e18ada327095bdfd60db5ad1272f7`  
		Last Modified: Thu, 18 May 2023 19:22:10 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6558439d440fd05fbaa68019468a24ef7589a70b9a87dcf999f1033ffbb5338`  
		Last Modified: Thu, 18 May 2023 19:22:18 GMT  
		Size: 51.7 MB (51657444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c0176829469343685212f6aad9af336ac2f85d30f56be1f0035ec3f314838`  
		Last Modified: Thu, 18 May 2023 19:22:10 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc958352a1c6b664cf7d12b4b18229f3ab5fa158446417a89387948a74f9128f`  
		Last Modified: Thu, 18 May 2023 19:22:10 GMT  
		Size: 2.8 KB (2794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:23-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:07dd542cf60bad6fe67a557b5523192ffc0b47361b9281b97eb737c3af4613be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104300691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a004f9218065b4e7e03a9ce07f1a544e596348faa51f7bde79f2896a8cda9e01`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Wed, 17 May 2023 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 17 May 2023 23:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_VERSION=23.0.6
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 May 2023 23:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 May 2023 23:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 May 2023 23:04:13 GMT
CMD ["sh"]
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-23.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-23.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-23.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-23.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 May 2023 23:04:13 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Wed, 17 May 2023 23:04:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 May 2023 23:04:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 May 2023 23:04:13 GMT
VOLUME [/var/lib/docker]
# Wed, 17 May 2023 23:04:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 May 2023 23:04:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 May 2023 23:04:13 GMT
CMD []
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
	-	`sha256:7755db036d15ac84998f2eac830ac44d7e439c03ecb38bd242508a0481efc0fc`  
		Last Modified: Thu, 11 May 2023 19:43:32 GMT  
		Size: 15.3 MB (15325101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f85b23db6b3d2bdbfb74d5012a03f03cb9ef9ff1e86bc625be7fd7367750a`  
		Last Modified: Thu, 11 May 2023 19:43:31 GMT  
		Size: 14.4 MB (14441512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9d48c32241b614c5848b869b6bfeacb30e6aebdda7d904bdc582d3e2ff429e`  
		Last Modified: Thu, 18 May 2023 19:41:39 GMT  
		Size: 14.9 MB (14861198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86f53d408c55b41eb343e81550022402775fd32b5bf607074efc56276d1ab87`  
		Last Modified: Thu, 18 May 2023 19:41:37 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f0ceb7eb6cdd1f7d46c43bd4cc2ac0ba4d7708d4c4c56981cee5f34d56cba`  
		Last Modified: Thu, 18 May 2023 19:41:37 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9183c9657b82c5064d034ac040bd12e3051caa2c68780603f9e87b3ed0696b9`  
		Last Modified: Thu, 18 May 2023 19:41:37 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c028e3aec1f8c92459e3c8d77f1c7e8ec0e006d7b7b4a591d4df5f466c818d`  
		Last Modified: Thu, 18 May 2023 19:41:51 GMT  
		Size: 7.2 MB (7245100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adb6c201184692e37b5bdc96a1fffad2e8f38ca6c37d23a25bb2bf34ff96aac`  
		Last Modified: Thu, 18 May 2023 19:41:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac540473072b68bd2beba37da390c4a3a71cc66b0e7a943b4cb4c52643d37f8`  
		Last Modified: Thu, 18 May 2023 19:41:55 GMT  
		Size: 47.1 MB (47053390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba8d2bf54e3c4d3eba778d4923af65875f91cdb92f2efb108172c15c8a088c7`  
		Last Modified: Thu, 18 May 2023 19:41:50 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d26837cbeb8df4573e808fd378731f4c69c12edd0e0c1ec2e2080e699a333ec`  
		Last Modified: Thu, 18 May 2023 19:41:50 GMT  
		Size: 2.8 KB (2795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
