## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:8d11a1e09d6505fcf06e6816c5bb752f2b6cde63ee3a1523fde3174440f1c26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ec3a3ed08227980d4ce3aeffabed14030037f00f7c079982b959d0f081dabba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131914511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74704cbdb083c8036e15ee3b2723767632e9354d7b28173e5f67498037404b40`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:50:15 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Sat, 11 Feb 2023 04:50:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Sat, 11 Feb 2023 04:50:52 GMT
ENV DOCKER_VERSION=20.10.23
# Sat, 11 Feb 2023 04:50:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 19:26:19 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 19:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 19:26:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 19:26:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 19:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 19:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 19:26:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:25 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 19:26:31 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 19:26:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 19:26:36 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 19:26:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 19:26:37 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 19:26:37 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 19:26:37 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 19:26:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 19:26:38 GMT
CMD []
# Fri, 17 Feb 2023 19:26:42 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 19:26:42 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 19:26:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 19:26:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 19:26:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 19:26:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 19:26:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fecbccebe0de4401c86ad11eb6d1e80391c0428c0e03c1d1126824d4965cd0`  
		Last Modified: Sat, 11 Feb 2023 04:52:12 GMT  
		Size: 2.1 MB (2064415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52775246328b5488517166f317b58a9d9bd69cc2eaf6e848a5e8bc2c2f5443a`  
		Last Modified: Sat, 11 Feb 2023 04:53:41 GMT  
		Size: 14.0 MB (13983194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7c552a88a39212ffc20730642b0decc72541011c2b844d857d742f1582275`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 16.0 MB (16000579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc012de83bb0a30c1c371da2f12b419cfe677a8fbbc4134f840a2ffd6a3bd664`  
		Last Modified: Fri, 17 Feb 2023 19:28:55 GMT  
		Size: 15.3 MB (15343455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d7aaa39f7071f48be2c5fb524910b4157d2b2e509690fcd57544910d6208c5`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47359bf92c41be26c41bff765be77e68ab6fb3586cd979b086ea2cf1318722cd`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4deb42c6d5b8238b08d107f430cbc0ae3af4938bdd01bcffa2d4768fdb04a1`  
		Last Modified: Fri, 17 Feb 2023 19:28:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5360b4f784053108de5ecf520ad5df69ddc3446cb17470c16047783636e5c`  
		Last Modified: Fri, 17 Feb 2023 19:29:18 GMT  
		Size: 6.8 MB (6837982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbdc36eafd75693d4ff20def87bccbe60a20a4854a86c9de302bcd8eeddcff0`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1687bdd25908a7772c8ebb8939bb7e3928a2589a93ddcaa967ab4c0e27f233af`  
		Last Modified: Fri, 17 Feb 2023 19:29:24 GMT  
		Size: 53.0 MB (53016630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080355d76c433c79c92801716e157420d04702f605701092e12593f8d9678432`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4d65c5fe9754c9bacc628b2b875f3f1437afc05c777f143b5af4a3425ae3`  
		Last Modified: Fri, 17 Feb 2023 19:29:17 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819af3a19eb2fb8344ce5b04fa757fb9fb63812e40af441d06dc6ac69eac599c`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 1.4 MB (1375655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f238c7ade23b8178f135a1bf39b920063dcbb59a2dbd0a5026fda04ec0905`  
		Last Modified: Fri, 17 Feb 2023 19:29:39 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b6cd94b662230d0cc1b1526e981dcf554042288936616ba0d28704aaf85a4`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0564c9b685495c4ee540edd499e066c7585736ab104cee7722448912575c6c0b`  
		Last Modified: Fri, 17 Feb 2023 19:29:42 GMT  
		Size: 19.9 MB (19909539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398903f47c4f6dad9cb5ebeae6746d1afb7c2627a997d396ee0e6359dab2a42`  
		Last Modified: Fri, 17 Feb 2023 19:29:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:622f70fa5e2e00a5aeb8a7995b8b3b48ff324d570d52426b4c156a3d395003bd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125262931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a287719108f01e5325f4867ffa9a3ae7e21c548743a2c6a89a85443a946c834`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:02:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Fri, 10 Feb 2023 22:02:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:37 GMT
ENV DOCKER_VERSION=20.10.23
# Fri, 10 Feb 2023 22:03:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version
# Fri, 17 Feb 2023 22:28:29 GMT
ENV DOCKER_BUILDX_VERSION=0.10.3
# Fri, 17 Feb 2023 22:28:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-amd64'; 			sha256='91f260c9879f8dc8b78912409f8d9f16a3429d457dbcfa0a67169f74837a9290'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v6'; 			sha256='1555a3605ae261cad6e64ace62cd3f5e026cee71fca30a3d9d00dd74b90c8662'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm-v7'; 			sha256='07eb9c583f40cb3e3943a228acd05b01245c5b1f45e1ede95b10a1e7ac45b54c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-arm64'; 			sha256='d37e6824d06bcaaf8bbedb2a802d3b0b9a551aa956a22f52dbcfeba65fe8e427'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-ppc64le'; 			sha256='bc9109501600f12db826ad587d4f342cb9b64e80fdad5b69fac0f75758a912d3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-riscv64'; 			sha256='ef3a7acfb3d991af6a2f846c37b9b02974fd94be1441bb90a7619978467f20cb'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.3/buildx-v0.10.3.linux-s390x'; 			sha256='f743330936b355d2780996f7f0fce296aa4c09fdbdef38775d09c78ca7726e40'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version
# Fri, 17 Feb 2023 22:28:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.16.0
# Fri, 17 Feb 2023 22:28:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-x86_64'; 			sha256='54ab01967b05e392e6bf13afbc654146890b9fa40501b40aca83a2db18f10427'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv6'; 			sha256='59caa4c31a6515a81b44446d978891c5e1d0f460b9b11e38dea27e1bffdb4cd6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-armv7'; 			sha256='558a083683bd597f5e167178dbdbe57824eecf2132bfb497a58f5d39c5e49e8a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-aarch64'; 			sha256='edaf196a0b9ebe749aa1a42a6ce4550d2c6c2620762aa98c36088a9b96fd22ef'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-ppc64le'; 			sha256='aac719dc81ef117bdcca96d7e43ecd605ebcdc1df77c0b09b9d5faf15ccf952e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-riscv64'; 			sha256='8c485ee45cf6be4d483179e925ffeb3b046280d1be045cdfc999c0a011ddfcd1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.16.0/docker-compose-linux-s390x'; 			sha256='fbaff480bd7901c31ead046652c3f5a3c1236766ce9f52fadfa935a18dd463b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version
# Fri, 17 Feb 2023 22:28:35 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 17 Feb 2023 22:28:35 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 17 Feb 2023 22:28:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 17 Feb 2023 22:28:36 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 17 Feb 2023 22:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 22:28:36 GMT
CMD ["sh"]
# Fri, 17 Feb 2023 22:28:41 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 17 Feb 2023 22:28:42 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 17 Feb 2023 22:28:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.23.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.23.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version
# Fri, 17 Feb 2023 22:28:46 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 17 Feb 2023 22:28:47 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 17 Feb 2023 22:28:47 GMT
COPY file:43a39857f9d05e4d332004b3092add05287d8e5c8bc3f32126e6c4b4c3a2c8bb in /usr/local/bin/ 
# Fri, 17 Feb 2023 22:28:47 GMT
VOLUME [/var/lib/docker]
# Fri, 17 Feb 2023 22:28:47 GMT
EXPOSE 2375 2376
# Fri, 17 Feb 2023 22:28:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 17 Feb 2023 22:28:47 GMT
CMD []
# Fri, 17 Feb 2023 22:28:52 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs
# Fri, 17 Feb 2023 22:28:52 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 17 Feb 2023 22:28:53 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 17 Feb 2023 22:28:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.23.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.23.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 17 Feb 2023 22:28:56 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 17 Feb 2023 22:28:56 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 17 Feb 2023 22:28:56 GMT
USER rootless
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c1c5692e7d0cc24a5e526b957e15210c454ed915e9fb77a2190f23a836ef8`  
		Last Modified: Fri, 10 Feb 2023 22:04:53 GMT  
		Size: 2.0 MB (2036946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8849adc6653234eb8d42c0aa5e93834290fbaee0da41b5365ab6c181020a0275`  
		Last Modified: Fri, 10 Feb 2023 22:06:19 GMT  
		Size: 12.7 MB (12741957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07dd11e4059589b4c7b3dc4fe541510095d02aff77b757ab8ef90775cad1056`  
		Last Modified: Fri, 17 Feb 2023 22:31:10 GMT  
		Size: 14.4 MB (14439310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581538f3c33ae42529779e5f48d65f1afa1ac9ad8c0ee2c11e662852b8a932cb`  
		Last Modified: Fri, 17 Feb 2023 22:31:10 GMT  
		Size: 13.8 MB (13819089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59fd73cef811c1741e81ce710dc7110d8086adeaa2d0c02e474bc057c43b9f3`  
		Last Modified: Fri, 17 Feb 2023 22:31:09 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0487890740c757e65a7c6ef0c413d5680c0263f33f6fe4e98f96ea679ba27c`  
		Last Modified: Fri, 17 Feb 2023 22:31:09 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c94f6353b9016ac80747fb518be5cd3278e0aa88b74abb860439b72b1c1649a`  
		Last Modified: Fri, 17 Feb 2023 22:31:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e8fe278c9841517db12e020b7cb4fafcd0601005f85941cb6a52d2b78a4f52`  
		Last Modified: Fri, 17 Feb 2023 22:31:33 GMT  
		Size: 7.0 MB (6991163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12c3f5fc070e7d924d5a5588c1b4c522127153c4f3db2761de17d54ea9825cb`  
		Last Modified: Fri, 17 Feb 2023 22:31:33 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de10f775e9a46d446578af89a2abe12832b03e9d868980a4ef6e8269163c8ee`  
		Last Modified: Fri, 17 Feb 2023 22:31:38 GMT  
		Size: 48.7 MB (48680424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe780443b0c5da1bcc42fec4765e30d8bc29cc5d531371cba3b736f5ebfd821`  
		Last Modified: Fri, 17 Feb 2023 22:31:32 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b61c92894e879d3b2333fd678758c219c212c63aac0dc4e2770a24e496a0b`  
		Last Modified: Fri, 17 Feb 2023 22:31:32 GMT  
		Size: 2.8 KB (2820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16352cbc57835317cafb20e4feb2979ba99aa4dca8a61ee56456f7b24b7c8ce`  
		Last Modified: Fri, 17 Feb 2023 22:31:54 GMT  
		Size: 1.4 MB (1401570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f1924adb96a8019d91f9973e23848ec72ef64cfb6694aa073bb616c77dd6f3`  
		Last Modified: Fri, 17 Feb 2023 22:31:53 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7131a91d33e1ff129a50673e98d127915826f9739d641711e16f1f40a6029275`  
		Last Modified: Fri, 17 Feb 2023 22:31:53 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf6d47557c5f246e494fbf62f086f40e650589032dcc31c41b5d90108279c68`  
		Last Modified: Fri, 17 Feb 2023 22:31:57 GMT  
		Size: 21.9 MB (21881888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1d5238de941b4e804ecbc0e30ec8b4503562cc6bd022e44632d581176da932`  
		Last Modified: Fri, 17 Feb 2023 22:31:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
