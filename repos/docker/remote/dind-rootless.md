## `docker:dind-rootless`

```console
$ docker pull docker@sha256:22cc04801985eabe176c9e115cdb3b34a6764e7e5c9506e6ad75e6050ba331c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:55d0396f029d381b7313d5b8224be5470043daee2a8634c1b1b960ffa00bed4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137390219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475f5c539c95e2b58734094291fc2890b3d09b0f11110a9264442e06a16f0efb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Fri, 26 May 2023 11:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 26 May 2023 11:04:23 GMT
ENV DOCKER_VERSION=24.0.2
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.10.5
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-amd64'; 			sha256='2f1995ee6c4e7d75668ff38242ce3381da71bd30a8ca1f648f077b0a066c742b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-arm-v6'; 			sha256='cd8d8b3fe02b07d60d323af27da53c72c35516e7c8a52e649e3a68582e113e76'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-arm-v7'; 			sha256='a10b60d9c541b30c8f46ed2c8e671c1c775125d6b71ff0b1787204c11ae84ba9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-arm64'; 			sha256='a60d2dfb46cbe66e7fa75c8fd4fc730bcf052e08b8e236df254c24600db388a9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-ppc64le'; 			sha256='1c1ac2bcad35a7d423e093bceba04e3f0d3f4381e534b64e1fb67e0dc932c973'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-riscv64'; 			sha256='f2da6e8ac73b00bafac1f4ecd76e126e8a3f6740adfcd04fbad0094d30274a55'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-s390x'; 			sha256='9a64f9248a8fa6d5b114d5599018814a1fc950f1910aa73e4fb9d012ca9bcbe6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 26 May 2023 11:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 May 2023 11:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 26 May 2023 11:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 26 May 2023 11:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 May 2023 11:04:23 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:05:39 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:05:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:05:39 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:05:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:05:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:05:39 GMT
CMD []
# Fri, 26 May 2023 11:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 May 2023 11:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 May 2023 11:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb60e7f5d22cf3e06856538fbb2c518c629c1bbe07d62a60d16e3c7fefa06f4`  
		Last Modified: Thu, 11 May 2023 19:23:43 GMT  
		Size: 2.0 MB (2014357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74671f55a8da50720028684fd32ee90f4fdeb79ffcadf0e7213a90cd50ef5c3`  
		Last Modified: Thu, 11 May 2023 19:23:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159682c80b19352ff5d84204bc0f2b07dad0e6f9d8f783e392abf74be5d38e40`  
		Last Modified: Fri, 26 May 2023 22:51:41 GMT  
		Size: 16.4 MB (16376159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd48ba55f881f492fb34fec724d5848e96d8372bc617711e19d452440adb8d`  
		Last Modified: Fri, 26 May 2023 22:51:39 GMT  
		Size: 16.0 MB (16003306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6478cae41da0e3e59a70ad3e99d481560c14e6aee2eff44cdca39d72a8d14681`  
		Last Modified: Fri, 26 May 2023 22:51:39 GMT  
		Size: 16.4 MB (16398977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc5e45939f94b0c37e88a1e2913c16e16e413c75359344c965715a17fbf6a60`  
		Last Modified: Fri, 26 May 2023 22:51:36 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec63addd3bc118ba863355a8eca288122d32cab485c9ccc9228a93c151fc8805`  
		Last Modified: Fri, 26 May 2023 22:51:36 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a314790488f3830db5baf454b6eee4768f01ee44033dc256940f741b974f90b`  
		Last Modified: Fri, 26 May 2023 22:51:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97b6f470a4493f86aee2e25288ed797adc330d4516c73712eaccfdb7f60b7e1`  
		Last Modified: Fri, 26 May 2023 22:51:59 GMT  
		Size: 7.0 MB (7025237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6b089fd04dd79b1b177e6416cfe32513219a399074e7e1c1ff5dc5660a76ec`  
		Last Modified: Fri, 26 May 2023 22:51:58 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3580870ab4aaaba86a2de0643be9b13a4d2ff506b82b4c6effadf8b3bcb53f2b`  
		Last Modified: Fri, 26 May 2023 22:52:05 GMT  
		Size: 54.2 MB (54155492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d2ee3b805d54fd9f82f25d6c1d36ec1e1dde24d64456efed0b2b0a01e8db31`  
		Last Modified: Wed, 31 May 2023 17:20:24 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237fc1405c9d425f562605b5576b1ffd52552ffbfc188843a4f5c8c4a2f335f`  
		Last Modified: Wed, 31 May 2023 17:20:24 GMT  
		Size: 2.8 KB (2794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765539a95d4376d87aec41ed85a62d0e8af256c6827fa18c3ded966356b80e1`  
		Last Modified: Wed, 31 May 2023 17:20:49 GMT  
		Size: 1.4 MB (1362360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450cdae0acb83ccac0b8bbf7cf2776c08f2ea07c7b0c8f2d07075843dad2311d`  
		Last Modified: Wed, 31 May 2023 17:20:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3d0fe52d71eb172f52f1952ae266828e8c4eaa6a04d43f3267ed77b4fb7cb6`  
		Last Modified: Wed, 31 May 2023 17:20:49 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc4ece160298bd35fa55f410c418b2af5a1cec1cb156c5cbbdfe4f9ce31affa`  
		Last Modified: Wed, 31 May 2023 17:20:52 GMT  
		Size: 20.6 MB (20648106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29ab32eb61dd1f33cd959fdb5701df6f8ee013034105ae2f6e3223aaff85663`  
		Last Modified: Wed, 31 May 2023 17:20:49 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e2fda7ae85e9dcd285c9be6b9c6ffe8601d3a40d0ba4e3eb10a990905cfb14f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134098672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d244a8c866fd5fa51b3127e77380a6b57257dbc52210edfee7fb85a74375780`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Tue, 13 Jun 2023 17:05:42 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
ENV DOCKER_VERSION=24.0.2
# Tue, 13 Jun 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
ENV DOCKER_BUILDX_VERSION=0.11.0
# Tue, 13 Jun 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-amd64'; 			sha256='ec2c9da22c3b733ad96d6a6897750153d884f1b2b86f2864ee5f743ce931055d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm-v6'; 			sha256='a925462288a55b709a42431fe39bb0e67f033961f02a4754897c4a388355feea'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm-v7'; 			sha256='e3f18a0d10346d8e53aff743fccfc0b95e45dc0235c3b0b72b49d3452c72b9e0'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-arm64'; 			sha256='e50f34f8feb7004407f826a375090bec6191891c473347b41b05cf5864bc5240'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-ppc64le'; 			sha256='de8670ab6b2c34feb32289d04af07014bb4517de879d1fdb6e31a00da28f1df4'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-riscv64'; 			sha256='a07ad5791d6e60094e38147ef5f5eac406b2692aa380eae5ac866bde91bcdc89'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.0/buildx-v0.11.0.linux-s390x'; 			sha256='fc1a57b9fb69f7736908bbea94013eb17b5ae03cd5ed99b0bd61e223f9b6e4a7'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Tue, 13 Jun 2023 17:05:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 13 Jun 2023 17:05:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 13 Jun 2023 17:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 17:05:42 GMT
CMD ["sh"]
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 30 May 2023 23:05:39 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 30 May 2023 23:05:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 30 May 2023 23:05:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 May 2023 23:05:39 GMT
VOLUME [/var/lib/docker]
# Tue, 30 May 2023 23:05:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 30 May 2023 23:05:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 30 May 2023 23:05:39 GMT
CMD []
# Fri, 26 May 2023 11:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 26 May 2023 11:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 26 May 2023 11:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf127bdc9f4f627525a187a7bf41c41f4706220fb1fe5b5c7d6cbc52114a9224`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 2.0 MB (2024535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b4810136f4ceecd47a02cbf6a0c55b8d9de3b014cf917ac2bf8ee632787ba0`  
		Last Modified: Thu, 11 May 2023 19:42:22 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1937eecd14a9231bd894a45b45eb86cd8745d7ded25c6306665048ab97a59c`  
		Last Modified: Fri, 26 May 2023 19:40:20 GMT  
		Size: 15.4 MB (15422650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c82755bf3f4aff8917107870c8820dd68df0f1f302c2736cb2579e878b3dfb`  
		Last Modified: Tue, 13 Jun 2023 22:30:43 GMT  
		Size: 15.8 MB (15758029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfeff40576576de275415134456f7e8ebe94ce3e3cfb1bc9c2fb06fcb241979b`  
		Last Modified: Tue, 13 Jun 2023 22:30:44 GMT  
		Size: 14.9 MB (14861194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebb707686e22de47f65174db3e1c20fcb05a290fe2b35ca1b67dbc96708beac`  
		Last Modified: Tue, 13 Jun 2023 22:30:42 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f0c567ee27c96c40e29f38b6644d3167d80ecc04e5083c7f639ec926059685`  
		Last Modified: Tue, 13 Jun 2023 22:30:42 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de25efff2e6a6722af58bf9a66595434caed36afa6131d194f78983d539b7cf`  
		Last Modified: Tue, 13 Jun 2023 22:30:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cf1065be68a8a8a3c0db811922e2f03de63018fab0799cb3925a2da7026e04`  
		Last Modified: Tue, 13 Jun 2023 22:30:58 GMT  
		Size: 9.4 MB (9359488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8de9cd3eb5c76885879c6fca5ebe4c046b4bc77b002a2d522cf6d5195f4e2`  
		Last Modified: Tue, 13 Jun 2023 22:30:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e69d8d469d631388eb2c5adcdcec1a16ff71f230167837a7a0b17f5f8f666`  
		Last Modified: Tue, 13 Jun 2023 22:31:02 GMT  
		Size: 49.5 MB (49460709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f25ba5767615b1b4bb6144dc4a63b21e74184055986e3bca65b36ebe5f0fc1`  
		Last Modified: Tue, 13 Jun 2023 22:30:57 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc0052abc167fa24b1e6e50a51a42d39787fd2799e9f32ca0979319ad269d49`  
		Last Modified: Tue, 13 Jun 2023 22:30:57 GMT  
		Size: 2.8 KB (2786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ca11611c8aa22913ec2af2ddd8ab6a644d3c6d9d4be91963c6ca3e470d072`  
		Last Modified: Tue, 13 Jun 2023 22:31:29 GMT  
		Size: 1.4 MB (1413248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157bd0565480402f4d8932ab7649b2a556838f1f2f94da31473f14a369f4428b`  
		Last Modified: Tue, 13 Jun 2023 22:31:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec13955e5d0fcc31fe62af69f792aad66fe4ea495ab9f5c4a93eb338c053982d`  
		Last Modified: Tue, 13 Jun 2023 22:31:29 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fe4402c98e3f37ad72b5516ff477da5210168bc86446260a6b3d9425c9c9d`  
		Last Modified: Tue, 13 Jun 2023 22:31:31 GMT  
		Size: 22.4 MB (22447258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6601f24d9b341dc110f53eacb6bbfd716b87bf81897b52abd58bc954574062`  
		Last Modified: Tue, 13 Jun 2023 22:31:29 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
