## `docker:stable-dind-rootless`

```console
$ docker pull docker@sha256:31c5d05c213d82b95ab7fc9d09ce9f590e95872dad5bacd787bc52c60afec6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:stable-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:410c7903023508e210a021dcd33fecf47c39ec4ae15f361dafe21e719f52cba8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94543878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9e3b078647e2b935e3d0a20888030293df624e527c1c422917085a1637bca5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:13:44 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 24 Apr 2020 14:13:45 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:13:45 GMT
ENV DOCKER_CHANNEL=stable
# Mon, 01 Jun 2020 16:19:39 GMT
ENV DOCKER_VERSION=19.03.11
# Mon, 01 Jun 2020 16:19:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 01 Jun 2020 16:19:45 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 01 Jun 2020 16:19:46 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 01 Jun 2020 16:19:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jun 2020 16:19:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 01 Jun 2020 16:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2020 16:19:47 GMT
CMD ["sh"]
# Mon, 01 Jun 2020 16:19:53 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 01 Jun 2020 16:19:54 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 01 Jun 2020 16:19:54 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Mon, 01 Jun 2020 16:19:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 01 Jun 2020 16:19:55 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Mon, 01 Jun 2020 16:19:55 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jun 2020 16:19:55 GMT
EXPOSE 2375 2376
# Mon, 01 Jun 2020 16:19:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jun 2020 16:19:56 GMT
CMD []
# Mon, 01 Jun 2020 16:20:01 GMT
RUN apk add --no-cache iproute2
# Mon, 01 Jun 2020 16:20:02 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 01 Jun 2020 16:20:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 01 Jun 2020 16:20:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Mon, 01 Jun 2020 16:20:05 GMT
ENV ROOTLESSKIT_VERSION=0.9.1
# Mon, 01 Jun 2020 16:20:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Mon, 01 Jun 2020 16:20:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 01 Jun 2020 16:20:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Jun 2020 16:20:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4c731d6eb3df3a5c5587aacd253a9f6d985fafb5a1c8ea03add752b00888ec`  
		Last Modified: Fri, 24 Apr 2020 14:14:46 GMT  
		Size: 2.0 MB (1994349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79d4ac3cd039c6e3f17d157c79b369e68a1a0d79c310a699cfd4835e283d48`  
		Last Modified: Fri, 24 Apr 2020 14:14:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03778b5123054e1106c9872aef276fd17d486c0e4f0333a23c4d338b51d6c920`  
		Last Modified: Mon, 01 Jun 2020 16:20:51 GMT  
		Size: 61.2 MB (61178676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796a5e6f8b3fcbf50a583aec63229fad7f008e7a6df14ea9322f8df314ff2d7`  
		Last Modified: Mon, 01 Jun 2020 16:20:38 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d64bbb9eee3c1bf8dc66577f62823c83f5d7143c5f4a38a120843689d0f8605`  
		Last Modified: Mon, 01 Jun 2020 16:20:38 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8877bd0f32edb41f2ec7671c98ab852e551391aa5137bfaac3a9d17886e1511`  
		Last Modified: Mon, 01 Jun 2020 16:20:38 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a82334afd0a8907fb0cff5610b0fff5c85f5f1ff52d81a0d47a7d81bd15bcbb`  
		Last Modified: Mon, 01 Jun 2020 16:20:59 GMT  
		Size: 5.5 MB (5544870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8567246d1f35f46a16ac36c60063e9b47f38b9dbe9cdef27857c24a4b2424477`  
		Last Modified: Mon, 01 Jun 2020 16:20:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2d2e333b235a6f578fefea13bb8c27386ba9a0dd330e56f8df7c5d4b1387d3`  
		Last Modified: Mon, 01 Jun 2020 16:20:58 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef51bdf702eefd04a6188a1c67e0ae75d60eaa7b2bf4efe20bc55bf91506a3e2`  
		Last Modified: Mon, 01 Jun 2020 16:20:58 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05a8efc7fae6d4824e11a996af6fcdb64a439a10383fb39abe0c3e818c44ab7`  
		Last Modified: Mon, 01 Jun 2020 16:21:08 GMT  
		Size: 737.9 KB (737899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e159500295128ac94e5fe1aaa1b84839cb7b69bc26d8b07630cd418ec3f3b579`  
		Last Modified: Mon, 01 Jun 2020 16:21:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f46fb844e19814cb7b81cb7927120268337a298da86877d5b4f996657c91d1c`  
		Last Modified: Mon, 01 Jun 2020 16:21:07 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3fcf0ef91e9283c2b63664710e893d1f00f71530231ab31df47ca61865ecb55`  
		Last Modified: Mon, 01 Jun 2020 16:21:09 GMT  
		Size: 9.1 MB (9109453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e74c01dea585f2f00413e88b7c6c65176dc2306d964f19c111c041380e2da9a`  
		Last Modified: Mon, 01 Jun 2020 16:21:09 GMT  
		Size: 13.2 MB (13157317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d944ef072c744f8ed2bdde8b3d0248494127196a31933b43014e0e29a53c1376`  
		Last Modified: Mon, 01 Jun 2020 16:21:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
