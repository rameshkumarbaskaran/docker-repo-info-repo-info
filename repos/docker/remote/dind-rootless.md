## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a46717f16a7beb4139b7fa0157ceadab16bf743372306a87841f6b8636058498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:7436413d95185cde4da98cdfa3fa60f00ec5c41c2005cffc1c06c87445bd95d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23dc91ab4e63260b7de0da5ff1e6f660a42d981fac68c3739541e70bea8cfe48`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:15:12 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Mon, 18 Jul 2022 22:15:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:15:44 GMT
ENV DOCKER_VERSION=20.10.17
# Mon, 18 Jul 2022 22:15:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 18 Jul 2022 22:15:50 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Mon, 18 Jul 2022 22:15:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 20 Jul 2022 23:27:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.7.0
# Wed, 20 Jul 2022 23:27:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-x86_64'; 			sha256='184df811a70366fa339e99df38fc6ff24fc9e51b3388335efe51c1941377d4ce'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-armv6'; 			sha256='a5fc14755a5de6c0998907a73b1eb115e3e45b80a05d284fecab2825a3722fca'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-armv7'; 			sha256='53ed781ff04efa2e93fc6e0c02fc3c7d792083780c747ef06e9e0e46e8bb7eb1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-aarch64'; 			sha256='bcc79aff65b35581246feca30d53261eddcfc79285868061b31f3ff86d102563'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-ppc64le'; 			sha256='a9de33aa3a306ee5a36d2d94e1dd88a5dea1330e774e27d1d7458d44c94d36f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-s390x'; 			sha256='429498246e1d4778669e781a70e659ba59fa8bb3cdee45f8ce8e01a716a12aff'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 20 Jul 2022 23:27:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 20 Jul 2022 23:27:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 20 Jul 2022 23:27:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Jul 2022 23:27:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 20 Jul 2022 23:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 23:27:48 GMT
CMD ["sh"]
# Wed, 20 Jul 2022 23:27:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 20 Jul 2022 23:27:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 20 Jul 2022 23:27:54 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 20 Jul 2022 23:27:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 20 Jul 2022 23:27:55 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 20 Jul 2022 23:27:55 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Jul 2022 23:27:55 GMT
EXPOSE 2375 2376
# Wed, 20 Jul 2022 23:27:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Jul 2022 23:27:56 GMT
CMD []
# Wed, 20 Jul 2022 23:27:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Wed, 20 Jul 2022 23:28:00 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 20 Jul 2022 23:28:01 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 20 Jul 2022 23:28:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 20 Jul 2022 23:28:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 20 Jul 2022 23:28:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 20 Jul 2022 23:28:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33702c1843d19cf7c37af730bcf50c456ac6456ed789053432b000db75d3bed3`  
		Last Modified: Mon, 18 Jul 2022 22:17:03 GMT  
		Size: 2.0 MB (2021603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c203384d5b9b22606055f5a6708153653df701158a6c04748cb77be8238c9e`  
		Last Modified: Mon, 18 Jul 2022 22:17:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146feb07c33136aba6d87c2a8d6882cd4d438d957eaaa8f388f59214f1269bd0`  
		Last Modified: Mon, 18 Jul 2022 22:18:30 GMT  
		Size: 65.5 MB (65511122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6b871713b8386f334ada3f80a6f187b8e9130ce7d69236e34fee9f9d44556`  
		Last Modified: Mon, 18 Jul 2022 22:18:19 GMT  
		Size: 14.5 MB (14454325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8946a7c6c2c651e2344e7e9ebb692ff53ae6ab2b108a5f484384e165056beb`  
		Last Modified: Wed, 20 Jul 2022 23:29:46 GMT  
		Size: 9.4 MB (9382039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649b2db28c4901ee36039690e8086767f9c069ebef2f819f53937774a4b74d6b`  
		Last Modified: Wed, 20 Jul 2022 23:29:44 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b044ff4e6b0f04ba45ff9f486263b0741ce55315ac6fb0498aec49a0375ee0`  
		Last Modified: Wed, 20 Jul 2022 23:29:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd7811a8fce869b1e3e2698db341271fcedfe91a3c90e63b19b243ba4187d91`  
		Last Modified: Wed, 20 Jul 2022 23:29:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9a2b83f06af506a5604e579efa96db12fc2e9a6dabb2e5d8f8976d12618e4d`  
		Last Modified: Wed, 20 Jul 2022 23:30:04 GMT  
		Size: 6.9 MB (6863255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4052cf0d7af0f561342863339ac1b2d1f37ee771bd52569c8189aad45d9c8f68`  
		Last Modified: Wed, 20 Jul 2022 23:30:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668035bf1efe47835345ca9886e537533fe6e96cfad0f9bd4d6db1ce214ba481`  
		Last Modified: Wed, 20 Jul 2022 23:30:03 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd9bc40a60cc9fc21d78501c218debc32591ebb4679bb0b79e5f83e5c54da44`  
		Last Modified: Wed, 20 Jul 2022 23:30:03 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b7db898d1ce4693ba250f48ed8c3536fec04f13528752e54e7de6c964a65f8`  
		Last Modified: Wed, 20 Jul 2022 23:30:23 GMT  
		Size: 1.4 MB (1358398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc1345c06a9de3867e5c3347d2c91ad9868ea9712c68268a34ad7656c58a7bb`  
		Last Modified: Wed, 20 Jul 2022 23:30:22 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1845ec2e995f77714e8474848e950b920dc6c8f033a67de9ff4b4a2c518d6b64`  
		Last Modified: Wed, 20 Jul 2022 23:30:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f1a8110d29ced77d041bdb085f3ea4eff17bd2747d18eb88f008eb9492922`  
		Last Modified: Wed, 20 Jul 2022 23:30:26 GMT  
		Size: 19.3 MB (19346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e4baaa9ac3069d233a5094be1ef7bf49f69ce4b689b92f089fb60f89628f39`  
		Last Modified: Wed, 20 Jul 2022 23:30:23 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4fdd5639eea968612b5b7a78f093e0d1ee8243ddf5cf9ebbee365fcf7bc66067
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115698192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10493d1fe921e071bf74cc7ea11a853e3259aa9f6095764bda91a8f745bf0aa1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 04:35:23 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 19 Jul 2022 04:35:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 19 Jul 2022 04:36:30 GMT
ENV DOCKER_VERSION=20.10.17
# Tue, 19 Jul 2022 04:36:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.17.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.17.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 19 Jul 2022 04:36:35 GMT
ENV DOCKER_BUILDX_VERSION=0.8.2
# Tue, 19 Jul 2022 04:36:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-amd64'; 			sha256='c64de4f3c30f7a73ff9db637660c7aa0f00234368105b0a09fa8e24eebe910c3'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v6'; 			sha256='d0e5d19cd67ea7a351e3bfe1de96f3d583a5b80f1bbadd61f7adcd61b147e5f5'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm-v7'; 			sha256='b5bb1e28e9413a75b2600955c486870aafd234f69953601eecc3664bd3af7463'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-arm64'; 			sha256='304d3d9822c75f98ad9cf57f0c234bcf326bbb96d791d551728cadd72a7a377f'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-ppc64le'; 			sha256='32b317d86c700d920468f162f93ae2282777da556ee49b4329f6c72ee2b11b85'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-riscv64'; 			sha256='76d5fcf92ffa31b3e470d8ec1ab11f7b6997729e5c94d543fec765ad79ad0630'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.8.2/buildx-v0.8.2.linux-s390x'; 			sha256='ec4bb6f271f38dca5a377a70be24ee2108a85f6e6ba511ad3b805c4f1602a0d2'; 			;; 		*) echo >&2 "warning: unsupported buildx architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	docker buildx version
# Wed, 20 Jul 2022 23:50:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.7.0
# Wed, 20 Jul 2022 23:50:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-x86_64'; 			sha256='184df811a70366fa339e99df38fc6ff24fc9e51b3388335efe51c1941377d4ce'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-armv6'; 			sha256='a5fc14755a5de6c0998907a73b1eb115e3e45b80a05d284fecab2825a3722fca'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-armv7'; 			sha256='53ed781ff04efa2e93fc6e0c02fc3c7d792083780c747ef06e9e0e46e8bb7eb1'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-aarch64'; 			sha256='bcc79aff65b35581246feca30d53261eddcfc79285868061b31f3ff86d102563'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-ppc64le'; 			sha256='a9de33aa3a306ee5a36d2d94e1dd88a5dea1330e774e27d1d7458d44c94d36f9'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.7.0/docker-compose-linux-s390x'; 			sha256='429498246e1d4778669e781a70e659ba59fa8bb3cdee45f8ce8e01a716a12aff'; 			;; 		*) echo >&2 "warning: unsupported compose architecture ($apkArch); skipping"; exit 0 ;; 	esac; 	plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	wget -O "$plugin" "$url"; 	echo "$sha256 *$plugin" | sha256sum -c -; 	chmod +x "$plugin"; 	ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 20 Jul 2022 23:50:35 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 20 Jul 2022 23:50:36 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 20 Jul 2022 23:50:36 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 20 Jul 2022 23:50:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 20 Jul 2022 23:50:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 23:50:39 GMT
CMD ["sh"]
# Wed, 20 Jul 2022 23:50:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 20 Jul 2022 23:50:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 20 Jul 2022 23:50:49 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 20 Jul 2022 23:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 20 Jul 2022 23:50:52 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 20 Jul 2022 23:50:52 GMT
VOLUME [/var/lib/docker]
# Wed, 20 Jul 2022 23:50:53 GMT
EXPOSE 2375 2376
# Wed, 20 Jul 2022 23:50:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 20 Jul 2022 23:50:55 GMT
CMD []
# Wed, 20 Jul 2022 23:51:03 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Wed, 20 Jul 2022 23:51:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 20 Jul 2022 23:51:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 20 Jul 2022 23:51:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.17.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.17.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 20 Jul 2022 23:51:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 20 Jul 2022 23:51:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 20 Jul 2022 23:51:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c091ce5682ea3dc37cb34a07cb2f7f7eef6db6db9ce92946c13f6998cddde5d`  
		Last Modified: Tue, 19 Jul 2022 04:38:36 GMT  
		Size: 2.0 MB (1996624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35394750c918441228eb16c7b94ac5f3b42003d306bf543947c63a99ce4bbf56`  
		Last Modified: Tue, 19 Jul 2022 04:38:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031fb191a11dd2614ff760708a09b4c682d5682ed65ee1cd5d1259be00d26852`  
		Last Modified: Tue, 19 Jul 2022 04:40:08 GMT  
		Size: 60.0 MB (60022177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c0caec1c253c973e08fcf8938af67e2f6b8c4acdac32b2227ec8a6feeec4b0`  
		Last Modified: Tue, 19 Jul 2022 04:39:58 GMT  
		Size: 13.1 MB (13097905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81d51e9a0e76156a95ac3137c7dcc945c572179c1a8f0fa759a7ce2ebd991fe`  
		Last Modified: Wed, 20 Jul 2022 23:53:36 GMT  
		Size: 8.6 MB (8595173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620763bd3c3c0488b04fed93237140985366fd31affa9f350f67569712fa79c8`  
		Last Modified: Wed, 20 Jul 2022 23:53:34 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f73d995b25d42b101919b888118d597454253e9569081a2ffe54641238a303f`  
		Last Modified: Wed, 20 Jul 2022 23:53:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c0e9154bf3b0cf86a99702aba5b7232c597741f309de0f2aa24dd9c8f657f`  
		Last Modified: Wed, 20 Jul 2022 23:53:34 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9cb4cd207596676b90181415040222cc962655cc8d10e4bc44120c5db682d3`  
		Last Modified: Wed, 20 Jul 2022 23:53:58 GMT  
		Size: 6.7 MB (6735699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b77458de54f4c6f9c3b7d8709a19636c7c6ad53e8126e73f28804488411dd65`  
		Last Modified: Wed, 20 Jul 2022 23:53:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c8ed8fe187479f0b34de7ed0a85381caba4db063ccbe7f071a10bc44f9495`  
		Last Modified: Wed, 20 Jul 2022 23:53:57 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2406406d2741e2291b3d43aed8fd918c04311e38950fddd10fa46efde5573968`  
		Last Modified: Wed, 20 Jul 2022 23:53:57 GMT  
		Size: 2.8 KB (2753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf133aaa6be55e4f748d20e67b6ab2bcefe81237ddf245381b67a4eb35f670`  
		Last Modified: Wed, 20 Jul 2022 23:54:21 GMT  
		Size: 1.4 MB (1370349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37611a3aa866f1b11851cc2c671c6bbfe5544d7c2d041f2ecdbf86a6b915d410`  
		Last Modified: Wed, 20 Jul 2022 23:54:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc909520181eb8ffac4dadbf51af7ad8b67ce6a7dd52f5a476abb840dfbfdad`  
		Last Modified: Wed, 20 Jul 2022 23:54:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b21bb251fbf60087a8d492fc286f30f3adfdb1b031cf00a861e18338277ba4e`  
		Last Modified: Wed, 20 Jul 2022 23:54:25 GMT  
		Size: 21.2 MB (21177072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4bcc8cced67cec618bc8e0d95381fe2f617ec36eabd6c8ea26c463072ed29e`  
		Last Modified: Wed, 20 Jul 2022 23:54:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
