## `docker:dind-rootless`

```console
$ docker pull docker@sha256:b49d0780a52a6111cca9e9c1b9969ae2aed34b98ffc2d375825e0bc3d292be7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ed5bddc9b7a6b01fbc12080258f52d451e09b9fa7e27453565a3561971bdd135
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97151981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85716c44234c63610e9ac53b6c682bbfdf23dfd8bbda5a31e38662a7b7cca9a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Thu, 26 Dec 2019 21:22:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 26 Dec 2019 21:22:15 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_CHANNEL=stable
# Thu, 26 Dec 2019 21:22:15 GMT
ENV DOCKER_VERSION=19.03.5
# Thu, 26 Dec 2019 21:22:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 26 Dec 2019 21:22:22 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Dec 2019 21:22:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 26 Dec 2019 21:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:24 GMT
CMD ["sh"]
# Thu, 26 Dec 2019 21:22:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 26 Dec 2019 21:22:31 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:31 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Thu, 26 Dec 2019 21:22:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 26 Dec 2019 21:22:32 GMT
COPY file:ecdfb2538258e3154663fab9321e96251276aff00fa2a01c2045656e10a627dd in /usr/local/bin/ 
# Thu, 26 Dec 2019 21:22:32 GMT
VOLUME [/var/lib/docker]
# Thu, 26 Dec 2019 21:22:33 GMT
EXPOSE 2375 2376
# Thu, 26 Dec 2019 21:22:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 26 Dec 2019 21:22:33 GMT
CMD []
# Thu, 26 Dec 2019 21:22:38 GMT
RUN apk add --no-cache iproute2
# Thu, 26 Dec 2019 21:22:38 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 26 Dec 2019 21:22:39 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 26 Dec 2019 21:22:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Thu, 26 Dec 2019 21:22:41 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Thu, 26 Dec 2019 21:22:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Thu, 26 Dec 2019 21:22:53 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 26 Dec 2019 21:22:53 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 26 Dec 2019 21:22:54 GMT
USER rootless
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb3b77ad49c7f3dc1e1240949ada3332fc07949a5fd88bf85ceb284c069509d`  
		Last Modified: Thu, 26 Dec 2019 21:23:12 GMT  
		Size: 2.4 MB (2425153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49ead4c98e3d4d53ca8b2a765a8043f9fb5a3527c1b5d9190b483cb5efbdace`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462afa1330adf1e85f53d5f34449210b4810e791e2c79ec8d2218e550cc06e`  
		Last Modified: Thu, 26 Dec 2019 21:23:24 GMT  
		Size: 63.8 MB (63803055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0637d9fbe54c3be5da0310206745b1fb212029acf8c780e33cf37c11c5d80026`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901dbaeb8b4aa6ef7d8d474e91c43ec83a7393dccf619116c142a4ddd7c4b849`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3652bd79826fd0fb2159012fdfd5aac6290f7be722db70ba4e5aaa331fec88`  
		Last Modified: Thu, 26 Dec 2019 21:23:11 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ec5d62350d3cda807f7e704c87d57b10fb1ba85fe1f699e21f84ad5c27c3f2`  
		Last Modified: Thu, 26 Dec 2019 21:23:30 GMT  
		Size: 5.6 MB (5585653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bd47420cfb04992ddff758284e17deb3e37d458561f6406509ceffbf8f961`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa446682b03f5fef5287800942831e4df43e14496e0cbb951b557e9f6768267f`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0558cf2aea5c752da89127f633b2a7bd9f21b7fbc37a193e1bc94d518b07f551`  
		Last Modified: Thu, 26 Dec 2019 21:23:29 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5afa62504214ebc0e35f7b268206c5d3b085f11adc540da5182ce3f7c1e318`  
		Last Modified: Thu, 26 Dec 2019 21:23:37 GMT  
		Size: 796.0 KB (795975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488acedb0ba32c098e28d9367064264249cae2021bc8e92d088a090b3999a0a1`  
		Last Modified: Thu, 26 Dec 2019 21:23:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c5d96ac8be9e3a3700cff8202049a5a14d4fdac438c153203c2e0680f24bd3`  
		Last Modified: Thu, 26 Dec 2019 21:23:36 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d924b263099a8c8faf2059c7bae3edb1d4d26f287b93697d651d173f97a3345c`  
		Last Modified: Thu, 26 Dec 2019 21:23:39 GMT  
		Size: 9.1 MB (9109447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8807edea1c6e0e26902e72213eeb7190dc14e8e613244598f0a05f2592407d26`  
		Last Modified: Thu, 26 Dec 2019 21:23:39 GMT  
		Size: 12.6 MB (12622908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c24f722998c19cb04fe828ce826fae1e96d31ceff3dc848ac9bc5d4fe6dffac`  
		Last Modified: Thu, 26 Dec 2019 21:23:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
