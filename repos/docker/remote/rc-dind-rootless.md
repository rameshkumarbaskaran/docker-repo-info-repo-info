## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:a68e0b3369c8f1cf200bca7f77243600be52fb3240fc17ae06197fbc9b3d3fc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:dafb822543bb98ed3c91222ca1ab99b27f590021e4fc442bc6261bf8b4f311f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141910492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9419a545032921b1362e01d3e83da836b8f0cf991373a70e184563a5b24510`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_VERSION=25.0.0-beta.3
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 Dec 2023 18:04:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
CMD ["sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
VOLUME [/var/lib/docker]
# Thu, 21 Dec 2023 18:04:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 21 Dec 2023 18:04:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
CMD []
# Thu, 21 Dec 2023 18:04:29 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 21 Dec 2023 18:04:29 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142e1aa444bb1f56305aafe0606764994b77c624a73690c2dd8a8042a9d41fd`  
		Last Modified: Thu, 21 Dec 2023 21:54:15 GMT  
		Size: 2.0 MB (2018460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9773057d5ca989179bb2b04f44b84609475413058ef8d2df12730c9b08ed49`  
		Last Modified: Thu, 21 Dec 2023 21:54:15 GMT  
		Size: 16.9 MB (16885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b85be145581b625bb964f25e5bff98d881199084b984330936c3a14b860d07`  
		Last Modified: Thu, 21 Dec 2023 21:54:15 GMT  
		Size: 17.2 MB (17195300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e6def8889a59399c076dd1e5bd792623868dbccbefb4de42aa7d8ef478b2dc`  
		Last Modified: Thu, 21 Dec 2023 21:54:15 GMT  
		Size: 17.9 MB (17852057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6bf451d936d94b9b3639df997f0f390720cc611752f725b76f9c99f94fd79c`  
		Last Modified: Thu, 21 Dec 2023 21:54:16 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718d540c199724f60959db37888e1d23527d9abfa310b051455325c80d6f8239`  
		Last Modified: Thu, 21 Dec 2023 21:54:16 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f734790d27f7198f0dbd5e6eb646f6122cd75fbff7d20d388c85a9df63f3ce`  
		Last Modified: Thu, 21 Dec 2023 21:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a269a7a5196a27f63a4d5349f9428f606c0660d7abf089f93ddba8d5470b6f30`  
		Last Modified: Thu, 21 Dec 2023 22:54:11 GMT  
		Size: 7.1 MB (7068028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd10b863ee5d41d540a10a5ce27ddacdf1f1248537c1174229774eb1d2136a4f`  
		Last Modified: Thu, 21 Dec 2023 22:54:11 GMT  
		Size: 83.6 KB (83638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fabd1283dbdb4c01f904bacd755a2a17f5617a3af5129aa205d8d9a05ef26`  
		Last Modified: Thu, 21 Dec 2023 22:54:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccf0e5d6831309ab0e6173f8adde32b35e987751fac4d097619a60da36d2a47`  
		Last Modified: Thu, 21 Dec 2023 22:54:12 GMT  
		Size: 55.6 MB (55553433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1555c0455cc42c492c3c91e43d224fae2cb7df45d3d4fe0c6507483df12e0916`  
		Last Modified: Thu, 21 Dec 2023 22:54:12 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0956410cdf1040b5c9b21ea5996de0dc0a532438bef053e23d66c696849ef5`  
		Last Modified: Thu, 21 Dec 2023 22:54:12 GMT  
		Size: 2.9 KB (2872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aafa76655d46f706d7c37152ac666135b420b197109e8abc85c88aaa8d59dc`  
		Last Modified: Thu, 21 Dec 2023 23:47:44 GMT  
		Size: 974.0 KB (974045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3136fcd8e50b25ba953f736aa0d7b9f9a60b8465fda7fe1f18647499fa5bb5`  
		Last Modified: Thu, 21 Dec 2023 23:47:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e76d069c5401a175c038afc798203cbc1f639aa8f78ffd2b9af197d627db6`  
		Last Modified: Thu, 21 Dec 2023 23:47:44 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce326024c68649fcb8fd34adcffd0942e3161c667e0be6d783b8f0d376f6044`  
		Last Modified: Thu, 21 Dec 2023 23:47:45 GMT  
		Size: 20.9 MB (20862806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aac7001be2155225db60650399a933167e13d77669f7d0abf50bd05d039b27b`  
		Last Modified: Thu, 21 Dec 2023 23:47:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:17794427f42b0216ff7c5cbd622cbfc9ddc5fc0f46309d200712be63172af904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.4 KB (759425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3056f36f662c972d0d115176279a49b50cceb235c9cb2a19bcba3e7e8df27da`

```dockerfile
```

-	Layers:
	-	`sha256:592281521908f45e56b6d46eb87c6f14b936ef559a26a83f05f6f1159966d7c5`  
		Last Modified: Thu, 21 Dec 2023 23:47:44 GMT  
		Size: 727.5 KB (727480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309b3129ba1954c4fcf481a23d7de217251b8ecc9e83b4a83c63d1de77bb45dd`  
		Last Modified: Thu, 21 Dec 2023 23:47:44 GMT  
		Size: 31.9 KB (31945 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:5beb643ceeec349b03356dd9a99e03463b6a22e56dd1e039ed1fdadccd56ee6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135732109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a736d5ea84db1029d34c3e72b1fdc1a8642b2b4a32e28164afc78c53228a62`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_VERSION=25.0.0-beta.3
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 21 Dec 2023 18:04:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
CMD ["sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-beta.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-beta.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
VOLUME [/var/lib/docker]
# Thu, 21 Dec 2023 18:04:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 21 Dec 2023 18:04:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 21 Dec 2023 18:04:29 GMT
CMD []
# Thu, 21 Dec 2023 18:04:29 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-beta.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-beta.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 21 Dec 2023 18:04:29 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 21 Dec 2023 18:04:29 GMT
USER rootless
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eb03ed3f91e53f4d3d72c81f89e5715574d77b4e164986420d97b629db97c9`  
		Last Modified: Thu, 21 Dec 2023 22:16:32 GMT  
		Size: 15.9 MB (15894672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1f3cb86aed01ceda3ee20bfc6e33e04ae55f1d749d214b9bd32149d385fb16`  
		Last Modified: Thu, 21 Dec 2023 22:16:32 GMT  
		Size: 15.6 MB (15640605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8b8cb9524fdc82e249d006f2975d8790a598861db14eaa4eb97ccdf39c6574`  
		Last Modified: Thu, 21 Dec 2023 22:16:32 GMT  
		Size: 16.3 MB (16302331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a74fe510df5303e281516724a63e68606a217d393800c6f11e4bc44b71209b`  
		Last Modified: Thu, 21 Dec 2023 22:16:31 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cfdb183e351ee2fb14080b8fad976a518f429ac12f9a3f2d439e14601d31bb`  
		Last Modified: Thu, 21 Dec 2023 22:16:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95efd6dbfdfa60fd1790425e338a96dc99561ef32affb029b591f5da89f173f5`  
		Last Modified: Thu, 21 Dec 2023 22:16:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89828353b7cef563f8d2990034c9536630a5fa76769c306af67e8a193a5d596a`  
		Last Modified: Thu, 21 Dec 2023 23:19:22 GMT  
		Size: 7.4 MB (7428519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcd3033ffb2925775bc9cd3851a1db2d41e128e266415b42e79bf85fbfe4b62`  
		Last Modified: Thu, 21 Dec 2023 23:19:22 GMT  
		Size: 93.1 KB (93065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9222f9334257fca4606310904ded22c5cb251c893b27ede012e5c751da4cfdcc`  
		Last Modified: Thu, 21 Dec 2023 23:19:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c980d7384d41381715981555e6c8b1b331ad33125101a9b3d5a4ec69537d241`  
		Last Modified: Thu, 21 Dec 2023 23:19:23 GMT  
		Size: 51.3 MB (51255823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4d003996749ddaec3688109cf45de3b455de346b81efbbcac15f89b691050`  
		Last Modified: Thu, 21 Dec 2023 23:19:23 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea7820df91ff2d7d22ebc42558bedd4454b0be5fff62575b338a4b56fb3ae3`  
		Last Modified: Thu, 21 Dec 2023 23:19:23 GMT  
		Size: 2.9 KB (2874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d953a7a07d27e8d9546bfec5b6142c90054657ea33e75d3c547ee7de8342e329`  
		Last Modified: Thu, 21 Dec 2023 23:48:31 GMT  
		Size: 1.0 MB (1016219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f48f28f2a056f902a94d32b7b55e6fae3c271867cf061ead1abfce2fea54f5`  
		Last Modified: Thu, 21 Dec 2023 23:48:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1edce01c50c52a86051153dc85291af1a1af0d445b373905afa717b3f42f67c`  
		Last Modified: Thu, 21 Dec 2023 23:48:31 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9c0482be056d886370592636dc170c82b917a9aa9bef5f132fbdde2150fe28`  
		Last Modified: Thu, 21 Dec 2023 23:48:32 GMT  
		Size: 22.7 MB (22729168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8353d2ea8b4217ca99ea94ba70be015dcc9e7d71ee5fefdd83fc47901aa0c2c`  
		Last Modified: Thu, 21 Dec 2023 23:48:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b27672fed65f892a19fed63c5f9ceee1efba4425fe964d973c837c9f2ee4f3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.5 KB (759495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38552884d5d440188de00d321dcf4a5de984fb28c7681724edefdcace0831bda`

```dockerfile
```

-	Layers:
	-	`sha256:37d8fd1a4c6181a3671a07fe23ed88f465b85ddda39904be7c08f7c009b7159c`  
		Last Modified: Thu, 21 Dec 2023 23:48:30 GMT  
		Size: 727.5 KB (727489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70d46f21a8e97fbf66da81ae58eadc6d47854cbd5baadd92fb280004a83bbec`  
		Last Modified: Thu, 21 Dec 2023 23:48:29 GMT  
		Size: 32.0 KB (32006 bytes)  
		MIME: application/vnd.in-toto+json
