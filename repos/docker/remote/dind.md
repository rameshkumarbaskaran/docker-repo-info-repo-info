## `docker:dind`

```console
$ docker pull docker@sha256:7b7ef8858c96e95fba85cbfa0d216db700a62a3c0fcddaa7a8f3b01b40679f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:7abbf564024e76ee5fc2b055b2a0790db660080bf35a7f827739df76c5622044
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108394154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daac9489dc300a47bcb0ea96855ff17e5353aaab9065dbe19b890f480626683`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:19:24 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Thu, 06 Oct 2022 20:19:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 26 Oct 2022 06:52:17 GMT
ENV DOCKER_VERSION=20.10.21
# Wed, 26 Oct 2022 06:52:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 26 Oct 2022 06:52:22 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 26 Oct 2022 06:52:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Wed, 26 Oct 2022 06:52:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.12.2
# Wed, 26 Oct 2022 06:52:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-x86_64'; 			sha256='36d1728ce001c7f021294be43bdfa3f508038bb00886c34b0794f7731cc9bf4b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv6'; 			sha256='e384beeb08ca89e4aeae5c47c561c5d49905e170d453e59440252015833183af'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv7'; 			sha256='22cfe5b2eab86a4832f328049cafacc8e7d76c12185ea7bdff7e7c7ce42f5f10'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-aarch64'; 			sha256='a2c9819115df18ada4e6a68be37f6515121984189d379456bdfd53058e07128b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-ppc64le'; 			sha256='155df9a23b30011ca5318ee4b2df436938c8cebe03d78c9b349998d1bec9ca79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-riscv64'; 			sha256='e6903410dbf2d8705dbc9984cbf235306c4f85f7dd84b21bc4ed042b6fed4667'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-s390x'; 			sha256='b318a46c768efcc2a5344a859c9dd9b969e5aa0967af0454dd50152e307a3dc3'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 26 Oct 2022 06:52:26 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 26 Oct 2022 06:52:26 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 26 Oct 2022 06:52:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Oct 2022 06:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 26 Oct 2022 06:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 06:52:27 GMT
CMD ["sh"]
# Wed, 26 Oct 2022 06:52:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 26 Oct 2022 06:52:34 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 26 Oct 2022 06:52:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Wed, 26 Oct 2022 06:52:40 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 26 Oct 2022 06:52:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 26 Oct 2022 06:52:41 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 26 Oct 2022 06:52:41 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Oct 2022 06:52:41 GMT
EXPOSE 2375 2376
# Wed, 26 Oct 2022 06:52:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Oct 2022 06:52:41 GMT
CMD []
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0dd730a5c3e0f2ca69ebcd573f312df80344d4349d3cdfc40bdc75c406b44d`  
		Last Modified: Thu, 06 Oct 2022 20:21:25 GMT  
		Size: 2.0 MB (2036059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b90f8029a368ccb8e58eae4ebf51ea850e9116df1d92a8e8687a6902c01e69f`  
		Last Modified: Thu, 06 Oct 2022 20:21:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89466c712af9ab8a7abdd90a1855026b236763417363050776d8b759fe3964b`  
		Last Modified: Wed, 26 Oct 2022 06:53:45 GMT  
		Size: 14.0 MB (13983070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6a0a734fa9e967ad4fcce18686a936d533e0dc1589098834c099d585cc61f5`  
		Last Modified: Wed, 26 Oct 2022 06:53:43 GMT  
		Size: 15.2 MB (15204071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeedf2bf9bb418db005446933330724754a8d9fbf00c647e8542ed66e319be5`  
		Last Modified: Wed, 26 Oct 2022 06:53:43 GMT  
		Size: 14.5 MB (14480779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc3016a91231dd848bfd60343267c98ca9cf384592115d15e58fd6d329db17b`  
		Last Modified: Wed, 26 Oct 2022 06:53:41 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d4345031563663d73d682b529231cc4ec411043fc8031a22c4a2d013192eba`  
		Last Modified: Wed, 26 Oct 2022 06:53:40 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539e1dfa39931c56aa5eeb10acbc0573659d8a17841e8d64bc957d9ec94c259f`  
		Last Modified: Wed, 26 Oct 2022 06:53:40 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0219f7532a8e74e32a1676579f832e53bbac918c55e6eac133f9e23949fba49a`  
		Last Modified: Wed, 26 Oct 2022 06:54:18 GMT  
		Size: 6.9 MB (6863661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190a2fb84408684acc0703ccb3f1c47a0789e6dbcbf370d1804e52acff142cc5`  
		Last Modified: Wed, 26 Oct 2022 06:54:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa203f981c78023ab643c66c72547933cd61117b41ac6b025b36767244b28fa1`  
		Last Modified: Wed, 26 Oct 2022 06:54:28 GMT  
		Size: 53.0 MB (53013554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616ae5a1587823a83d7fd6878543874cafe281db358c5581b52a057ba9eeedd4`  
		Last Modified: Wed, 26 Oct 2022 06:54:17 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d41681601ca19265af75c4bd23dacb2379bcf874b116b269a0581fcdace5005`  
		Last Modified: Wed, 26 Oct 2022 06:54:17 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f47b70ab2a1ccf20e9bed9ba478927d4b1df6c9889912e64123031fd339cf93f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99708405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0635a4760882a58404cac044e55ddcec8c90d89cd7e3256c1618173a70bbb150`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 00:28:46 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 25 Oct 2022 00:28:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 26 Oct 2022 15:08:37 GMT
ENV DOCKER_VERSION=20.10.21
# Wed, 26 Oct 2022 15:08:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 26 Oct 2022 15:08:40 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 26 Oct 2022 15:08:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Wed, 26 Oct 2022 15:08:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.12.2
# Wed, 26 Oct 2022 15:08:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-x86_64'; 			sha256='36d1728ce001c7f021294be43bdfa3f508038bb00886c34b0794f7731cc9bf4b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv6'; 			sha256='e384beeb08ca89e4aeae5c47c561c5d49905e170d453e59440252015833183af'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-armv7'; 			sha256='22cfe5b2eab86a4832f328049cafacc8e7d76c12185ea7bdff7e7c7ce42f5f10'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-aarch64'; 			sha256='a2c9819115df18ada4e6a68be37f6515121984189d379456bdfd53058e07128b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-ppc64le'; 			sha256='155df9a23b30011ca5318ee4b2df436938c8cebe03d78c9b349998d1bec9ca79'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-riscv64'; 			sha256='e6903410dbf2d8705dbc9984cbf235306c4f85f7dd84b21bc4ed042b6fed4667'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.12.2/docker-compose-linux-s390x'; 			sha256='b318a46c768efcc2a5344a859c9dd9b969e5aa0967af0454dd50152e307a3dc3'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Wed, 26 Oct 2022 15:08:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 26 Oct 2022 15:08:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 26 Oct 2022 15:08:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 26 Oct 2022 15:08:45 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 26 Oct 2022 15:08:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 15:08:45 GMT
CMD ["sh"]
# Wed, 26 Oct 2022 15:08:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 26 Oct 2022 15:08:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 26 Oct 2022 15:08:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Wed, 26 Oct 2022 15:08:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 26 Oct 2022 15:08:56 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 26 Oct 2022 15:08:56 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Wed, 26 Oct 2022 15:08:56 GMT
VOLUME [/var/lib/docker]
# Wed, 26 Oct 2022 15:08:56 GMT
EXPOSE 2375 2376
# Wed, 26 Oct 2022 15:08:56 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 26 Oct 2022 15:08:57 GMT
CMD []
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5833820420a0776b323417da6527ee1ed41947060ce2b721ee3dbdb5c828cf1`  
		Last Modified: Tue, 25 Oct 2022 00:30:35 GMT  
		Size: 2.0 MB (2010755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79069699b8305641a125c0409ad7decf0f1b775c9d2e6d13a4f388895271ae15`  
		Last Modified: Tue, 25 Oct 2022 00:30:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444a66d86b54db1b8beaf201fa9d1df30d97cabb54589a1e14bdd37ea781176d`  
		Last Modified: Wed, 26 Oct 2022 15:10:01 GMT  
		Size: 12.7 MB (12739265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8c662400c062de6d81e5c6b4dd0171e529191a4b0f6e0271372690c81a6f00`  
		Last Modified: Wed, 26 Oct 2022 15:09:59 GMT  
		Size: 13.8 MB (13764602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7851778f47af8763e4f5e2d3160b0cadf1c740354823a3895f6d5f4afd0d1c57`  
		Last Modified: Wed, 26 Oct 2022 15:09:59 GMT  
		Size: 13.1 MB (13077285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969048075247946be76542d9faaf75ff6325e5c383b0bbe87eee25a76de28aa9`  
		Last Modified: Wed, 26 Oct 2022 15:09:57 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d268b6129f5979aab3aa69e83e9d00d5b59954f952b41064c753a2da9edba`  
		Last Modified: Wed, 26 Oct 2022 15:09:57 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d72239e8c8beed00219d7ba939a5d9b8b4e24b39db04377ba90c448cfcd352`  
		Last Modified: Wed, 26 Oct 2022 15:09:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b361ec95e14bd79e6d5674e168ce6aa47384935853a767635135052ac5ed5ed`  
		Last Modified: Wed, 26 Oct 2022 15:10:33 GMT  
		Size: 6.7 MB (6736771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ef3a09d4c92fb202b189c3c257d09d1cc08acdb6788fa4392baa5d2399d57`  
		Last Modified: Wed, 26 Oct 2022 15:10:32 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a8d3a2c8e30c40d1991893f9a9007def9fc0b00d04349b9be173091c1f0e2e`  
		Last Modified: Wed, 26 Oct 2022 15:10:38 GMT  
		Size: 48.7 MB (48665159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd14fb18f8f0acc813879723991df281157b87ad7a56915d1a2c54f53653b29`  
		Last Modified: Wed, 26 Oct 2022 15:10:32 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087d56d714a996fbd38b30c9d74ff7f09cbcf585731c333a821009b87a00e81c`  
		Last Modified: Wed, 26 Oct 2022 15:10:32 GMT  
		Size: 2.7 KB (2749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
