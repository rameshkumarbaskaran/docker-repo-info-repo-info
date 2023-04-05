## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:52e24c8b7dac5d420336bc404910ae7648809b4161bd15b5ed39cbcad0c1fd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:574d0e6bf4a15594a899e3d2768e61dbf63cd50b8576a9e558fb85c09639d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134354056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a71742096b4c3e269ff671b212c1cca3e78dc1cb256f8e37a0f125d643af8db`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_VERSION=20.10.24
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.24.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.24.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.24.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.24.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 04 Apr 2023 21:27:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
CMD ["sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.24.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.24.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.24.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.24.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
VOLUME [/var/lib/docker]
# Tue, 04 Apr 2023 21:27:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 04 Apr 2023 21:27:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
CMD []
# Tue, 04 Apr 2023 21:27:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.24.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.24.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 04 Apr 2023 21:27:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58d4c93159790b1fa011caf2ec698afe11bc8d70e2d863396f9a2a48b142da1`  
		Last Modified: Wed, 29 Mar 2023 18:46:47 GMT  
		Size: 2.1 MB (2064379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d85d4996fe89c86109a5e6848318bef12adfeaadb609367c14ea420bbfae6`  
		Last Modified: Wed, 29 Mar 2023 18:46:46 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c2d63c93393987388c8e0d7072c4bbe823b8c2624c70fc856f8a2a5994a32`  
		Last Modified: Wed, 05 Apr 2023 00:48:20 GMT  
		Size: 14.1 MB (14117997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aac0a14c67b5fbb55fad8cac994ef5d028747711ab0e4e37489454dda46bb8`  
		Last Modified: Wed, 05 Apr 2023 00:48:19 GMT  
		Size: 16.0 MB (16001750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14084dcc34731245437ce2afe045bf23423b2c956c7bea9b88af1c42d743aed0`  
		Last Modified: Wed, 05 Apr 2023 00:48:19 GMT  
		Size: 16.4 MB (16375109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56320ec6770ca05ad62e2c725a25ccf58f28252e19b82bc38d4b442a4b6ba863`  
		Last Modified: Wed, 05 Apr 2023 00:48:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db30bd5d32923770a94b91574a222d0c2ad3783219a0575d7b64a67efcdef37`  
		Last Modified: Wed, 05 Apr 2023 00:48:16 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f341e479b362dc2959b0b3a506e2728c9935f21d13601ce8d7cc3a145bd87ab1`  
		Last Modified: Wed, 05 Apr 2023 00:48:16 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd287d81a79672dd826b96d526c371cedd6ea63cacdf8bc852fc82e393f9aff`  
		Last Modified: Wed, 05 Apr 2023 00:48:42 GMT  
		Size: 6.8 MB (6839083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448fbd5f15d15a4bb4336c4608fa58aa89e00d968b1a01e975cfa2ff75c5bd9d`  
		Last Modified: Wed, 05 Apr 2023 00:48:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e5de35564b71bfbf62072eac365d085e3ba0623743b2176e3bc11960493a8`  
		Last Modified: Wed, 05 Apr 2023 00:48:48 GMT  
		Size: 53.9 MB (53901024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cdcdef5590cffec6225f3209fb7b12e47286bf7055ec73fcd932ac3fd3e297`  
		Last Modified: Wed, 05 Apr 2023 00:48:41 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2ef335b06115928d2509c7b138c643c98e405f86e38cda4efcb36e70a94209`  
		Last Modified: Wed, 05 Apr 2023 00:48:41 GMT  
		Size: 2.8 KB (2813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729296e618c71581528664e18f8fac5198e1b0308d03735cf79018bc13503308`  
		Last Modified: Wed, 05 Apr 2023 00:49:03 GMT  
		Size: 1.4 MB (1375628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3e9dfd984f9e5669d94b7f522d75de9c506e892bb92614621b0d937f1e2c49`  
		Last Modified: Wed, 05 Apr 2023 00:49:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9871a999079008b891f93fa22af151d45966517401b60976fc10058781bb4448`  
		Last Modified: Wed, 05 Apr 2023 00:49:02 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f28b14e3a76cb958d2b562915f70f4ba9f86fe1259e39e9055b44466770395`  
		Last Modified: Wed, 05 Apr 2023 00:49:06 GMT  
		Size: 20.3 MB (20295783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc2cabb5feee7093b9a550a8eb8c42616fe56afa9446061e2e5429ff3d57667`  
		Last Modified: Wed, 05 Apr 2023 00:49:02 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4d17da05f99fd8cb8102bdb26b08dce9477e696859fa7e04f54861b4d1845a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127330541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b898c44b17823166db75ecc52ecf3232273a2a43c444f839b88699d0d2862265`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_VERSION=20.10.24
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.24.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.24.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.24.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.24.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_BUILDX_VERSION=0.10.4
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-amd64'; 			sha256='dbe68cdc537d0150fc83e3f30974cd0ca11c179dafbf27f32d6f063be26e869b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v6'; 			sha256='d50aa01a22a53e5a0eae9918274c9931b813b5336c0e30061a6b1904efb0c5eb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm-v7'; 			sha256='aabc8cef5b9221ecbcb0af9846004a30591540be8668504d70814efe870448c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-arm64'; 			sha256='e8f666134cf4aa83ec2b1b6afef0c83b1ea1387984d7a40ae6657b7da4d82d91'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-ppc64le'; 			sha256='d107178f36e6c83286f3f9316e2f66b18f08306570cef209cb5840c880bd91ae'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-riscv64'; 			sha256='393db8518aeb442d0ca5f3ccf4800622dfc5eb8993c29bbfccb023cbfde6cdbc'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.4/buildx-v0.10.4.linux-s390x'; 			sha256='16ce9071c14293640e9bcd547ff01578c65cfc68fc6c154091abd81daaf10929'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_COMPOSE_VERSION=2.17.2
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64'; 			sha256='895e20812231543eae9f6b98ef9395327f4f21f1f31fa51fc252d21415802dda'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv6'; 			sha256='16a2ce7e9bc45cb864020fb61a4da7425162cb5215ee7c81c48f98b6a7c945c4'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-armv7'; 			sha256='4c8948696831fde2992e82dfcb505c5d6e4a56df9d759cd39a1dee6b6cded1c0'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-aarch64'; 			sha256='fcc2a21588907a7e6d9aa83538f134d2916f7a756cf391e5ce11b9d67bc4aad0'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-ppc64le'; 			sha256='546e0421cda6f0bbedd82efc2d95daf9775ec736ae0c82bcdc051c952eee09cd'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-riscv64'; 			sha256='65824b6aad564debb5ae9f70423f94bf5bbf20062fa4d9d47d2d2bcaf6a822b7'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-s390x'; 			sha256='4fcf6d847203162eb0a698657b98007542047c167188df3c65cca047b4b656c0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 04 Apr 2023 21:27:52 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
CMD ["sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.24.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.24.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.24.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.24.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
VOLUME [/var/lib/docker]
# Tue, 04 Apr 2023 21:27:52 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 04 Apr 2023 21:27:52 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 04 Apr 2023 21:27:52 GMT
CMD []
# Tue, 04 Apr 2023 21:27:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.24.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.24.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 04 Apr 2023 21:27:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 04 Apr 2023 21:27:52 GMT
USER rootless
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441464e00401568e9fc906ba5092790b0ef071a02adc95dea9f96c224533c0b2`  
		Last Modified: Thu, 30 Mar 2023 05:49:27 GMT  
		Size: 2.0 MB (2036948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da37f279e39fed4b5c19eb0a904b97e3030f30f384158ded047a522ea4b27aa3`  
		Last Modified: Thu, 30 Mar 2023 05:49:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dafe9b75847e20a9e5cdf438f6d696c1233be69d69408c7bc25ee4933cd2f91`  
		Last Modified: Wed, 05 Apr 2023 00:50:54 GMT  
		Size: 12.8 MB (12836224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658433621f2cb0d3d7e456caf1a62b57d74108d0f4609b98173c2bb186bd9b82`  
		Last Modified: Wed, 05 Apr 2023 00:50:53 GMT  
		Size: 14.4 MB (14441506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504bd821770d1dbfb1778e6caedaf71ff9c6923872d234c6622ee055c32112ef`  
		Last Modified: Wed, 05 Apr 2023 00:50:53 GMT  
		Size: 14.8 MB (14830396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f036fbf1a8512911c1f3df99a1140ea084619e532c98cf19717cb85a90a82a`  
		Last Modified: Wed, 05 Apr 2023 00:50:51 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee266ec2899bb5b171ceb19363890c8f7caaa05a6b68be105cfc0f7be69e0a1c`  
		Last Modified: Wed, 05 Apr 2023 00:50:51 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e8d93ec0ae08f5df3b0f77a73f8973534cd467e1c013078cc9c288a33d66f`  
		Last Modified: Wed, 05 Apr 2023 00:50:51 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db6f3dddceba8b02470aba3cbb908cb1f9c92a26c06ec0e1274f983d1ce1232`  
		Last Modified: Wed, 05 Apr 2023 00:51:17 GMT  
		Size: 7.0 MB (6992864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e02306cac4a08360b711961143ecf5a49472ed7d2d19753512ed5cef58d32a`  
		Last Modified: Wed, 05 Apr 2023 00:51:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35cde95b4b2ce21133b36a244ffd6238bbab72d2d1126c3ac066b8195034c25`  
		Last Modified: Wed, 05 Apr 2023 00:51:21 GMT  
		Size: 49.3 MB (49320270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad8459262bf6dde29d10d97bc68b19fc9e42e22d9d2de6f879e768dd2201e6a`  
		Last Modified: Wed, 05 Apr 2023 00:51:16 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8109c9f0581fb39cd07693d3282a50fd97e7dbe32a576c02770c2b29200e830c`  
		Last Modified: Wed, 05 Apr 2023 00:51:16 GMT  
		Size: 2.8 KB (2814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a10fbf06881fb5836ff6a32b26104c7a1f94dd4b0ccd5db9f62591e58aff50a`  
		Last Modified: Wed, 05 Apr 2023 00:51:36 GMT  
		Size: 1.4 MB (1401530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a1eefc195900a14a87e654ef283c99ff8ae1bc7ba37584dbac4ffca7c15a64`  
		Last Modified: Wed, 05 Apr 2023 00:51:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c842714b4ca8099d282fb6f9486308acb0a3062e2e19f0ae8c31d10e9c6ca30`  
		Last Modified: Wed, 05 Apr 2023 00:51:35 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b61a8713825a572db8afad9d8ce3efb0fa47165092d9c59a698ce4a49d19b0b`  
		Last Modified: Wed, 05 Apr 2023 00:51:38 GMT  
		Size: 22.2 MB (22200209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa079e1c954b70e6412d3df63b1f3d0cf00b4e81fa3593e8bbd54e60efbc296`  
		Last Modified: Wed, 05 Apr 2023 00:51:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
