## `docker:test-dind-rootless`

```console
$ docker pull docker@sha256:1fcc48420e7c2c216f0c32923267fe471a134270c8405156c67f2c4c5d72e6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:test-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e4353296f241b85976ea7f1885b00fed7be4ea44268d5fbd22b7c302b7b17710
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97580840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88504cd9a3f192922c817319508a9c5f9f5b506682835c320873b17dd12deee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 04 Mar 2020 17:21:51 GMT
ENV DOCKER_VERSION=19.03.7
# Wed, 04 Mar 2020 17:21:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 04 Mar 2020 17:21:57 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 04 Mar 2020 17:21:57 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:21:57 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Mar 2020 17:21:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 04 Mar 2020 17:21:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Mar 2020 17:21:58 GMT
CMD ["sh"]
# Wed, 04 Mar 2020 17:22:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 04 Mar 2020 17:22:05 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 04 Mar 2020 17:22:05 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 04 Mar 2020 17:22:06 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 04 Mar 2020 17:22:07 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Wed, 04 Mar 2020 17:22:07 GMT
VOLUME [/var/lib/docker]
# Wed, 04 Mar 2020 17:22:07 GMT
EXPOSE 2375 2376
# Wed, 04 Mar 2020 17:22:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 04 Mar 2020 17:22:07 GMT
CMD []
# Wed, 04 Mar 2020 17:22:12 GMT
RUN apk add --no-cache iproute2
# Wed, 04 Mar 2020 17:22:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 04 Mar 2020 17:22:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 04 Mar 2020 17:22:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 04 Mar 2020 17:22:16 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Wed, 04 Mar 2020 17:22:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 04 Mar 2020 17:22:28 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 04 Mar 2020 17:22:28 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 04 Mar 2020 17:22:28 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa4cf184ccf4b52d5c8d08df033371766d079793fe1867970b60474ac4fc507`  
		Last Modified: Wed, 04 Mar 2020 17:23:02 GMT  
		Size: 64.2 MB (64218024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aca4f9099240ff6a1a6e2e518fb4daf0eef7b50a9b967ad64286e48bebd3104`  
		Last Modified: Wed, 04 Mar 2020 17:22:44 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60fe6b6c13841ddde5debfedcfc47b25f1676e7f2e3c567fe6e34766258c78e`  
		Last Modified: Wed, 04 Mar 2020 17:22:44 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be01bc37983eab8da8605450958ba7b9f7fd092b3179923b32dfb45741c848f`  
		Last Modified: Wed, 04 Mar 2020 17:22:44 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2e7dd2f7ff9a88146afde90862ff21d3756e2ad8391b39f0b77b19a47087f6`  
		Last Modified: Wed, 04 Mar 2020 17:23:10 GMT  
		Size: 5.6 MB (5598399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8f469d3c2a9233205751c9765649477d7924d26e861cca0747a14e9b34d869`  
		Last Modified: Wed, 04 Mar 2020 17:23:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf5c0c310ba9cf022fbaf0c64aae31d8f300a76f480aaa90d064c236eaf7063`  
		Last Modified: Wed, 04 Mar 2020 17:23:09 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367cd13753e5e7c74e0ecb1d3ec19f3fa50126b80873249c8441df6dd4e8e502`  
		Last Modified: Wed, 04 Mar 2020 17:23:10 GMT  
		Size: 2.5 KB (2535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6141bfb617c1af01bc7c06529965c74d87e42d2f1443c7dc1800432e7cae3bf4`  
		Last Modified: Wed, 04 Mar 2020 17:23:17 GMT  
		Size: 796.0 KB (796001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e93580a4ad9de8706bd94bb723c6c88b0c9fefe97965c822a7afcc7c259fea`  
		Last Modified: Wed, 04 Mar 2020 17:23:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a16432e12743b944b3536a0a26cc715e7ebf954b1d13168d2723ed2560e9fd`  
		Last Modified: Wed, 04 Mar 2020 17:23:17 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101f55e0075f21e2509937b9e1efb80a044ca9a085e09bf91a939c6bc474ae45`  
		Last Modified: Wed, 04 Mar 2020 17:23:20 GMT  
		Size: 9.1 MB (9109450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95b21c4fce4a8090f3cc6a3c39b8d9c1832f8e3c146e33fb8eb4ee2a18e3ca3`  
		Last Modified: Wed, 04 Mar 2020 17:23:19 GMT  
		Size: 12.6 MB (12622836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0682ee4c01c0d29e92f148d15eaec72f7aaad9552eb1063b3698498d12436fc7`  
		Last Modified: Wed, 04 Mar 2020 17:23:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
