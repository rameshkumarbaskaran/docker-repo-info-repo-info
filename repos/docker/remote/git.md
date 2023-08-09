## `docker:git`

```console
$ docker pull docker@sha256:725f30c8cd55b6328fc1b453b1d24795ea0278b3f3b9c954c4ed6a1edfb01ea0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:affe461eb55487613423ab7d9f46cfd7c86e7dc3f46a93550e4c77ef1e45ab23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123654478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8f4303c3cac3ce6a261f4f09d3a65deeaab6270afe1db803dd622436ab3c8b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-x86_64'; 			sha256='b9385dabb7931636a3afc0aee94625ebff3bb29584493a87804afb6ebaf2d916'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv6'; 			sha256='39cef332454d1c7a26e12f8d9ee297908d1da9cb71112ede1816c550766ddb8e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv7'; 			sha256='139275f3453761b46f0837a4e4c2a00883b778abee997e299c52e1bcf3d8fc9f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-aarch64'; 			sha256='e63a24e57d2104a09b37ee6aa04c76f4ae85bdf7a59e1bf79adc6d5f55340a31'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-ppc64le'; 			sha256='9c08eb875a7ffd4a832a585540a4c9c81da5dcab263ec3e704ab1d62b573636f'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-riscv64'; 			sha256='5a3bff32ecf0a5a38a83afeb3dc2effd8ca3d52eb2e07ec000334663d493055b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-s390x'; 			sha256='297be6a0ece070ae95d5caf91a23b89dc1b2563e928db80eee480d7018919ee6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad064af57440dca4202f18dcb750753af2a5b1da4b621df21a3ec2f6cd607c9`  
		Last Modified: Wed, 09 Aug 2023 01:27:03 GMT  
		Size: 2.0 MB (2014262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6efc7f364af6c3e5cb0612b81c99cfaaae02478da24b1a89ff4b07636b3965`  
		Last Modified: Wed, 09 Aug 2023 01:27:04 GMT  
		Size: 16.4 MB (16390644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916a43ed1218ee57d0732a6ca25a0d7c9de3a475f99d498ba555b1c432d1c769`  
		Last Modified: Wed, 09 Aug 2023 01:27:04 GMT  
		Size: 17.5 MB (17459264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fadea4d4ed802b50a5a9025f2a3bd12c578207b60f526d5ddf773811e7a2044`  
		Last Modified: Wed, 09 Aug 2023 01:27:05 GMT  
		Size: 18.0 MB (17988747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b381fa0229e92629cadb724ceeb2f0e63367fe6f5a34b6b1fe47f4d895f80f`  
		Last Modified: Wed, 09 Aug 2023 01:27:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026f462a88bb33b410dd06e825b278cff9c8ee8f9ab96bb14d9019090be28bfb`  
		Last Modified: Wed, 09 Aug 2023 01:27:05 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5e508963a28fda4f994deb04b1032780dffdb131f98191050fecf6ec988164`  
		Last Modified: Wed, 09 Aug 2023 01:27:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2254824a6ba0f93f6a2074a721646112d7e18379a29ae0398eba2033b8ce9b`  
		Last Modified: Wed, 09 Aug 2023 02:17:09 GMT  
		Size: 7.1 MB (7080303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51924c8453aae9aa206edd5d109c47218a72e55c641e1506cbfc91785765ff9d`  
		Last Modified: Wed, 09 Aug 2023 02:17:08 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa3d25b814cd91d08d16670ca84382376e6b60483dda4fa287e4cbeb7cb3226`  
		Last Modified: Wed, 09 Aug 2023 02:17:11 GMT  
		Size: 54.4 MB (54377567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae0e3207a13ad21d90c007ecd6f09e538a451498158cb1926f041db58b7661`  
		Last Modified: Wed, 09 Aug 2023 02:17:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad64cd962bbaea8348769f4ef0b43db6b6301f0b31c16b1c60d153810a7bf8`  
		Last Modified: Wed, 09 Aug 2023 02:17:09 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd67b11adc6ef6f501ebbf31ff423ba395d633b836af83c734162604f16863e`  
		Last Modified: Wed, 09 Aug 2023 03:13:54 GMT  
		Size: 4.9 MB (4935253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:git` - unknown; unknown

```console
$ docker pull docker@sha256:e02e58941424c2a8254d9e8e6f65d52e62337ecb941291bb3769064155718511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.6 KB (812569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d0695bfa2e2d0aeff2080bfd93510e30c67ea14998194dc7e62081b50914e9`

```dockerfile
```

-	Layers:
	-	`sha256:d10e08cea2d93fafb51a9de6ff5e546cd678fa0b10ebdffa80f880cde0f2bc39`  
		Last Modified: Wed, 09 Aug 2023 03:13:53 GMT  
		Size: 799.6 KB (799640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8440ecf947ce32c1a86bdfad5440d8aa35fec60cbfffb9f8b086288a01ce5a0`  
		Last Modified: Wed, 09 Aug 2023 03:13:53 GMT  
		Size: 12.9 KB (12929 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:855984662030850added6ae77586611fe8eeb1b1b516dc9cd871742cff303bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114918094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b086c150baf2e203f2b17ed227adfd13278864bac9b35688af28c173706dae6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 16 May 2023 17:59:38 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Tue, 16 May 2023 17:59:38 GMT
CMD ["/bin/sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_VERSION=24.0.5
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.2
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-x86_64'; 			sha256='b9385dabb7931636a3afc0aee94625ebff3bb29584493a87804afb6ebaf2d916'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv6'; 			sha256='39cef332454d1c7a26e12f8d9ee297908d1da9cb71112ede1816c550766ddb8e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-armv7'; 			sha256='139275f3453761b46f0837a4e4c2a00883b778abee997e299c52e1bcf3d8fc9f'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-aarch64'; 			sha256='e63a24e57d2104a09b37ee6aa04c76f4ae85bdf7a59e1bf79adc6d5f55340a31'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-ppc64le'; 			sha256='9c08eb875a7ffd4a832a585540a4c9c81da5dcab263ec3e704ab1d62b573636f'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-riscv64'; 			sha256='5a3bff32ecf0a5a38a83afeb3dc2effd8ca3d52eb2e07ec000334663d493055b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-linux-s390x'; 			sha256='297be6a0ece070ae95d5caf91a23b89dc1b2563e928db80eee480d7018919ee6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 16 May 2023 17:59:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD ["sh"]
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 16 May 2023 17:59:38 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 16 May 2023 17:59:38 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 16 May 2023 17:59:38 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 May 2023 17:59:38 GMT
VOLUME [/var/lib/docker]
# Tue, 16 May 2023 17:59:38 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 16 May 2023 17:59:38 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 16 May 2023 17:59:38 GMT
CMD []
# Tue, 16 May 2023 17:59:38 GMT
RUN apk add --no-cache git # buildkit
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852f3ef0b5f9b77c7c21abf9035ed77c331514fd6aa1498370a5dbd3e2048b5`  
		Last Modified: Mon, 07 Aug 2023 22:18:57 GMT  
		Size: 2.0 MB (2024556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37278d121b4b21d7bddb02dabb1e78b7fc30c3f3a41e41d6f6967d040f3a1b54`  
		Last Modified: Mon, 07 Aug 2023 22:18:58 GMT  
		Size: 15.4 MB (15435452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c05b0ea06520d0d3c1e2b6753a684589ba3e17e586d4be8ad9ddfbb2d3b1d4c`  
		Last Modified: Mon, 07 Aug 2023 22:18:59 GMT  
		Size: 15.8 MB (15768051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b920faef0f924e0bc6293f765487b42850f8fcc7dc006e00acab7779365e7b3`  
		Last Modified: Mon, 07 Aug 2023 22:18:59 GMT  
		Size: 16.3 MB (16320824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfd071449c0a8d2d4ea27ffa825ac548273b41fc00b7dc76e13263f55c129ac`  
		Last Modified: Mon, 07 Aug 2023 22:18:58 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd8c360864191385b3ebd69155f1dfe1900d09f75ebfc489c01c86434583e8d`  
		Last Modified: Mon, 07 Aug 2023 22:18:59 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fdce017755150f777e27def5147cfbc3441af3770996ea37fd694a0a07bbed`  
		Last Modified: Mon, 07 Aug 2023 22:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc68e27d20d81c5082a28faedb7feda3ac23db34bbbcc2caa1b82b1021eca9`  
		Last Modified: Mon, 07 Aug 2023 22:55:11 GMT  
		Size: 7.3 MB (7291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2c99fcb4ebd1ddf039f1e83fc19e534b2ab9fedf7129a9eedbb875356f8c67`  
		Last Modified: Mon, 07 Aug 2023 22:55:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42173ff4f85357bbcdbea0f5a420603cac5a52162f8d7b6cf30061397ce5fdfb`  
		Last Modified: Mon, 07 Aug 2023 22:55:13 GMT  
		Size: 49.7 MB (49718883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48772cf52f8ea3e9b59a7fa20a40f91c26df17d138fc892cc8f2c44cc87607d4`  
		Last Modified: Mon, 07 Aug 2023 22:55:10 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8520c3392243d65413eb8453582848ba7e8a5bdff7874268638054b34a07af7c`  
		Last Modified: Mon, 07 Aug 2023 22:55:11 GMT  
		Size: 2.8 KB (2792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9c60c4cec33980bb34cba99ed4c48aa55b44ef8eedc4e4cafb4636e8de426f`  
		Last Modified: Tue, 08 Aug 2023 00:16:14 GMT  
		Size: 5.0 MB (5021563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:git` - unknown; unknown

```console
$ docker pull docker@sha256:3f6a93be60c14930bb7c4ec76785458f556403ec9ebadfa24dd2439b57b4274b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **810.6 KB (810619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dcdaaa68cca8bffeae1683fd93e718f5d514c3a0b917194ea92affe08c9204`

```dockerfile
```

-	Layers:
	-	`sha256:bc154a2910e139de71067dc4ecb170e39db9fa3341ca4e85d53fdec2828c95cb`  
		Last Modified: Tue, 08 Aug 2023 00:16:13 GMT  
		Size: 799.9 KB (799855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6db004726bd338f5399ea9c2dd875d6c49e97ef3a4ace21c924c5e8597a07c9`  
		Last Modified: Tue, 08 Aug 2023 00:16:12 GMT  
		Size: 10.8 KB (10764 bytes)  
		MIME: application/vnd.in-toto+json
