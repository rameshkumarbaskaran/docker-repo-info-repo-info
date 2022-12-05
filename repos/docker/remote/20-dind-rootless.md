## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:ffc4d98a1b1c125dabee612414807ec078e72785478ff5e2c2bbc87bc6933ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:04d3a1614f4a58b707819e816d4d09a99541e8fab1790259968dd6297e6599c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130244869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f66a31281a5703aabd733191b34a581f23c4d7dd81b2ed76790c83bd17432f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:27:01 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:27:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Tue, 29 Nov 2022 01:27:39 GMT
ENV DOCKER_VERSION=20.10.21
# Tue, 29 Nov 2022 01:27:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 29 Nov 2022 01:27:43 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Tue, 29 Nov 2022 01:27:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 05 Dec 2022 21:20:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.0
# Mon, 05 Dec 2022 21:20:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64'; 			sha256='fdf634ab2b01aca33372bef2bf866699ef2e1f2dab19972e37967b1fc2a11402'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv6'; 			sha256='63e0826ddebc1ae776f38ab872b41f68b48fca246cdf67c709e07eef543cdf88'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv7'; 			sha256='c1664c4dcefc2a56a4f16f4dbd76e531f237bfbf713b90d3acea50df42a1aada'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-aarch64'; 			sha256='0265f45b30f4f0e1d53c1968c590181f64c546129d967460de382c6de38af191'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-ppc64le'; 			sha256='dbee58426af567787e5c1d14e925cca0d0a958edc55203c4b29c10dda8e27355'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-riscv64'; 			sha256='d447a75ff4d900b19d40e0c69811b335518f8a5fbc6377e0aff25a3b999a8c49'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-s390x'; 			sha256='2c5bbb6513d7377919bd4189f25d8bf5d8706a5345f10609d8c49d5cf4d8ab88'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 05 Dec 2022 21:20:13 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 05 Dec 2022 21:20:13 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 05 Dec 2022 21:20:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 05 Dec 2022 21:20:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 05 Dec 2022 21:20:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:20:14 GMT
CMD ["sh"]
# Mon, 05 Dec 2022 21:20:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 05 Dec 2022 21:20:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 05 Dec 2022 21:20:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 05 Dec 2022 21:20:27 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 05 Dec 2022 21:20:27 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 05 Dec 2022 21:20:27 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 05 Dec 2022 21:20:27 GMT
VOLUME [/var/lib/docker]
# Mon, 05 Dec 2022 21:20:28 GMT
EXPOSE 2375 2376
# Mon, 05 Dec 2022 21:20:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 05 Dec 2022 21:20:28 GMT
CMD []
# Mon, 05 Dec 2022 21:20:32 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 05 Dec 2022 21:20:33 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 05 Dec 2022 21:20:33 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 05 Dec 2022 21:20:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 05 Dec 2022 21:20:36 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 05 Dec 2022 21:20:36 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 05 Dec 2022 21:20:36 GMT
USER rootless
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93eea1d5d8e5eb7f3c01c44eb6652605d4b5ad66cf819d1e3b6053733f2f13cf`  
		Last Modified: Tue, 29 Nov 2022 01:28:59 GMT  
		Size: 2.1 MB (2064254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6984615ae18456cfe3414608e241ff765a9b48524ec0d8f2820d1067f08fa892`  
		Last Modified: Tue, 29 Nov 2022 01:30:17 GMT  
		Size: 14.0 MB (13983067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e603bb994164c1620cee092b6fc73ee016c526c92af58f26b3900e68f913a1b`  
		Last Modified: Tue, 29 Nov 2022 01:30:16 GMT  
		Size: 15.2 MB (15204113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4574c54fe4263e68aa09e4e5564427e12d35ea2f382ecb1ec95e847872acde12`  
		Last Modified: Mon, 05 Dec 2022 21:22:37 GMT  
		Size: 14.5 MB (14476601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa297596aa73b85091032d96e504a9e1fa88cacde1344f74f45adaeea39003e3`  
		Last Modified: Mon, 05 Dec 2022 21:22:35 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b35383209c182a3dd55d8c52460fda5561fedf4acd41e7f25c2cddbb477226b`  
		Last Modified: Mon, 05 Dec 2022 21:22:35 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e87bb700b0a9ab1d51b6fae93c7befc600bd440673652214ab4330aa6d27c2`  
		Last Modified: Mon, 05 Dec 2022 21:22:35 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57123aab25b7bafd0ed7fb37cab9d6ecd0786b31dd8b479862497183bf0729dd`  
		Last Modified: Mon, 05 Dec 2022 21:23:04 GMT  
		Size: 6.8 MB (6837765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2150228dd078718b42d5b790f64b86f74c8892c50c42164a0ad7c6bcefc9d67`  
		Last Modified: Mon, 05 Dec 2022 21:23:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178fd42e9286cbddb9678f0fb4d2fb35f5fb2849455e633042bd13aa0aa08fb`  
		Last Modified: Mon, 05 Dec 2022 21:23:11 GMT  
		Size: 53.0 MB (53013560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703c11aa55e52f07181039195bfbbed9b8d05d4edc7d592c0c8c1e741f4eef62`  
		Last Modified: Mon, 05 Dec 2022 21:23:02 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0ddee3b69fffa411d38d94311491bf8cf43f83749d74d58fcc0aefe1eccbae`  
		Last Modified: Mon, 05 Dec 2022 21:23:03 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a96f7685aa0fc7762e127780f4893f8184bd43db9fde43d89f3e536bd9e0fc2`  
		Last Modified: Mon, 05 Dec 2022 21:23:27 GMT  
		Size: 1.4 MB (1375659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3992c55e9e7c34094e5885d8c0c0dd3b8484a4e4793aa8f542dcfb8fb7f52f2`  
		Last Modified: Mon, 05 Dec 2022 21:23:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b442a907add0785fe6b7df2473ce07e2992af28abb08e12a49d0cbfd4d3318eb`  
		Last Modified: Mon, 05 Dec 2022 21:23:27 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058dbb8ece9c5922018477d084ea053a340641e95ea25e756212ef39fb465aff`  
		Last Modified: Mon, 05 Dec 2022 21:23:30 GMT  
		Size: 19.9 MB (19910579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef545679d98a3992b83d8102bbf7dc16bd25ef6785239775bd00177c4095008f`  
		Last Modified: Mon, 05 Dec 2022 21:23:27 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:168d9734a0ea468d0fa71a15c7f2691cb0afea0945b29b425f8c8c06f16f75ca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123813275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5583d03f24d8af62052e01d1f08d19be127d714f390fb7b811a41db2ef1f5c13`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 01:42:08 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Nov 2022 01:42:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Tue, 29 Nov 2022 01:42:55 GMT
ENV DOCKER_VERSION=20.10.21
# Tue, 29 Nov 2022 01:42:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 29 Nov 2022 01:42:59 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Tue, 29 Nov 2022 01:43:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 05 Dec 2022 20:40:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.0
# Mon, 05 Dec 2022 20:40:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64'; 			sha256='fdf634ab2b01aca33372bef2bf866699ef2e1f2dab19972e37967b1fc2a11402'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv6'; 			sha256='63e0826ddebc1ae776f38ab872b41f68b48fca246cdf67c709e07eef543cdf88'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv7'; 			sha256='c1664c4dcefc2a56a4f16f4dbd76e531f237bfbf713b90d3acea50df42a1aada'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-aarch64'; 			sha256='0265f45b30f4f0e1d53c1968c590181f64c546129d967460de382c6de38af191'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-ppc64le'; 			sha256='dbee58426af567787e5c1d14e925cca0d0a958edc55203c4b29c10dda8e27355'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-riscv64'; 			sha256='d447a75ff4d900b19d40e0c69811b335518f8a5fbc6377e0aff25a3b999a8c49'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-s390x'; 			sha256='2c5bbb6513d7377919bd4189f25d8bf5d8706a5345f10609d8c49d5cf4d8ab88'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 05 Dec 2022 20:40:05 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 05 Dec 2022 20:40:05 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 05 Dec 2022 20:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 05 Dec 2022 20:40:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 05 Dec 2022 20:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:40:05 GMT
CMD ["sh"]
# Mon, 05 Dec 2022 20:40:12 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 05 Dec 2022 20:40:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 05 Dec 2022 20:40:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.21.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.21.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 05 Dec 2022 20:40:16 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 05 Dec 2022 20:40:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 05 Dec 2022 20:40:17 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 05 Dec 2022 20:40:17 GMT
VOLUME [/var/lib/docker]
# Mon, 05 Dec 2022 20:40:17 GMT
EXPOSE 2375 2376
# Mon, 05 Dec 2022 20:40:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 05 Dec 2022 20:40:17 GMT
CMD []
# Mon, 05 Dec 2022 20:40:21 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Mon, 05 Dec 2022 20:40:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 05 Dec 2022 20:40:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 05 Dec 2022 20:40:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.21.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.21.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 05 Dec 2022 20:40:24 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 05 Dec 2022 20:40:24 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 05 Dec 2022 20:40:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb5dec0c1f562bd55dc773ccc0c77fbfd42b92083262478523c19bcc0f397af`  
		Last Modified: Tue, 29 Nov 2022 01:44:14 GMT  
		Size: 2.0 MB (2036851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90e06f207318e77d0df221e7f354882895dee491dd233e5d36728caa3e56f7a`  
		Last Modified: Tue, 29 Nov 2022 01:45:27 GMT  
		Size: 12.7 MB (12739256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f45adca886768ef514f318c52a8be2bfb2cf2c3b77a4f79080aee488d34bf51`  
		Last Modified: Tue, 29 Nov 2022 01:45:25 GMT  
		Size: 13.8 MB (13764593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d61cddf01ddc68098c5b2fd19d61bce2f5f132c7ac7b93c397f0a86aedd9b15`  
		Last Modified: Mon, 05 Dec 2022 20:42:24 GMT  
		Size: 13.1 MB (13066783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c9ba3ddce3e9bfe6e84522bbfe59583e4ef7d4fb98391ac49dc00696d3f7d`  
		Last Modified: Mon, 05 Dec 2022 20:42:23 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7deb8a233dd4d65d382b8e84672684f3ab2d31aaef29c104f249ae1bda12f0`  
		Last Modified: Mon, 05 Dec 2022 20:42:23 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1447d85b5ea17ee9732a6be6f2982b71a22de35ff9d893f25b4003f6e38bed89`  
		Last Modified: Mon, 05 Dec 2022 20:42:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f9bf7750a9a771df39fd36d53bf0473b57d5be66c7796fc39225770f0c582`  
		Last Modified: Mon, 05 Dec 2022 20:42:51 GMT  
		Size: 7.0 MB (6990975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011d6af44e2923a3e72b89583ad896d9d3f4f19524fe5c63f2308749b8e7ca39`  
		Last Modified: Mon, 05 Dec 2022 20:42:50 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0c127cb2a153731f96a42c91471c1ca75ae0e84d6caca9b5f94e53dcc569d6`  
		Last Modified: Mon, 05 Dec 2022 20:42:55 GMT  
		Size: 48.7 MB (48665163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4351d2f5d80024f27d4db14ed0b15ce9a5a8d3ed66030c22e573a62adb67a44`  
		Last Modified: Mon, 05 Dec 2022 20:42:50 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee28717f9f0601644002e8c274b7b083f196528d1360ae76fbe92e65f03366f`  
		Last Modified: Mon, 05 Dec 2022 20:42:50 GMT  
		Size: 2.8 KB (2751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e2088b90f776881ac83d50bad18ab20b2af37597afee1bda496e2882a9f80d`  
		Last Modified: Mon, 05 Dec 2022 20:43:12 GMT  
		Size: 1.4 MB (1401540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d731f83b7f6762d74e240b5c63a21bff079d6ef630606d27e5a650ecc58cbbbc`  
		Last Modified: Mon, 05 Dec 2022 20:43:12 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55de5833c48113a726bf4acf6475dffb47c5f06cbc549ae6d9a1052103de3dbe`  
		Last Modified: Mon, 05 Dec 2022 20:43:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d7edcb9a297e7d57855c79f12b82323dca95438df9a59b3574cceb0096f0b3`  
		Last Modified: Mon, 05 Dec 2022 20:43:15 GMT  
		Size: 21.9 MB (21880365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50dc7d0cd576d31dae437cdfdfe9a21979a6e3afe9f2669dcdfdc29f82bcf06`  
		Last Modified: Mon, 05 Dec 2022 20:43:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
