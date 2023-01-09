## `docker:dind-rootless`

```console
$ docker pull docker@sha256:f72e91cd32951940a572779d3aa4c6ffdac9dd85a9a755e2e60e53cb66e35e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:181aaaac52b11b0e803cff63f22cf7d528e719a2fdd195203488395986d55596
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130248692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc58b624115b4d27eb03ab9c4dd7317fdcc9d59d866ab592600d9be6a63e70ff`
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
# Mon, 09 Jan 2023 21:13:35 GMT
ENV DOCKER_VERSION=20.10.22
# Mon, 09 Jan 2023 21:13:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Mon, 09 Jan 2023 21:13:41 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Mon, 09 Jan 2023 21:13:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 09 Jan 2023 21:13:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.0
# Mon, 09 Jan 2023 21:13:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-x86_64'; 			sha256='ba481d45be2b137a2a185abd05f61d6d7766dbedfa038f16e4705760767a206e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv6'; 			sha256='0f46aea568f35decc22e1db6af76decaf1c36b9bb374610bc08c3b3618170f8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv7'; 			sha256='343b552c61d74446fc8e8ce7695f878cb2ad49f7fae98deb7fb76a37f24c251e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-aarch64'; 			sha256='634e397090ca0e857a898d853ab08d7e2f226328b305026c143c68d6ce0686de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-ppc64le'; 			sha256='236831ebb63ad30fe716bf22946c91e21b1277bff2785a8538e616168a0d93f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-riscv64'; 			sha256='365d9bf34ae7a2ad0dc028d13363c8c427db1300b1335834a4e06b7e4fa412af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-s390x'; 			sha256='8072776b50f34d135f90c8118da60749435b2474afee3df96bbd9c95755f7a2f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 09 Jan 2023 21:13:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 09 Jan 2023 21:13:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 09 Jan 2023 21:13:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Jan 2023 21:13:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 09 Jan 2023 21:13:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 21:13:47 GMT
CMD ["sh"]
# Mon, 09 Jan 2023 21:13:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 09 Jan 2023 21:13:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 09 Jan 2023 21:13:57 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 09 Jan 2023 21:13:57 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 09 Jan 2023 21:13:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 09 Jan 2023 21:13:58 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 09 Jan 2023 21:13:58 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Jan 2023 21:13:58 GMT
EXPOSE 2375 2376
# Mon, 09 Jan 2023 21:13:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Jan 2023 21:13:59 GMT
CMD []
# Mon, 09 Jan 2023 21:14:02 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 09 Jan 2023 21:14:03 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 09 Jan 2023 21:14:03 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 09 Jan 2023 21:14:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 09 Jan 2023 21:14:07 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 09 Jan 2023 21:14:07 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Jan 2023 21:14:07 GMT
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
	-	`sha256:0ba836ede3c52b4e50be778327aae06076bede29bc2ccd9f317f54c2268167f9`  
		Last Modified: Mon, 09 Jan 2023 21:16:13 GMT  
		Size: 14.0 MB (13982943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42624319d54272c9bffedc65eb42e2b7a99f3293d597ef18162aa9b223cb364`  
		Last Modified: Mon, 09 Jan 2023 21:16:12 GMT  
		Size: 15.2 MB (15204113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd86fd98caf08a27598b9e1624f985494e4349505c5d6e068bc6ea54435c246`  
		Last Modified: Mon, 09 Jan 2023 21:16:12 GMT  
		Size: 14.5 MB (14477438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3694a9b5f421529379332f458216c37bfabd51cb937cb69f32eaa072c2caaa9`  
		Last Modified: Mon, 09 Jan 2023 21:16:09 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc565ab9379a607eb9f2e4c74d47ffbc774c2537274ae7e85b3418602ce977c`  
		Last Modified: Mon, 09 Jan 2023 21:16:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c433ae52674a57413593010b24f70b9d91e8b31ebd04a31b0092f782bf146d1`  
		Last Modified: Mon, 09 Jan 2023 21:16:09 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2138e94d5db6e54ab378c5e360627cfaa1c3198d91ccb84e25ec35646ac998be`  
		Last Modified: Mon, 09 Jan 2023 21:16:40 GMT  
		Size: 6.8 MB (6837882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455ece194d884a4f5506324a640deb73ccbaf81e619ef1e2ac6cf0693922981`  
		Last Modified: Mon, 09 Jan 2023 21:16:38 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee349781e932d7d383b3063654628baebc32946e9ef56b83fcdba74e87a709c9`  
		Last Modified: Mon, 09 Jan 2023 21:16:47 GMT  
		Size: 53.0 MB (53018054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000882bc847cc33e91da86314fb6c8bd59de63c8573ccdc180b0af961a70d1c6`  
		Last Modified: Mon, 09 Jan 2023 21:16:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8770128049ee74bc690d90f2022b0bddd5b5be510b74ce731cc34feb727357`  
		Last Modified: Mon, 09 Jan 2023 21:16:39 GMT  
		Size: 2.7 KB (2742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e796f2cff66710695b71e84b750ae869d670db1bf04585442dd4b93392150eb`  
		Last Modified: Mon, 09 Jan 2023 21:17:03 GMT  
		Size: 1.4 MB (1375651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc9b07a72645943627879dad3fe2eca387e498e7a883118f780c6ea1b40ffe3`  
		Last Modified: Mon, 09 Jan 2023 21:17:03 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d228119537444aff31a2bcfe4da81431472e8306f8d08af76a99f273f0ab70`  
		Last Modified: Mon, 09 Jan 2023 21:17:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0fff991a3754029336ef4dba8069da4c2e66edc6510a727efb14be136318e`  
		Last Modified: Mon, 09 Jan 2023 21:17:06 GMT  
		Size: 19.9 MB (19909180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1883f8d753a2e2d95af126b81e5a78962c00455690c7f8a4c1adbb8bf6ebb866`  
		Last Modified: Mon, 09 Jan 2023 21:17:03 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6c0dda73483eac2fc33b9601969688828ed9a639becd1d0d15ab7f227dfb3a7e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123839514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963335637f982b0d498dbc5419762d7aaae65cfe93d48dcbcf9121cb1147e817`
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
# Mon, 09 Jan 2023 17:29:40 GMT
ENV DOCKER_VERSION=20.10.22
# Mon, 09 Jan 2023 17:29:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Mon, 09 Jan 2023 17:29:42 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Mon, 09 Jan 2023 17:29:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 09 Jan 2023 17:29:44 GMT
ENV DOCKER_COMPOSE_VERSION=2.15.0
# Mon, 09 Jan 2023 17:29:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-x86_64'; 			sha256='ba481d45be2b137a2a185abd05f61d6d7766dbedfa038f16e4705760767a206e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv6'; 			sha256='0f46aea568f35decc22e1db6af76decaf1c36b9bb374610bc08c3b3618170f8f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-armv7'; 			sha256='343b552c61d74446fc8e8ce7695f878cb2ad49f7fae98deb7fb76a37f24c251e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-aarch64'; 			sha256='634e397090ca0e857a898d853ab08d7e2f226328b305026c143c68d6ce0686de'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-ppc64le'; 			sha256='236831ebb63ad30fe716bf22946c91e21b1277bff2785a8538e616168a0d93f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-riscv64'; 			sha256='365d9bf34ae7a2ad0dc028d13363c8c427db1300b1335834a4e06b7e4fa412af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.15.0/docker-compose-linux-s390x'; 			sha256='8072776b50f34d135f90c8118da60749435b2474afee3df96bbd9c95755f7a2f'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 09 Jan 2023 17:29:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 09 Jan 2023 17:29:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:29:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 09 Jan 2023 17:29:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 09 Jan 2023 17:29:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 17:29:47 GMT
CMD ["sh"]
# Mon, 09 Jan 2023 17:29:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 09 Jan 2023 17:29:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 09 Jan 2023 17:29:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.22.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.22.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 09 Jan 2023 17:29:57 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 09 Jan 2023 17:29:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 09 Jan 2023 17:29:58 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 09 Jan 2023 17:29:58 GMT
VOLUME [/var/lib/docker]
# Mon, 09 Jan 2023 17:29:58 GMT
EXPOSE 2375 2376
# Mon, 09 Jan 2023 17:29:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 09 Jan 2023 17:29:58 GMT
CMD []
# Mon, 09 Jan 2023 17:30:02 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 09 Jan 2023 17:30:02 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 09 Jan 2023 17:30:03 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 09 Jan 2023 17:30:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.22.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.22.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 09 Jan 2023 17:30:06 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 09 Jan 2023 17:30:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 09 Jan 2023 17:30:06 GMT
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
	-	`sha256:3e5567070d966674de4065d4af430ca10957d42583f6fb752fa8a33d1cbaafc1`  
		Last Modified: Mon, 09 Jan 2023 17:32:10 GMT  
		Size: 12.7 MB (12743371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d0f0d9717536c71f21f59fe9bd4193c98236f16044817911d210c56103f508`  
		Last Modified: Mon, 09 Jan 2023 17:32:09 GMT  
		Size: 13.8 MB (13764599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97f76f4c77dd1811c1522df255cfb813d9ed74dcd779f3f9e23c709483733c5`  
		Last Modified: Mon, 09 Jan 2023 17:32:09 GMT  
		Size: 13.1 MB (13069171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c224378d7d2092b72a23f1897dc47b083406ed054f112929088e0351f5550e`  
		Last Modified: Mon, 09 Jan 2023 17:32:07 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496ca6e97232fa7036123430ba2b7196a7255d49b01a2cffb02bb7d9918447ed`  
		Last Modified: Mon, 09 Jan 2023 17:32:07 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695dc555807585f128a263fdcbe39fa32785481673636af9c69ec48e807acdc1`  
		Last Modified: Mon, 09 Jan 2023 17:32:07 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec7c94494f08e97aee85b8246d708a18b039777ec56e316d86b15026641914f`  
		Last Modified: Mon, 09 Jan 2023 17:32:37 GMT  
		Size: 7.0 MB (6991068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dfa07401333c294973ed803100efedae636e92c8f6f99ac23759f5ff4ce0b9`  
		Last Modified: Mon, 09 Jan 2023 17:32:36 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd83e8cf04e91a7bc34d75583b2d809dedcd1a9acfb5bc687131072049471744`  
		Last Modified: Mon, 09 Jan 2023 17:32:42 GMT  
		Size: 48.7 MB (48676636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e73c2afe7ad11be3c21dc9be1d632319066f031a30df8046dd403df1b6123`  
		Last Modified: Mon, 09 Jan 2023 17:32:36 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa33b1efb8a71c8a4574874f511de3408c9507cba869ef173794541cdabd56b3`  
		Last Modified: Mon, 09 Jan 2023 17:32:36 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a43f1edc99470e50a125b2a3fc8a8a4420618adfb0a79aa3145dab4afa71fde`  
		Last Modified: Mon, 09 Jan 2023 17:32:59 GMT  
		Size: 1.4 MB (1401555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3665e66941cfbbc8efcc4aedfb1f45a9f32fcb896b9372b0ddfc28256751c6`  
		Last Modified: Mon, 09 Jan 2023 17:32:59 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6e61614216086a405738f7884c46edd6961218254703732bfda359fa691b8f`  
		Last Modified: Mon, 09 Jan 2023 17:32:59 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf1869fcdb96edce0e9519ac07c7625c1c81686680326e3b2dcd540f481fa44`  
		Last Modified: Mon, 09 Jan 2023 17:33:02 GMT  
		Size: 21.9 MB (21888428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d460e0a2a4906bc7b94654af7e98f14537a17e9d7f940320ecefd2b5353d8f1`  
		Last Modified: Mon, 09 Jan 2023 17:32:59 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
