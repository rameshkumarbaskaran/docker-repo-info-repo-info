## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:b1ba6b5c5d00fdfbf812971cbeb72a81bbb9fca8f70a1809b68c74968a49849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e0fbfc60a11eae3ce35434bd72828bf2d74b711dd3fd309ee36f646d69fd30a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98553507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e19ccffdf6245ad57a0ca98e0abd6e6cc5eb4495fe9358f90e1c9837de9c5`
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
# Wed, 11 Mar 2020 21:19:32 GMT
ENV DOCKER_VERSION=19.03.8
# Wed, 11 Mar 2020 21:19:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 11 Mar 2020 21:19:38 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 11 Mar 2020 21:19:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 11 Mar 2020 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:39 GMT
CMD ["sh"]
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 11 Mar 2020 21:19:45 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:46 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Wed, 11 Mar 2020 21:19:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 11 Mar 2020 21:19:47 GMT
COPY file:4e6e736f556c5e54c84a8eadea8263445b94a959e1f3ce178dd6d77ddb579d38 in /usr/local/bin/ 
# Wed, 11 Mar 2020 21:19:47 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Mar 2020 21:19:47 GMT
EXPOSE 2375 2376
# Wed, 11 Mar 2020 21:19:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Mar 2020 21:19:47 GMT
CMD []
# Wed, 11 Mar 2020 21:19:52 GMT
RUN apk add --no-cache iproute2
# Wed, 11 Mar 2020 21:19:53 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 11 Mar 2020 21:19:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 11 Mar 2020 21:19:56 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Wed, 11 Mar 2020 21:19:56 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Wed, 11 Mar 2020 21:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 11 Mar 2020 21:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 11 Mar 2020 21:20:09 GMT
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
	-	`sha256:82dd17ef2c28fbb77b8b589e2e601e3ce86c0b9bcdb9dc73b6330d7ca16dca19`  
		Last Modified: Wed, 11 Mar 2020 21:20:40 GMT  
		Size: 64.2 MB (64218865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca57ea69baf170d62b8d1a51d898ff8d9383e22cd18bbde168ff539e74be8a4`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3af031952ce6719d5ca2f369b2187e1819fdab00252d315555a00048d6b99b7`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29377cccb214061fb46c1d5a1c27f53c366384d34f168cdb8484f5c7fcfb87a`  
		Last Modified: Wed, 11 Mar 2020 21:20:27 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4939ff19fbb72e09aad6b10bc7440f9b23e0983f05c3cf6679a6392a40103b27`  
		Last Modified: Wed, 11 Mar 2020 21:20:48 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617664eed4c7060ec14f8178529d17b8a637b33a19f65101e062e185feda4c1`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8b6f7ec5ec983309648ff91b432c6abc38b547fc0610e3d81ab7e2472ad7ae`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb8de5d1a5be108527d435aef60a4a041879e0ddcf6d747ff324d57a5000f03`  
		Last Modified: Wed, 11 Mar 2020 21:20:47 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af40291eab6e7e25f86e0b385342cfe0318d38212a55bc20dd0aef9d3cc1a708`  
		Last Modified: Wed, 11 Mar 2020 21:20:56 GMT  
		Size: 796.0 KB (796003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd959232e7eccc0e2cb0117fb87809c0a4750269e1486a4ded4cbcff13c7b088`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1d69b9f04b015fb9771d9751d1e6cfe72d91da8d347c8bb83bde351f464b`  
		Last Modified: Wed, 11 Mar 2020 21:20:55 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cdb51a3ef0eb7411052a13cb5c1f4dbcb005a502d6805092f9d0006a963ad7`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 9.1 MB (9109448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ff93d35ca71a9e8a6fcfab5be9089f24b654a6c2c9f0fc46727937a534447`  
		Last Modified: Wed, 11 Mar 2020 21:20:57 GMT  
		Size: 13.6 MB (13594708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc08146368fd44217f9c582fc83a67d4d4b6844c8a9ed76700b579a514f8a4a`  
		Last Modified: Wed, 11 Mar 2020 21:20:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
