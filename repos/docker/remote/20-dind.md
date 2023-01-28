## `docker:20-dind`

```console
$ docker pull docker@sha256:4dc065bd0c29c4eb33f0e9a28480930a8227e353a60bff2610c485f1fe01a89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:5c854de0db802a7922da1a271a969bd43c3c725cb6ea24953b217f3273aa1f2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109765809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e76db19a191647d74efa689b7a05d564f06c68ca108bff31a7d439511f0f02`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 21:12:54 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 09 Jan 2023 21:12:54 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 21 Jan 2023 00:20:06 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 21 Jan 2023 00:20:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 27 Jan 2023 23:24:24 GMT
ENV DOCKER_BUILDX_VERSION=0.10.1
# Fri, 27 Jan 2023 23:24:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-amd64'; 			sha256='31be610820f12fdf5e1c310886e95856e659f647e26965f819bd728dcc94fe18'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v6'; 			sha256='60c0044dca2c82bc336af15c5529262a88ce4509e75ad5730db10bf688820b0e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v7'; 			sha256='2ee39cf64dcf64505f1c7d6213052b8bda39b06e1410c21098d3ca5a3eb72fe7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm64'; 			sha256='1561306348d5ffd63b2fe5e32f3440dd4e8751faf94ffa3103364cb94818f5ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-ppc64le'; 			sha256='1cf2e28fa82064bc05c8a69a2a0b798c7adbe572e53042a4dcd604ae9f0103ad'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-riscv64'; 			sha256='46e2188c265b684f224a3fbdb11a40531057e278a580cd3ca01b2042f48c492b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-s390x'; 			sha256='e4cecfa4c4489385c4cb1ce6f9f518c9afce63705588088c5d32c7c286c9c41a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 27 Jan 2023 23:24:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.1
# Fri, 27 Jan 2023 23:24:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64'; 			sha256='bcfd9ea51dee4c19dccdfaeef0e7956ef68bf14f3d175933742061a7271ef0f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv6'; 			sha256='a8934600100af88f535eb50b45c7d8d2ac37835221803ba2910e0b167b3af22e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv7'; 			sha256='e5b03ac1258ad4243af0ac4afcb1c6cc8c9956b2483a50309cdb38cdb8387e37'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-aarch64'; 			sha256='14d31297794868520cb2e61b543bb1c821aaa484af22b397904314ae8227f6a2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-ppc64le'; 			sha256='bdada874a26d382b20ced7c170707a1ebcf9f20d7d6f394b962076968473ca9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-riscv64'; 			sha256='9cc1b9c8de313a1e43b8f3dcca47c29eeb87af3de24c67448c463bf882166430'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-s390x'; 			sha256='cf311824af115d0bece5d5d60a73464912dad07cdd00fdaa469dabbcad60f289'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 27 Jan 2023 23:24:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 27 Jan 2023 23:24:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:24:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 27 Jan 2023 23:24:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 27 Jan 2023 23:24:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:24:30 GMT
CMD ["sh"]
# Fri, 27 Jan 2023 23:24:36 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 27 Jan 2023 23:24:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 27 Jan 2023 23:24:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 27 Jan 2023 23:24:41 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 27 Jan 2023 23:24:42 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 27 Jan 2023 23:24:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:24:42 GMT
VOLUME [/var/lib/docker]
# Fri, 27 Jan 2023 23:24:42 GMT
EXPOSE 2375 2376
# Fri, 27 Jan 2023 23:24:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 27 Jan 2023 23:24:43 GMT
CMD []
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea237885379427b44e97fa21c0d47eaa42f826dfd0833a69279002a7ce8f50d9`  
		Last Modified: Mon, 09 Jan 2023 21:14:56 GMT  
		Size: 2.1 MB (2064267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a201afc762d4387d79af22a29b3c10cf0087308df49bed7f8a49a23c9cf96923`  
		Last Modified: Sat, 21 Jan 2023 00:22:43 GMT  
		Size: 14.0 MB (13983181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab1e0b18632a29e39502f4def8a577417a23197bf53cc8755d23e736ce5b9eb`  
		Last Modified: Fri, 27 Jan 2023 23:26:54 GMT  
		Size: 16.0 MB (15995426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654619d88cafe21b7b229041667b8a1be7e95f1b37ede533b0f373ea802b1008`  
		Last Modified: Fri, 27 Jan 2023 23:26:53 GMT  
		Size: 14.5 MB (14490896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975894971898f4fcc14fe64c8db855462cc1a95fadeba63fa8c112f95b20cd5`  
		Last Modified: Fri, 27 Jan 2023 23:26:51 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4efa4767f53f48ae61fde8b62de052b200a6e39df00f459b5ab9ad7a9a6685`  
		Last Modified: Fri, 27 Jan 2023 23:26:51 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29acf2f8dfa9bdf940fb32f5c4a0395d4d68d37c782f9f27ddb33c65f955eee6`  
		Last Modified: Fri, 27 Jan 2023 23:26:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd6cde1ecf376a516fc1ed11a13ec7f1e8d534aba4e23f1b0034cc7fc01d6a7`  
		Last Modified: Fri, 27 Jan 2023 23:27:20 GMT  
		Size: 6.8 MB (6837929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515484edefdff2a3646f8e3f33f8f1318bd95bf4afb9a3a49686d278f08798cd`  
		Last Modified: Fri, 27 Jan 2023 23:27:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa29c43eb88d971166a4cdd8b5d221b64d80dc23e8bd3ec1305b63ecde41ae0`  
		Last Modified: Fri, 27 Jan 2023 23:27:27 GMT  
		Size: 53.0 MB (53016659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffd364fdb30f883d3c3ece135f6a5fd19134e89cf8e9df2c0fe682fb92cc89e`  
		Last Modified: Fri, 27 Jan 2023 23:27:19 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539918c8b57af0b1c9db31726e75b0c271e73122380aa53a478ef0e10922a1c9`  
		Last Modified: Fri, 27 Jan 2023 23:27:19 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:937a30d89cf69f75088f21a2f531d3f8fa2f4d3e63012465ab8b601a89540083
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101233972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324044312c91ec06522fb60286edcb62c6b922ee8649fe35e392159616d568a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:29:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 09 Jan 2023 17:29:01 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 21 Jan 2023 00:39:56 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 21 Jan 2023 00:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 27 Jan 2023 23:39:52 GMT
ENV DOCKER_BUILDX_VERSION=0.10.1
# Fri, 27 Jan 2023 23:39:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-amd64'; 			sha256='31be610820f12fdf5e1c310886e95856e659f647e26965f819bd728dcc94fe18'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v6'; 			sha256='60c0044dca2c82bc336af15c5529262a88ce4509e75ad5730db10bf688820b0e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v7'; 			sha256='2ee39cf64dcf64505f1c7d6213052b8bda39b06e1410c21098d3ca5a3eb72fe7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm64'; 			sha256='1561306348d5ffd63b2fe5e32f3440dd4e8751faf94ffa3103364cb94818f5ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-ppc64le'; 			sha256='1cf2e28fa82064bc05c8a69a2a0b798c7adbe572e53042a4dcd604ae9f0103ad'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-riscv64'; 			sha256='46e2188c265b684f224a3fbdb11a40531057e278a580cd3ca01b2042f48c492b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-s390x'; 			sha256='e4cecfa4c4489385c4cb1ce6f9f518c9afce63705588088c5d32c7c286c9c41a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 27 Jan 2023 23:39:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.1
# Fri, 27 Jan 2023 23:39:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64'; 			sha256='bcfd9ea51dee4c19dccdfaeef0e7956ef68bf14f3d175933742061a7271ef0f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv6'; 			sha256='a8934600100af88f535eb50b45c7d8d2ac37835221803ba2910e0b167b3af22e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv7'; 			sha256='e5b03ac1258ad4243af0ac4afcb1c6cc8c9956b2483a50309cdb38cdb8387e37'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-aarch64'; 			sha256='14d31297794868520cb2e61b543bb1c821aaa484af22b397904314ae8227f6a2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-ppc64le'; 			sha256='bdada874a26d382b20ced7c170707a1ebcf9f20d7d6f394b962076968473ca9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-riscv64'; 			sha256='9cc1b9c8de313a1e43b8f3dcca47c29eeb87af3de24c67448c463bf882166430'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-s390x'; 			sha256='cf311824af115d0bece5d5d60a73464912dad07cdd00fdaa469dabbcad60f289'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 27 Jan 2023 23:39:59 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 27 Jan 2023 23:39:59 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:39:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 27 Jan 2023 23:39:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 27 Jan 2023 23:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:39:59 GMT
CMD ["sh"]
# Fri, 27 Jan 2023 23:40:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 27 Jan 2023 23:40:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 27 Jan 2023 23:40:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 27 Jan 2023 23:40:09 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 27 Jan 2023 23:40:10 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 27 Jan 2023 23:40:10 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:40:10 GMT
VOLUME [/var/lib/docker]
# Fri, 27 Jan 2023 23:40:10 GMT
EXPOSE 2375 2376
# Fri, 27 Jan 2023 23:40:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 27 Jan 2023 23:40:10 GMT
CMD []
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e78d5cc3f021297e04408059511c5dff9e32e8d9410a4f7815ccdd7d509eb`  
		Last Modified: Mon, 09 Jan 2023 17:30:59 GMT  
		Size: 2.0 MB (2036908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603170b2f7902394d21011bcf24dd4eb1201cdc6fb46df092f67652550a21b1`  
		Last Modified: Sat, 21 Jan 2023 00:42:26 GMT  
		Size: 12.7 MB (12741960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2006dcd2b17e623f1d3145ca40234b79cf534a3744796d270f06b5990bf5e82d`  
		Last Modified: Fri, 27 Jan 2023 23:42:17 GMT  
		Size: 14.4 MB (14437076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3f9fdde4bcd69c63d830686417da32eb82d99d52a54d0ffa714ef19c4e5650`  
		Last Modified: Fri, 27 Jan 2023 23:42:17 GMT  
		Size: 13.1 MB (13080439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7d3ab4f140209b7b3f451355a4dd765871213afdee65b4afc1d589ca255d77`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4c90b17bef664324198715e94f9dcbf633bc28ad188c2d53dd86c5fd357450`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1603afee115a56d2dfc2b2b73cd4666ea7861ad7341bbecbd61909f9e717d9`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecddf450dd3d79729a48880405853b2820ddab5fa766593483dd865ce8875f93`  
		Last Modified: Fri, 27 Jan 2023 23:42:44 GMT  
		Size: 7.0 MB (6991098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7aa53beaded636cab75ec65279b90642f6900c979994c4eb0a1888539b119`  
		Last Modified: Fri, 27 Jan 2023 23:42:43 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be5ccc3c5a89738e458ae34618bcdef3f44234d32fa815ea7d4a4142ecac896`  
		Last Modified: Fri, 27 Jan 2023 23:42:49 GMT  
		Size: 48.7 MB (48680422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09c915cf565e3e4a4a8bd53dbf3a0ba0405427e9edc229fee8ae3e9cd444c47`  
		Last Modified: Fri, 27 Jan 2023 23:42:43 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6287f6239ece01416c03036bc878a65bd9840179621348e959661406afb39d2`  
		Last Modified: Fri, 27 Jan 2023 23:42:43 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
