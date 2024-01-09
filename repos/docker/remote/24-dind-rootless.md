## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:8b4ed3154b182e3bcfa69fd06455272167c3847c6750d6ed6b6fc4ad330aaea2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c219c2fca1a5f3856b8e552d8180d7bd192ebfc56dfb3cad3bbb9d35e88280dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140043344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4395233c29311fdcdd689e965212308e82b5e24cc8c36567444df4d3cfd1eae`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 26 Oct 2023 17:04:13 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["/bin/sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/var/lib/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD []
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53a859d716d847246628ec5f739d4d7f6c1728f55c205abd1598f2961a2c971`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 2.0 MB (2018457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf01e7f8edca3a0012a20af11f8c2f7be6c2c902de3981ed32bc6ebad2655716`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1c0178eca3693c4ce0502dd216fae6def1dfa4497af2f0d680f888c3a3448a`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 16.4 MB (16400387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bfe81a0ee4e5a2ebbac7ff0b76da9dd5ba83575c207e2b02877fb9e2054034`  
		Last Modified: Fri, 05 Jan 2024 01:53:58 GMT  
		Size: 17.2 MB (17195289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf4974ce8787b54ac0af681cd7f519e3864bd9556ab69f588c33fa58175918`  
		Last Modified: Fri, 05 Jan 2024 01:53:59 GMT  
		Size: 17.9 MB (17852058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28675e076aedbe9776450e25ab7891c5e4a1478ae05a8cc51c67d40be2454b7d`  
		Last Modified: Fri, 05 Jan 2024 01:53:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afea6457077a569f2c37e45b0300ddb42b1c081c1c00b07bf504f78ef68831d8`  
		Last Modified: Fri, 05 Jan 2024 01:53:59 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9082a5a0c9c3065e4969dca03f10a9357bc7c8bc7e4ea8d0f26c1eb10bc65841`  
		Last Modified: Fri, 05 Jan 2024 01:54:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bcda7fcd8a8bb6402add081039e9b9e4f79c5115d91e19ccb03271c3880610`  
		Last Modified: Tue, 09 Jan 2024 00:54:13 GMT  
		Size: 7.1 MB (7068018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03da58e67fb0124eaa7d3a34becb2845ccf494b7f1763b757de8a38194bbab3d`  
		Last Modified: Tue, 09 Jan 2024 00:54:13 GMT  
		Size: 83.6 KB (83639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f604493c922450620e6422597c8f0e3200668a6892ba2892678fd614cfe9a68`  
		Last Modified: Tue, 09 Jan 2024 00:54:13 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0f31f771d69a5dba7cf31d96d3bf3bfa3de423981f821b5359a4c81a2816f`  
		Last Modified: Tue, 09 Jan 2024 00:54:15 GMT  
		Size: 54.4 MB (54371668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae94a413a4a6c2f89a01c7fdd40108897fa670faa3657b28fb09e14f5a29bc`  
		Last Modified: Tue, 09 Jan 2024 00:54:14 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7e7c86a4be0fa713a887c0f7bd24aa798e26c2aa4d2907fc96ae460cfc4506`  
		Last Modified: Tue, 09 Jan 2024 00:54:14 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246734434aed1db335a5c4d95f27498ddcbc3b1244ab79fa4b72975d4d27980e`  
		Last Modified: Tue, 09 Jan 2024 02:47:39 GMT  
		Size: 974.0 KB (974017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e0797b3de9e8878678fa9bb1542181f47eb22582ca8863c876bc4443a2d3a4`  
		Last Modified: Tue, 09 Jan 2024 02:47:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cedc0a773d30ef93fd5f4ded67e026060784ce322dd6d8fbae46970f2d9dd1`  
		Last Modified: Tue, 09 Jan 2024 02:47:39 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f914a3915f0ece1ae4ee9f23c5e49f4ef8548e8d6e1181d55f4154c1f8d00b59`  
		Last Modified: Tue, 09 Jan 2024 02:47:40 GMT  
		Size: 20.7 MB (20661379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87997dcb63ff3e019833abbe8b01e11ee3fd5a971f02aa916aafcd3fd0ed0ec6`  
		Last Modified: Tue, 09 Jan 2024 02:47:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:07521422a9f4671ca2476afa627289ad65d09c721bba8ba7404b60bfdd902ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.4 KB (758406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d0d097d80445b0198fd9d03898a5b0bbcdb8af2e0f3e9eb5adf58339c19012`

```dockerfile
```

-	Layers:
	-	`sha256:be80ebd763922f8986ac79a817fd215288e33b0ccb47d7d0c4fea224cbb9de84`  
		Last Modified: Tue, 09 Jan 2024 02:47:39 GMT  
		Size: 725.2 KB (725157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec07f9c718aaeaf95e4ff951254d8d26b0931aabedea1d4f741d834cd7e1bd8`  
		Last Modified: Tue, 09 Jan 2024 02:47:39 GMT  
		Size: 33.2 KB (33249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9995dc834436922099de7287f03370c695672f4123642f16b70d2156b95aeba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133466891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3077a803c87b9de9ce35133489e28f9bde47200009d2527a1bd658df45eeded1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 26 Oct 2023 17:04:13 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["/bin/sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/var/lib/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD []
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
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
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cd2aef7e75dfb117f3229ae16a845ec7fc5a531dc4703c9570b506ea21c29`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 15.4 MB (15449542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e44a629b948c47ee6da1de5e92365267b4b537fe5fad7bfda80adb3e3f5518`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 15.6 MB (15640605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04298b4e6756d10ff289aaf3ecd71e35a76893d2d0896c9bfb14e81246ec448`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 16.3 MB (16302331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00625aa31c36fd07b00a42fdc96f86e019cd92b3fb6c78893737e23aefc440`  
		Last Modified: Fri, 05 Jan 2024 02:15:26 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fbfa586ea4aa82277160546ce02d4693104a660a28fc41a3c6012be35dc9d2`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f0179b0d1729e72edf34c7bdbbc54a11dddced0d7d5a937a104b39f4d74f3`  
		Last Modified: Fri, 05 Jan 2024 02:15:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c888c82111fa29af8888fb20ea00263fb193bb333c0e07598bd2ffb8c19ad53`  
		Last Modified: Fri, 05 Jan 2024 06:15:10 GMT  
		Size: 7.4 MB (7428479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d864b1096e775d8b77215c9453fd27837d89862fb34052920420260f1c46db80`  
		Last Modified: Fri, 05 Jan 2024 06:15:09 GMT  
		Size: 93.1 KB (93068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c9c04c7c50d5d1563eb06e931bb544ee9307658850a497e3cef850c7fbc4ad`  
		Last Modified: Fri, 05 Jan 2024 06:15:09 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91812c08847e4b8a9fac6febf66b6737a798f5a87ff6f00081bfe3b391d7e65f`  
		Last Modified: Fri, 05 Jan 2024 06:15:11 GMT  
		Size: 49.7 MB (49711214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe041380c5e8ee783d23426da30de77a9331666e65c6b8da2e16f823311f249`  
		Last Modified: Fri, 05 Jan 2024 06:15:10 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b179960a5a8580482089b6fd3f29f22263a7a6ef579eec981906b83e583cf9`  
		Last Modified: Tue, 09 Jan 2024 02:07:02 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391459ce9face6ce09b645ac76bb005cc51322790587197a9d8ad1593493ea39`  
		Last Modified: Tue, 09 Jan 2024 03:21:31 GMT  
		Size: 1.0 MB (1016206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b622078fffebeddfb06c4624da2d602bf2bb79f35573033938ca422844fae4b`  
		Last Modified: Tue, 09 Jan 2024 03:21:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be25b9cdac3e6cb3d60cc4a146c6f4b668deb15310b6dd815d1dea55f9825a8`  
		Last Modified: Tue, 09 Jan 2024 03:21:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e8f552c92a3d54f6f93c8f6ad4fd51d289707d0b1c1d7b6587dc0fe7a5d94`  
		Last Modified: Tue, 09 Jan 2024 03:21:33 GMT  
		Size: 22.5 MB (22452795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8c29a35c5ddbd7beb4810c2e4722b186d699ed83129bc322173f4311e5c962`  
		Last Modified: Tue, 09 Jan 2024 03:21:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6c1ff0ab49534a734105a70c81a2b63a84371b091aa69f9e823d824388ebe734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.5 KB (758480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f04f4c08d45e3ae911b3ccbeee29fb744a48492c1cc87e738d4ac3fcb374c8`

```dockerfile
```

-	Layers:
	-	`sha256:33f22775184eb0ea7a761862b164a8e8e836839519116ab0b31bbeb88bae04ce`  
		Last Modified: Tue, 09 Jan 2024 03:21:31 GMT  
		Size: 725.2 KB (725168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e04d9a321936277fe0f0fe6ad560d24d9d2569529066c32a38f27f584f6abe2`  
		Last Modified: Tue, 09 Jan 2024 03:21:30 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json
