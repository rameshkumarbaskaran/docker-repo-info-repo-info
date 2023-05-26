## `docker:dind`

```console
$ docker pull docker@sha256:52e59bcbda099e0877cc7bf7fc7a0895df4075a3695e64b83aa18fa670ef1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:22679c5c3a1967133f1e817c3ba187024375205d1ef084be7aecf6b0d4599c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115370841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d614d42cf981bd9981fad62de07de3687a1076092a884c394fc5c7ad5d92dbb8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Mon, 22 May 2023 23:05:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 22 May 2023 23:05:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 22 May 2023 23:05:39 GMT
ENV DOCKER_VERSION=24.0.1
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 22 May 2023 23:05:39 GMT
ENV DOCKER_BUILDX_VERSION=0.10.5
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-amd64'; 			sha256='2f1995ee6c4e7d75668ff38242ce3381da71bd30a8ca1f648f077b0a066c742b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-arm-v6'; 			sha256='cd8d8b3fe02b07d60d323af27da53c72c35516e7c8a52e649e3a68582e113e76'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-arm-v7'; 			sha256='a10b60d9c541b30c8f46ed2c8e671c1c775125d6b71ff0b1787204c11ae84ba9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-arm64'; 			sha256='a60d2dfb46cbe66e7fa75c8fd4fc730bcf052e08b8e236df254c24600db388a9'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-ppc64le'; 			sha256='1c1ac2bcad35a7d423e093bceba04e3f0d3f4381e534b64e1fb67e0dc932c973'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-riscv64'; 			sha256='f2da6e8ac73b00bafac1f4ecd76e126e8a3f6740adfcd04fbad0094d30274a55'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.10.5/buildx-v0.10.5.linux-s390x'; 			sha256='9a64f9248a8fa6d5b114d5599018814a1fc950f1910aa73e4fb9d012ca9bcbe6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 22 May 2023 23:05:39 GMT
ENV DOCKER_COMPOSE_VERSION=2.18.1
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-x86_64'; 			sha256='b4e6aff14c30f82ce26e94d37686b5598b3f870ce1e053927c853b4f4b128575'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv6'; 			sha256='34430890fe8ab68fe091a2907ebff174d1d6dcfc3d4e87f8c50bb105a2ac8b5f'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-armv7'; 			sha256='cced34fc17c3689b5e0760b115ef481014eb004370a7b9380fc25eeef55570bb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-aarch64'; 			sha256='6d1784542f74806ef0ed4e798d31c91604453eb06b86448b4c60d7df5d5b7afb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-ppc64le'; 			sha256='baa21ead951f0b0a0dc191e4dc7718e584961d0fcbb5969004bdcf1950203cde'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-riscv64'; 			sha256='2e84879a8677bcebda18d7772a86fa107f3745ba693f7c9c397b9fede355e3f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-linux-s390x'; 			sha256='e8d5669b5f11212310d080d239348fe293b783c7357bb1085728fbed69e519c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 22 May 2023 23:05:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 22 May 2023 23:05:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 May 2023 23:05:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 22 May 2023 23:05:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 22 May 2023 23:05:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 May 2023 23:05:39 GMT
CMD ["sh"]
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 22 May 2023 23:05:39 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Mon, 22 May 2023 23:05:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 22 May 2023 23:05:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 May 2023 23:05:39 GMT
VOLUME [/var/lib/docker]
# Mon, 22 May 2023 23:05:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 22 May 2023 23:05:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 22 May 2023 23:05:39 GMT
CMD []
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
	-	`sha256:75039dcfa57a7b4e9405dbd4aa6d212ea4202c813e54a727ccd1e54d545afc28`  
		Last Modified: Sat, 20 May 2023 00:20:31 GMT  
		Size: 16.4 MB (16376152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a867a08cc62aba90b08b1da3ef9ec49bc28d26e61fe5d11dd876855dc8e85b2a`  
		Last Modified: Tue, 23 May 2023 01:29:04 GMT  
		Size: 16.0 MB (16003304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f897c97d93d5c3e3a47e69b213f3b39c2593c7c49f4c0b49e79f2a34bceab398`  
		Last Modified: Tue, 23 May 2023 01:29:04 GMT  
		Size: 16.4 MB (16398969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5893dfdf02699e20fb56be75a304867d4fec743b9eac91f0a063a5cb09cdfe24`  
		Last Modified: Tue, 23 May 2023 01:29:01 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd0f5addfbf9728ca04b0dea382dc8e4b950648089413635c64277f0bfc44b2`  
		Last Modified: Tue, 23 May 2023 01:29:02 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3364461d2a2d8174b06d66820c387e9f5e2b1d551114d865ee58292a6313f81`  
		Last Modified: Tue, 23 May 2023 01:29:02 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b63b390fabeb872b583734d1517576a6318107fc70d9c713765732d33dda261`  
		Last Modified: Tue, 23 May 2023 01:29:19 GMT  
		Size: 7.0 MB (7025225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200a256d559fb8adfa83be30ad368d83212bd98330aa37b171415be89ea9b0d1`  
		Last Modified: Tue, 23 May 2023 01:29:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36549cf8e4b803d03ea7f6c3926d54f3479a5591686a4f60437c5e381d00d22`  
		Last Modified: Tue, 23 May 2023 01:29:25 GMT  
		Size: 54.1 MB (54148363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135f01648aa4bd90a15ab5392d49ed1504f2927999f4fae1a947ac73a0bc0e28`  
		Last Modified: Tue, 23 May 2023 01:29:18 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9804e6a84f9c66c5cf3770c679b656ff06839fb9f5b809483e821f128c06c17`  
		Last Modified: Tue, 23 May 2023 01:29:18 GMT  
		Size: 2.8 KB (2789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e7dd654551e93a8f676283d8220f0917c8c178fa1aece5988f9206989ab69f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106806073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378262559e310b63d3a4c5e9fc402778a918bf46648a7b5d984073aedd658628`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
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
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 26 May 2023 11:04:23 GMT
ENV DIND_COMMIT=1f32e3c95d72a29b3eaacba156ed675dba976cb5
# Fri, 26 May 2023 11:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 26 May 2023 11:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 May 2023 11:04:23 GMT
VOLUME [/var/lib/docker]
# Fri, 26 May 2023 11:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 26 May 2023 11:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 26 May 2023 11:04:23 GMT
CMD []
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
	-	`sha256:db6263205561a1ecc9c81481e25134ce8146f462b6e7b0b751272bc1a0650044`  
		Last Modified: Fri, 26 May 2023 19:40:19 GMT  
		Size: 14.4 MB (14442049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39314cee2a9c080db124e84ec45013ce82a68172249fc85d38fb9597a76394df`  
		Last Modified: Fri, 26 May 2023 19:40:19 GMT  
		Size: 14.9 MB (14861192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ee298bff01dbaf777899acfee9f3d9698906fc761563fe9e5f4acb40df8c4d`  
		Last Modified: Fri, 26 May 2023 19:40:17 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fda9acfdd9011e51bd57574020d2a7217a64f9464a25b3253f8158e0d87fc60`  
		Last Modified: Fri, 26 May 2023 19:40:17 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a277f3b8dc15fa5d2b731d9bce30bf93abefeffc8469f4bac4786543d7cc4`  
		Last Modified: Fri, 26 May 2023 19:40:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b761764eaff7515457aafb85a2d7520751bf26b6b8b08b331b04622da656006c`  
		Last Modified: Fri, 26 May 2023 19:40:38 GMT  
		Size: 7.2 MB (7245077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b49e70f544e3288c618562f9e01149361b1213c85f7f1500ce61510c5afd79`  
		Last Modified: Fri, 26 May 2023 19:40:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262f260c9231d6d77a6f9d540bed2d9b19f76f3be39cf3001c75d0ac5a9ebf9f`  
		Last Modified: Fri, 26 May 2023 19:40:43 GMT  
		Size: 49.5 MB (49460732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3263c4f34c93f014ce7073fb19850a9b70aab4ef2061f52315a6e88c3700572`  
		Last Modified: Fri, 26 May 2023 19:40:36 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e6daf4fc04535ef402ae603768e53c096612da6469f0e7d8380c7b0ebe33a8`  
		Last Modified: Fri, 26 May 2023 19:40:37 GMT  
		Size: 2.8 KB (2791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
