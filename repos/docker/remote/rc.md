## `docker:rc`

```console
$ docker pull docker@sha256:156cfd057320db7115f9bb15a593c81d27ff0d07a7f72ce4941e9f3a5c5b8e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:d81dfc1e79da777d9e13b1f9a666148bb31ae665cbd6991f90a4bd8df04ca099
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104005470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ab95f1c7fac1d0c976cf87ff27a669d4dd9d251aae51a6644f8160a286d98f`
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
# Tue, 29 Nov 2022 01:27:02 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 29 Nov 2022 01:27:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 29 Nov 2022 01:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Tue, 29 Nov 2022 01:27:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 05 Dec 2022 21:19:38 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.0
# Mon, 05 Dec 2022 21:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64'; 			sha256='fdf634ab2b01aca33372bef2bf866699ef2e1f2dab19972e37967b1fc2a11402'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv6'; 			sha256='63e0826ddebc1ae776f38ab872b41f68b48fca246cdf67c709e07eef543cdf88'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv7'; 			sha256='c1664c4dcefc2a56a4f16f4dbd76e531f237bfbf713b90d3acea50df42a1aada'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-aarch64'; 			sha256='0265f45b30f4f0e1d53c1968c590181f64c546129d967460de382c6de38af191'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-ppc64le'; 			sha256='dbee58426af567787e5c1d14e925cca0d0a958edc55203c4b29c10dda8e27355'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-riscv64'; 			sha256='d447a75ff4d900b19d40e0c69811b335518f8a5fbc6377e0aff25a3b999a8c49'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-s390x'; 			sha256='2c5bbb6513d7377919bd4189f25d8bf5d8706a5345f10609d8c49d5cf4d8ab88'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 05 Dec 2022 21:19:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 05 Dec 2022 21:19:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 05 Dec 2022 21:19:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 05 Dec 2022 21:19:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 05 Dec 2022 21:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 21:19:42 GMT
CMD ["sh"]
# Mon, 05 Dec 2022 21:19:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 05 Dec 2022 21:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 05 Dec 2022 21:19:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 05 Dec 2022 21:19:53 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 05 Dec 2022 21:19:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 05 Dec 2022 21:19:54 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 05 Dec 2022 21:19:54 GMT
VOLUME [/var/lib/docker]
# Mon, 05 Dec 2022 21:19:54 GMT
EXPOSE 2375 2376
# Mon, 05 Dec 2022 21:19:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 05 Dec 2022 21:19:55 GMT
CMD []
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
	-	`sha256:167876a5be069f24a780c6f691232a898b42897a71a944c290b9ddbc8db9108d`  
		Last Modified: Tue, 29 Nov 2022 01:29:01 GMT  
		Size: 8.7 MB (8706448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbb609ba54efd37f7c5e2c41163e4e2406ba2867404a804a9a1a9fbad592523`  
		Last Modified: Tue, 29 Nov 2022 01:28:59 GMT  
		Size: 15.2 MB (15204113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09716e9ca691a29bd3f1f33472f6f6ebe6d98605748c6809b9772b3a06f3063f`  
		Last Modified: Mon, 05 Dec 2022 21:21:26 GMT  
		Size: 14.5 MB (14476602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b69c926a04e07f8459cb4eff2ffa27b3a36573666f6ff69acd59faa90ee6b0`  
		Last Modified: Mon, 05 Dec 2022 21:21:24 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799a77eae7a2fb5b6e636118304a5313c7f44febac9d6c4b207859c1cb500ca2`  
		Last Modified: Mon, 05 Dec 2022 21:21:24 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfcc82c166e915c52d283a6b17a8c860941a0e801c7c7c6006d7500b317ef3`  
		Last Modified: Mon, 05 Dec 2022 21:21:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b3d1e269b0a60a1f805df2d3fa25a533592e7abd61719f32daeaac924ff54e`  
		Last Modified: Mon, 05 Dec 2022 21:21:40 GMT  
		Size: 6.8 MB (6837784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd8c7ca8d7ee3283ef7f2c3c9a728985e70b39cc97e2c95c7488d2857adbe6b`  
		Last Modified: Mon, 05 Dec 2022 21:21:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603227e8ec913d9976101b06cf648159528ef947222b387ffc4200c872298b04`  
		Last Modified: Mon, 05 Dec 2022 21:21:47 GMT  
		Size: 53.3 MB (53338720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e11563d38ee6ad5d4d85a42d741dea790e02f8d2ae4a44a3143639ea2709eb`  
		Last Modified: Mon, 05 Dec 2022 21:21:39 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e77ad2eb7a7cf756c2c95a10052753327bef932428c0efecbbdf442e0a6ce8`  
		Last Modified: Mon, 05 Dec 2022 21:21:39 GMT  
		Size: 2.8 KB (2753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5f0790e14bea84147d758f9b36d957a64252a7d148d03e7b94f7cf4e4ec6bf46
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96151132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af487508489c701a9927b308a4c538c32c1373b21795abbfd723e92f586658`
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
# Tue, 29 Nov 2022 01:42:08 GMT
ENV DOCKER_VERSION=22.06.0-beta.0
# Tue, 29 Nov 2022 01:42:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Tue, 29 Nov 2022 01:42:11 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Tue, 29 Nov 2022 01:42:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Mon, 05 Dec 2022 20:39:31 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.0
# Mon, 05 Dec 2022 20:39:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-x86_64'; 			sha256='fdf634ab2b01aca33372bef2bf866699ef2e1f2dab19972e37967b1fc2a11402'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv6'; 			sha256='63e0826ddebc1ae776f38ab872b41f68b48fca246cdf67c709e07eef543cdf88'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-armv7'; 			sha256='c1664c4dcefc2a56a4f16f4dbd76e531f237bfbf713b90d3acea50df42a1aada'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-aarch64'; 			sha256='0265f45b30f4f0e1d53c1968c590181f64c546129d967460de382c6de38af191'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-ppc64le'; 			sha256='dbee58426af567787e5c1d14e925cca0d0a958edc55203c4b29c10dda8e27355'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-riscv64'; 			sha256='d447a75ff4d900b19d40e0c69811b335518f8a5fbc6377e0aff25a3b999a8c49'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-linux-s390x'; 			sha256='2c5bbb6513d7377919bd4189f25d8bf5d8706a5345f10609d8c49d5cf4d8ab88'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Mon, 05 Dec 2022 20:39:37 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 05 Dec 2022 20:39:37 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 05 Dec 2022 20:39:37 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 05 Dec 2022 20:39:37 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 05 Dec 2022 20:39:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 05 Dec 2022 20:39:37 GMT
CMD ["sh"]
# Mon, 05 Dec 2022 20:39:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 05 Dec 2022 20:39:44 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 05 Dec 2022 20:39:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-22.06.0-beta.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-22.06.0-beta.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-22.06.0-beta.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-22.06.0-beta.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Mon, 05 Dec 2022 20:39:48 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 05 Dec 2022 20:39:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 05 Dec 2022 20:39:48 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Mon, 05 Dec 2022 20:39:48 GMT
VOLUME [/var/lib/docker]
# Mon, 05 Dec 2022 20:39:49 GMT
EXPOSE 2375 2376
# Mon, 05 Dec 2022 20:39:49 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 05 Dec 2022 20:39:49 GMT
CMD []
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
	-	`sha256:80b845a285d7e5030c4ad0ef7da9967f0d0a1303715750be254e670890a3d095`  
		Last Modified: Tue, 29 Nov 2022 01:44:15 GMT  
		Size: 8.0 MB (8048675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ce1ba28fe13a4eaba8fa7079f76a9adb36b95cbf782e3cfbc6184b190e0e7d`  
		Last Modified: Tue, 29 Nov 2022 01:44:13 GMT  
		Size: 13.8 MB (13764573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7783d324fa9a522be7a78159863d5fcc45911a1816f658a44b681eab5b15adc4`  
		Last Modified: Mon, 05 Dec 2022 20:41:14 GMT  
		Size: 13.1 MB (13066811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d25a5038290f4c67c7b65ec87de9e045404992d8bfbaad3a79cfcd3686a35b3`  
		Last Modified: Mon, 05 Dec 2022 20:41:12 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e77df4799ebce1b1648741a5bd2af19471ec4394fec0ad33726c5f23f6f7b`  
		Last Modified: Mon, 05 Dec 2022 20:41:12 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bb521a34c4f1a687b524cfb9873fcbe2b5a81d6f3425af30a5116c5f6f4248`  
		Last Modified: Mon, 05 Dec 2022 20:41:12 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ae4990c28c337cd3b7280af05db74d421839793aaadb5a62419a154b303c60`  
		Last Modified: Mon, 05 Dec 2022 20:41:28 GMT  
		Size: 7.0 MB (6991005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f65438cc246e33483a558202883d578bd5d3d70da73d4cc7bd720c485fa9d84`  
		Last Modified: Mon, 05 Dec 2022 20:41:27 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42785bf6faea87b398688f51abe051ba5973935be24ea86b011af68a289c7cf`  
		Last Modified: Mon, 05 Dec 2022 20:41:32 GMT  
		Size: 49.0 MB (48977180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0c99f0f2992ff1f54a666adc3be2be37e31dd25a5520c00314c4c940f5db9d`  
		Last Modified: Mon, 05 Dec 2022 20:41:26 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52dc2722d24b344f4bf320ea12c44a1705594d0211c45aca89ebfe4738d72e5`  
		Last Modified: Mon, 05 Dec 2022 20:41:27 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
