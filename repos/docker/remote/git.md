## `docker:git`

```console
$ docker pull docker@sha256:46f45256fe30f752757284d92d2fb786fde906773f443944697496594cc3d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:78c3bf68d760204982aa488954c8009816f3413d2eed85b40d188312ed90a92c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101113440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0da71b7df62168fcc9690d11b40e49d89d7e7a9ac6eefb7451e7c132af8f699`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 20 Jul 2022 23:28:08 GMT
RUN apk add --no-cache git
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
	-	`sha256:1a83d24e1e6e015080755c0dc2a33bf8deef755e13e82d590dcedc36f46c3b5a`  
		Last Modified: Wed, 20 Jul 2022 23:30:43 GMT  
		Size: 6.9 MB (6943672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:05b5a915e52a37ab7def711fd2aca2e9b988917e4ea4cf5f481d39c48dacc3c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93465419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abdc73e7e2f40163148cc8d977702e2c17962d78e7bd29ef7a4da20d6c24a86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Wed, 20 Jul 2022 23:51:16 GMT
RUN apk add --no-cache git
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
	-	`sha256:eb69026465ce672780301878b16a7698a99dd554f189220c87db33b020845c51`  
		Last Modified: Wed, 20 Jul 2022 23:54:46 GMT  
		Size: 7.1 MB (7056975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
