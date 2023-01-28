## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:7defd8f850e2ba1c2980b6c0589e2e5ab05687a72d7e0f927a1fe40e50e46073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:df5059968dae8b292a948611c0513891d324570f0b09eb3e5ce22cf9dc1e861c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132188901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9704b91403980e5dbeaa201df36c644185744517b0d904b7ba960f59212d2be3`
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
# Sat, 21 Jan 2023 00:19:32 GMT
ENV DOCKER_VERSION=23.0.0-rc.3
# Sat, 21 Jan 2023 00:19:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 27 Jan 2023 23:23:53 GMT
ENV DOCKER_BUILDX_VERSION=0.10.1
# Fri, 27 Jan 2023 23:23:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-amd64'; 			sha256='31be610820f12fdf5e1c310886e95856e659f647e26965f819bd728dcc94fe18'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v6'; 			sha256='60c0044dca2c82bc336af15c5529262a88ce4509e75ad5730db10bf688820b0e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v7'; 			sha256='2ee39cf64dcf64505f1c7d6213052b8bda39b06e1410c21098d3ca5a3eb72fe7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm64'; 			sha256='1561306348d5ffd63b2fe5e32f3440dd4e8751faf94ffa3103364cb94818f5ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-ppc64le'; 			sha256='1cf2e28fa82064bc05c8a69a2a0b798c7adbe572e53042a4dcd604ae9f0103ad'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-riscv64'; 			sha256='46e2188c265b684f224a3fbdb11a40531057e278a580cd3ca01b2042f48c492b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-s390x'; 			sha256='e4cecfa4c4489385c4cb1ce6f9f518c9afce63705588088c5d32c7c286c9c41a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 27 Jan 2023 23:23:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.1
# Fri, 27 Jan 2023 23:23:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64'; 			sha256='bcfd9ea51dee4c19dccdfaeef0e7956ef68bf14f3d175933742061a7271ef0f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv6'; 			sha256='a8934600100af88f535eb50b45c7d8d2ac37835221803ba2910e0b167b3af22e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv7'; 			sha256='e5b03ac1258ad4243af0ac4afcb1c6cc8c9956b2483a50309cdb38cdb8387e37'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-aarch64'; 			sha256='14d31297794868520cb2e61b543bb1c821aaa484af22b397904314ae8227f6a2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-ppc64le'; 			sha256='bdada874a26d382b20ced7c170707a1ebcf9f20d7d6f394b962076968473ca9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-riscv64'; 			sha256='9cc1b9c8de313a1e43b8f3dcca47c29eeb87af3de24c67448c463bf882166430'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-s390x'; 			sha256='cf311824af115d0bece5d5d60a73464912dad07cdd00fdaa469dabbcad60f289'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 27 Jan 2023 23:23:58 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 27 Jan 2023 23:23:58 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:23:58 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 27 Jan 2023 23:23:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 27 Jan 2023 23:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:23:59 GMT
CMD ["sh"]
# Fri, 27 Jan 2023 23:24:03 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 27 Jan 2023 23:24:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 27 Jan 2023 23:24:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 27 Jan 2023 23:24:08 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 27 Jan 2023 23:24:09 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 27 Jan 2023 23:24:09 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:24:10 GMT
VOLUME [/var/lib/docker]
# Fri, 27 Jan 2023 23:24:10 GMT
EXPOSE 2375 2376
# Fri, 27 Jan 2023 23:24:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 27 Jan 2023 23:24:10 GMT
CMD []
# Fri, 27 Jan 2023 23:24:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 27 Jan 2023 23:24:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 27 Jan 2023 23:24:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 27 Jan 2023 23:24:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-23.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-23.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 27 Jan 2023 23:24:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 27 Jan 2023 23:24:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 27 Jan 2023 23:24:18 GMT
USER rootless
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
	-	`sha256:548520107574b7ff7bae27177341f82ff58fd0889ef71c3b9e6bcd06ab291eaa`  
		Last Modified: Sat, 21 Jan 2023 00:21:26 GMT  
		Size: 16.2 MB (16211018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b41c75025d60403860519a94f59d8079557eb055f29df9adea4fffdbca666f`  
		Last Modified: Fri, 27 Jan 2023 23:25:41 GMT  
		Size: 16.0 MB (15995426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf47aef24c2a5602d4d9cb942f1493784e6428867d6eea3f4735ff0153d1ac4`  
		Last Modified: Fri, 27 Jan 2023 23:25:41 GMT  
		Size: 14.5 MB (14490896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b868471ae97893ab27a281f0d2a70ed97fb6d3d5eb77f17952ae9c5f9a9b3f83`  
		Last Modified: Fri, 27 Jan 2023 23:25:38 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb99ae8c306fb128d711a56b2d66c82213739826956bc0d58512f4fabee9b29`  
		Last Modified: Fri, 27 Jan 2023 23:25:38 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed54d1cb949573e21632cc761e17647bb68abe6dd2e18dab83f511b8b75dc0c`  
		Last Modified: Fri, 27 Jan 2023 23:25:38 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e41f5500b3eeaaec870c90fece70dfae624391a5e7520115003d3ae376fc41`  
		Last Modified: Fri, 27 Jan 2023 23:25:54 GMT  
		Size: 6.8 MB (6837913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6027e9d75cac757dc434581d8685a169774407a031ace8ba765266cd6156b646`  
		Last Modified: Fri, 27 Jan 2023 23:25:53 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284d152d414b7c7081e455a26177133a5518528b75a63e8ea8d41d21d1b8bda9`  
		Last Modified: Fri, 27 Jan 2023 23:26:01 GMT  
		Size: 51.5 MB (51508624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63321d7b44a2e66f8fd42f6b73d9e458f64ac3c1bfea759bb50171f4639845f1`  
		Last Modified: Fri, 27 Jan 2023 23:25:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99395e97254f1bfc34471a669f7f2da99c80a964394bce8228c536779e65250b`  
		Last Modified: Fri, 27 Jan 2023 23:25:53 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab03ec864060a7af507a16864d651a511bf4803401b1db9cddd6c30840c147f3`  
		Last Modified: Fri, 27 Jan 2023 23:26:26 GMT  
		Size: 1.4 MB (1375657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395d3b277894903160d4faf2243b6f04e8bbb898dba02466801335af834f6add`  
		Last Modified: Fri, 27 Jan 2023 23:26:25 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7eb7aa130a05e9e504fdc972e165910a8c4cd2a443c085b07ebdd0cacdceb`  
		Last Modified: Fri, 27 Jan 2023 23:26:25 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43c941812ab4258247daac8b1e0e3676385e99d6fc134058f98ec87c8182deb`  
		Last Modified: Fri, 27 Jan 2023 23:26:29 GMT  
		Size: 20.3 MB (20325931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76135f5cef92332e63c16949b8828e972c4a66f293fe9ecaed4d89df2363af5`  
		Last Modified: Fri, 27 Jan 2023 23:26:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:41811e4b2f65f7ed59a208627ce022e9affc8712f2855a7934ee7995741cab84
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125656549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459bdade5eeb96151fc7c7e8e518a5dfd58227d368429ce58100babaf819c447`
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
# Sat, 21 Jan 2023 00:39:20 GMT
ENV DOCKER_VERSION=23.0.0-rc.3
# Sat, 21 Jan 2023 00:39:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 27 Jan 2023 23:39:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.1
# Fri, 27 Jan 2023 23:39:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-amd64'; 			sha256='31be610820f12fdf5e1c310886e95856e659f647e26965f819bd728dcc94fe18'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v6'; 			sha256='60c0044dca2c82bc336af15c5529262a88ce4509e75ad5730db10bf688820b0e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm-v7'; 			sha256='2ee39cf64dcf64505f1c7d6213052b8bda39b06e1410c21098d3ca5a3eb72fe7'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-arm64'; 			sha256='1561306348d5ffd63b2fe5e32f3440dd4e8751faf94ffa3103364cb94818f5ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-ppc64le'; 			sha256='1cf2e28fa82064bc05c8a69a2a0b798c7adbe572e53042a4dcd604ae9f0103ad'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-riscv64'; 			sha256='46e2188c265b684f224a3fbdb11a40531057e278a580cd3ca01b2042f48c492b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.1/buildx-v0.10.1.linux-s390x'; 			sha256='e4cecfa4c4489385c4cb1ce6f9f518c9afce63705588088c5d32c7c286c9c41a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 27 Jan 2023 23:39:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.1
# Fri, 27 Jan 2023 23:39:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64'; 			sha256='bcfd9ea51dee4c19dccdfaeef0e7956ef68bf14f3d175933742061a7271ef0f5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv6'; 			sha256='a8934600100af88f535eb50b45c7d8d2ac37835221803ba2910e0b167b3af22e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-armv7'; 			sha256='e5b03ac1258ad4243af0ac4afcb1c6cc8c9956b2483a50309cdb38cdb8387e37'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-aarch64'; 			sha256='14d31297794868520cb2e61b543bb1c821aaa484af22b397904314ae8227f6a2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-ppc64le'; 			sha256='bdada874a26d382b20ced7c170707a1ebcf9f20d7d6f394b962076968473ca9c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-riscv64'; 			sha256='9cc1b9c8de313a1e43b8f3dcca47c29eeb87af3de24c67448c463bf882166430'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-s390x'; 			sha256='cf311824af115d0bece5d5d60a73464912dad07cdd00fdaa469dabbcad60f289'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 27 Jan 2023 23:39:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 27 Jan 2023 23:39:26 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:39:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 27 Jan 2023 23:39:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 27 Jan 2023 23:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:39:27 GMT
CMD ["sh"]
# Fri, 27 Jan 2023 23:39:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 27 Jan 2023 23:39:34 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 27 Jan 2023 23:39:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 27 Jan 2023 23:39:39 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 27 Jan 2023 23:39:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 27 Jan 2023 23:39:40 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 27 Jan 2023 23:39:40 GMT
VOLUME [/var/lib/docker]
# Fri, 27 Jan 2023 23:39:40 GMT
EXPOSE 2375 2376
# Fri, 27 Jan 2023 23:39:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 27 Jan 2023 23:39:40 GMT
CMD []
# Fri, 27 Jan 2023 23:39:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 27 Jan 2023 23:39:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 27 Jan 2023 23:39:44 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 27 Jan 2023 23:39:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-23.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-23.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 27 Jan 2023 23:39:47 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 27 Jan 2023 23:39:47 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 27 Jan 2023 23:39:47 GMT
USER rootless
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
	-	`sha256:b694baa125da6ab4e6e535ad523ce90e4db013b78b806e046d6d2a0231d0e1c8`  
		Last Modified: Sat, 21 Jan 2023 00:41:13 GMT  
		Size: 15.3 MB (15287387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ba4686a975c532b7b037f583d15cc717ffdb10d97f5ccfe8cdcfd3f615f5dd`  
		Last Modified: Fri, 27 Jan 2023 23:41:06 GMT  
		Size: 14.4 MB (14437097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5772895ad0666405de1843a6325dde0e2c1a7167b78413460b42e4095b3c2de`  
		Last Modified: Fri, 27 Jan 2023 23:41:06 GMT  
		Size: 13.1 MB (13080440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b1709577b26298a922159b45612def3c988e506d06157239e047412e2d6328`  
		Last Modified: Fri, 27 Jan 2023 23:41:04 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081a9d7fb08225bfa84524bf6e0918c91384d9c5c67889fd70332b42df0d2b6`  
		Last Modified: Fri, 27 Jan 2023 23:41:04 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1a594797b2708c4e3a2b16c7ef0234a2e71770b236e22397ba2cd3f00c8236`  
		Last Modified: Fri, 27 Jan 2023 23:41:04 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29677e00c958132de5a1090b1aab39441eb639f75a98f66edd6c0605dea11461`  
		Last Modified: Fri, 27 Jan 2023 23:41:19 GMT  
		Size: 7.0 MB (6991058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98bca55938b822fc54b68dd0bf3988e8275a390dee8cfceebef8c60b66ee4c5`  
		Last Modified: Fri, 27 Jan 2023 23:41:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52140281716082631ed30040c22083f10497a30847ac7643775fde63030afc8`  
		Last Modified: Fri, 27 Jan 2023 23:41:24 GMT  
		Size: 46.9 MB (46922083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4bbfe6b73efcb6da742bfcbf85b90ce90d6998daeae6e6144e00130037b36`  
		Last Modified: Fri, 27 Jan 2023 23:41:18 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1c559258bfa1d5f26e7542bb8b7614ed813fac22938d4074540ff8425dbc65`  
		Last Modified: Fri, 27 Jan 2023 23:41:18 GMT  
		Size: 2.7 KB (2746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999d9c14630fb8936b7c38e60d08ede93cd3737fcefb840f1972b02e65ae59b5`  
		Last Modified: Fri, 27 Jan 2023 23:41:49 GMT  
		Size: 1.4 MB (1401550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe0bc11eae0f38f46610916efde923919744e07d92e03314a497f2edc020481`  
		Last Modified: Fri, 27 Jan 2023 23:41:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7f7578a2f80ef6afbd8587a05b959043d8796d02596aadfbd60e18b35386f3`  
		Last Modified: Fri, 27 Jan 2023 23:41:48 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc62a3c28c0cabcf77d7889c46bb18a00abed406681f2e5d95211b80df77e37f`  
		Last Modified: Fri, 27 Jan 2023 23:41:52 GMT  
		Size: 22.2 MB (22232238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7dde1534c049b677737c3628db288f46afa36b85afe9c8819ac22e592f1c03`  
		Last Modified: Fri, 27 Jan 2023 23:41:48 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
