## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:183faf5b368ef46014f388bbe43b34b7e41911bb47877b69cd12b24980fd7c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:afeb0037ec2bfc65ffe30fbeb4c1b55c1423bf8fad0c08c41479c6d2eb31ae18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132080495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105b4a2ec268c177f1ab4d99b7e2295b8617657159ef913ffd16b8124c1da277`
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
# Wed, 07 Dec 2022 01:26:54 GMT
ENV DOCKER_VERSION=23.0.0-beta.1
# Wed, 07 Dec 2022 01:26:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 07 Dec 2022 01:26:58 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 07 Dec 2022 01:27:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 16 Dec 2022 23:19:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.1
# Fri, 16 Dec 2022 23:19:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-x86_64'; 			sha256='e0c916bd108c49830c7847e416787387398f97de8dda7c1c35dad59438692664'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv6'; 			sha256='7345474ef0ce498a9e7befb14679d8ba86b8a03e81072cd9cfa4e0345b2eb1d6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv7'; 			sha256='4f283a2341f8faa9dd58fd68ffa45bc4909051ab8d8f376998155ec0a3d4123e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-aarch64'; 			sha256='49924009641e9a60f178b4085c9d308bb726b5ae74eed46c5d1a7dbc8f04948b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-ppc64le'; 			sha256='6699d98c002532f719954ecf8737dfed39d0fd079c71438f04fe0ee63d23f0f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-riscv64'; 			sha256='c5a51c7db8b8008d4645241d917afbbb752829753c83858e030154e8c541d827'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-s390x'; 			sha256='44b132059a2162834e7f7c285362f5a007f2569943496cc1656cce8aaea0dd2b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 16 Dec 2022 23:19:28 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 16 Dec 2022 23:19:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 16 Dec 2022 23:19:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Dec 2022 23:19:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 16 Dec 2022 23:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Dec 2022 23:19:29 GMT
CMD ["sh"]
# Fri, 16 Dec 2022 23:19:34 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 16 Dec 2022 23:19:35 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 16 Dec 2022 23:19:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 16 Dec 2022 23:19:40 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 16 Dec 2022 23:19:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 16 Dec 2022 23:19:41 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 16 Dec 2022 23:19:41 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Dec 2022 23:19:41 GMT
EXPOSE 2375 2376
# Fri, 16 Dec 2022 23:19:41 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Dec 2022 23:19:41 GMT
CMD []
# Fri, 16 Dec 2022 23:19:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 16 Dec 2022 23:19:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 16 Dec 2022 23:19:47 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 16 Dec 2022 23:19:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 16 Dec 2022 23:19:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 16 Dec 2022 23:19:49 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 16 Dec 2022 23:19:50 GMT
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
	-	`sha256:0ef02f9f1efc27efc29707880482dfa2ad75f9438dc67f8e6874b36848775c12`  
		Last Modified: Wed, 07 Dec 2022 01:28:23 GMT  
		Size: 16.2 MB (16206327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8080842079f84ea37ca12e0c88883b94e02511f6a628f2880960051186d33fd`  
		Last Modified: Wed, 07 Dec 2022 01:28:22 GMT  
		Size: 15.2 MB (15204105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f73814769bb410d614ee803ec12a3d6abb893e06b8126ffe9822d77d56cb7d`  
		Last Modified: Fri, 16 Dec 2022 23:21:16 GMT  
		Size: 14.5 MB (14475530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83e8cd5c5fcca21b118b8b05b73a94b686323ff818d17e0c0a7228f5b617dc9`  
		Last Modified: Fri, 16 Dec 2022 23:21:13 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ae9f906a7ea309445d960e8fc86ce5da8deba292e8ae0e467b381eb9a677d`  
		Last Modified: Fri, 16 Dec 2022 23:21:13 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c908555f2b4ce8da15296e95e3d0a05cf360bb4e210e6aaccdbeb5ece30c96f`  
		Last Modified: Fri, 16 Dec 2022 23:21:13 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdb1a60ea6331bef99aa86dac888a0d6cfab4e9998af2c6716ab7766dfd361d`  
		Last Modified: Fri, 16 Dec 2022 23:21:30 GMT  
		Size: 6.8 MB (6837818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a713e49b55b318bf63e126d0cd30655a903071e20a8672a28a268f1c0ba62199`  
		Last Modified: Fri, 16 Dec 2022 23:21:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0541f4b686c52d3ef78d0ff804ec1344f884f365a936041bbeb25ffa0ddca0fd`  
		Last Modified: Fri, 16 Dec 2022 23:21:36 GMT  
		Size: 52.2 MB (52211603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64ec123cf27d46829bfce70f5edec7cbd9060a6110fac5bedb73d36b65ec8ee`  
		Last Modified: Fri, 16 Dec 2022 23:21:28 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841fc1596771f7114d2709bfa27022c8b78212bbd815c410376adb9488186b30`  
		Last Modified: Fri, 16 Dec 2022 23:21:28 GMT  
		Size: 2.8 KB (2751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3220841a9fdf9b991359db181b6775711750e55c6f614098e0c60808bb5cb2c`  
		Last Modified: Fri, 16 Dec 2022 23:22:00 GMT  
		Size: 1.4 MB (1375657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b847a0761f08b0c3345d915e1f0905ba9b0a20fe3aeea5cdb1c205efafc93bbd`  
		Last Modified: Fri, 16 Dec 2022 23:22:00 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7554c5e3b92c330d4e4821ac31e79b84038a3024bec5a099ed6d1ce816993866`  
		Last Modified: Fri, 16 Dec 2022 23:21:59 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b83502408357a14797c91818b3a278b3e79f8183da56b80b030eb91e00af93`  
		Last Modified: Fri, 16 Dec 2022 23:22:03 GMT  
		Size: 20.3 MB (20325933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a3a24cd088ab6ad57b554bdf9c4e14101f7bdd7d3e26802872ec68abccafe4`  
		Last Modified: Fri, 16 Dec 2022 23:21:59 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:27dc8b6d480c34a218b4d4277954215b3675d592affbd87de76e1acb96ebf641
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125818014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da624b4ccc22e50528d88f3d541e97265c8edf01a700bc437a485cda6b2b4ff1`
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
# Wed, 07 Dec 2022 01:45:17 GMT
ENV DOCKER_VERSION=23.0.0-beta.1
# Wed, 07 Dec 2022 01:45:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Wed, 07 Dec 2022 01:45:20 GMT
ENV DOCKER_BUILDX_VERSION=0.9.1
# Wed, 07 Dec 2022 01:45:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-amd64'; 			sha256='a7fb95177792ca8ffc7243fad7bf2f33738b8b999a184b6201f002a63c43d136'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v6'; 			sha256='159925b4e679eb66e7f0312c7d57a97e68a418c1fa602a00dd8b29b6406768f0'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm-v7'; 			sha256='ba8e5359ce9ba24fec6da07f73591c1b20ac0797a2248b0ef8088f57ae3340fc'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-arm64'; 			sha256='bbf6a76bf9aef9c5759ff225b97ce23a24fc11e4fa3cdcae36e5dcf1de2cffc5'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-ppc64le'; 			sha256='1b2441886e556c720c1bf12f18f240113cc45f9eb404c0f162166ca1c96c1b60'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-riscv64'; 			sha256='c32372dad653fc70eb756b2cffd026e74425e807c01accaeed4559da881ff57c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.9.1/buildx-v0.9.1.linux-s390x'; 			sha256='90b0ecf315d741888920dddeac9fe2e141123c4fe79465b7b10fe23521c9c366'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Sat, 17 Dec 2022 00:09:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.14.1
# Sat, 17 Dec 2022 00:10:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-x86_64'; 			sha256='e0c916bd108c49830c7847e416787387398f97de8dda7c1c35dad59438692664'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv6'; 			sha256='7345474ef0ce498a9e7befb14679d8ba86b8a03e81072cd9cfa4e0345b2eb1d6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-armv7'; 			sha256='4f283a2341f8faa9dd58fd68ffa45bc4909051ab8d8f376998155ec0a3d4123e'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-aarch64'; 			sha256='49924009641e9a60f178b4085c9d308bb726b5ae74eed46c5d1a7dbc8f04948b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-ppc64le'; 			sha256='6699d98c002532f719954ecf8737dfed39d0fd079c71438f04fe0ee63d23f0f1'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-riscv64'; 			sha256='c5a51c7db8b8008d4645241d917afbbb752829753c83858e030154e8c541d827'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.14.1/docker-compose-linux-s390x'; 			sha256='44b132059a2162834e7f7c285362f5a007f2569943496cc1656cce8aaea0dd2b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Sat, 17 Dec 2022 00:10:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Sat, 17 Dec 2022 00:10:00 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Sat, 17 Dec 2022 00:10:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sat, 17 Dec 2022 00:10:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Sat, 17 Dec 2022 00:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Dec 2022 00:10:01 GMT
CMD ["sh"]
# Sat, 17 Dec 2022 00:10:06 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Sat, 17 Dec 2022 00:10:06 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Sat, 17 Dec 2022 00:10:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-23.0.0-beta.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-23.0.0-beta.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Sat, 17 Dec 2022 00:10:12 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Sat, 17 Dec 2022 00:10:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Sat, 17 Dec 2022 00:10:13 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Sat, 17 Dec 2022 00:10:13 GMT
VOLUME [/var/lib/docker]
# Sat, 17 Dec 2022 00:10:13 GMT
EXPOSE 2375 2376
# Sat, 17 Dec 2022 00:10:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sat, 17 Dec 2022 00:10:13 GMT
CMD []
# Sat, 17 Dec 2022 00:10:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Sat, 17 Dec 2022 00:10:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Sat, 17 Dec 2022 00:10:19 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Sat, 17 Dec 2022 00:10:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-23.0.0-beta.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-23.0.0-beta.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Sat, 17 Dec 2022 00:10:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Sat, 17 Dec 2022 00:10:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 17 Dec 2022 00:10:22 GMT
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
	-	`sha256:7c931478a7d4262453158b142ce84704388d7a888881237bb0fe62210b5de51e`  
		Last Modified: Wed, 07 Dec 2022 01:46:42 GMT  
		Size: 15.3 MB (15283665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e624c6a935d00e78b1ab5eba821e18b39a5cb5e34e6f3542e06d74ac0800514`  
		Last Modified: Wed, 07 Dec 2022 01:46:41 GMT  
		Size: 13.8 MB (13764593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf6b9c34791d1268f6745bc6e66ed1e2fa06a37aaa4187aab6c43ece5446744`  
		Last Modified: Sat, 17 Dec 2022 00:11:41 GMT  
		Size: 13.1 MB (13064521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7776272d49d54da8401de83370b95896846a3114e93d042941af7cde80c4c8`  
		Last Modified: Sat, 17 Dec 2022 00:11:39 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986a0ba4e16b5d535201fa5887badb9bcf76cda5c0b7801d5f2ebf71923cb38`  
		Last Modified: Sat, 17 Dec 2022 00:11:39 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46de49a00077c8fc0ec4994c5504a234222e9b449ed6e1c6666da19d37e714a8`  
		Last Modified: Sat, 17 Dec 2022 00:11:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a56fd452f10179952b84cedbd9577dde3f39ce4f0c421046c509f43c1d24e1`  
		Last Modified: Sat, 17 Dec 2022 00:11:55 GMT  
		Size: 7.0 MB (6991019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80940f7a7e5330272d3ef6aa722ff464e6f1ce575ba173ed3551f43a222538c2`  
		Last Modified: Sat, 17 Dec 2022 00:11:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837d4f435092a20d5cf1c08f7761b301b4f77a1e0010dde7d76f08dbd08fb132`  
		Last Modified: Sat, 17 Dec 2022 00:11:59 GMT  
		Size: 47.8 MB (47781858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb57956bb3fbd3f80c05a30a900e66616c267859eefe2ee5b7b74e9ed1f2d22`  
		Last Modified: Sat, 17 Dec 2022 00:11:54 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb5ffb6d86147c9e6c00b58c271466b90a03c8449d49cfe45f3765acf252d44`  
		Last Modified: Sat, 17 Dec 2022 00:11:53 GMT  
		Size: 2.8 KB (2754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eca9a3755c2c2feb5c828fd66d98ec3fff9a34062f2d25d87f93a5145311b3e`  
		Last Modified: Sat, 17 Dec 2022 00:12:24 GMT  
		Size: 1.4 MB (1401548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2158234f326b0d55cf07b47e0af86362a2d90e1c979b356d79f6e2b5c35939ac`  
		Last Modified: Sat, 17 Dec 2022 00:12:23 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca2c7518c716f3759813ac0e4c04e5b586dd013e59ae1d571113cc8be897af1`  
		Last Modified: Sat, 17 Dec 2022 00:12:23 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b38edaf1c5f636732282c5de98b886b319a1cad6194ccd81e4078c5e579b86`  
		Last Modified: Sat, 17 Dec 2022 00:12:26 GMT  
		Size: 22.2 MB (22226202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eda138df9e8672e1af95af3528c3fe834d07805f4ef496ba6e762d55f7f3e71`  
		Last Modified: Sat, 17 Dec 2022 00:12:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
