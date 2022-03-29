<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:20`](#docker20)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20-windowsservercore`](#docker20-windowsservercore)
-	[`docker:20-windowsservercore-1809`](#docker20-windowsservercore-1809)
-	[`docker:20-windowsservercore-ltsc2022`](#docker20-windowsservercore-ltsc2022)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10-windowsservercore-ltsc2022`](#docker2010-windowsservercore-ltsc2022)
-	[`docker:20.10.14`](#docker201014)
-	[`docker:20.10.14-alpine3.15`](#docker201014-alpine315)
-	[`docker:20.10.14-dind`](#docker201014-dind)
-	[`docker:20.10.14-dind-alpine3.15`](#docker201014-dind-alpine315)
-	[`docker:20.10.14-dind-rootless`](#docker201014-dind-rootless)
-	[`docker:20.10.14-git`](#docker201014-git)
-	[`docker:20.10.14-windowsservercore`](#docker201014-windowsservercore)
-	[`docker:20.10.14-windowsservercore-1809`](#docker201014-windowsservercore-1809)
-	[`docker:20.10.14-windowsservercore-ltsc2022`](#docker201014-windowsservercore-ltsc2022)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:20`

```console
$ docker pull docker@sha256:7dad83861f0b28bd6a0b281dc5f72144927b9f8173e388e461c8feba6be20bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:aa4dc93183c9fb765d7cc0711f36b76ef87bea3dd8da75a23db3b4f7c4981cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d65aad428d30878e893e86ddfd74979979b0d2a03894069bab1b118a73370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9f067566960231408895cb3e9624a89075b8686eb1e256764c30722b7e2f6f2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52727829a8a5c9f4af7070ed9e1989de3a18dcc5fdbd1da2b8a3cea534d8624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:e816908591767e57b84fec6b5edb483cfdae5309c2446d2164c4a5bde44f26b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:f298d13e26555aee67cae3fa5a583d46d5b0371af9441d9cac1c32ca3287c536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b4360e0d3d89d8818540cbaf23f53ddf20517464b4c91f7965b9412eab73c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d74f218351f4e28fb0570e6d0d36c122f464720c6ec7ed72f62a4ac3c73bd3b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69843447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99507798763b8d6e8a8b59538c8ee2a4ad0b8d5ef7d5d6643e1c733ce56e3765`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:c31cd994528547d39cca0c316543d48755dd35c84f3aada0cb57555105016a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2f0b85d045b57c599d7e708caf9d8c58c3e89759e2ffefb45bda432297f79215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654d75e6897e0f11556600d5f6d0f726b36d9f218e8a3609d7b0670816300b3b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
# Tue, 29 Mar 2022 16:00:19 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 16:00:20 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 16:00:20 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 16:00:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 16:00:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbffe6c06b16254032b389fa3f86818cca4e9a213a119635c91a5e898144a834`  
		Last Modified: Tue, 29 Mar 2022 16:01:43 GMT  
		Size: 1.2 MB (1161977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307c773a4b3a5fde8358db70594c0b2eb70e29cb705abd7a9f5f37e7a8dbcacb`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a39d77abf76ca975b2d7bf4bd8cfd2c64d3cad5bd02b3b9f677bbc27ac608a`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07fe32ef27e29e4dba3ed88d5bef111de510f7be0c2cc8bcafe20c0c62bb82e`  
		Last Modified: Tue, 29 Mar 2022 16:01:45 GMT  
		Size: 19.1 MB (19131836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eb12ffa47b1c5d4d06f6fdace1e2865d2e8ca129b07af04424e73777114d4c`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7de587d995b63425b4259e844f4b7fae2da8aace781cef932a9527543d848276
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cd8574e21f5c51c032be3097f830805605216e2002fc98285c751e5c876d39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
# Tue, 29 Mar 2022 08:26:54 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 08:26:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 08:26:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 08:26:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 08:27:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 08:27:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9cd2d9598f1fe4d3e31f530b587846630feeddf9f81e758bc6e2be58dfee75`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.2 MB (1177968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f04c0a5e9bca029e1cb5248b4a3b240b8076292c568464ebad797be38ccd1b7`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab7129a628a3e4c5ee9c74357935e9145f0a302df09d25c508ba16215018a05`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af21fbff071b5dfc4a65fcfd9c1bd353541f4e0fed929a4a68e3cf594e3c00b5`  
		Last Modified: Tue, 29 Mar 2022 08:28:47 GMT  
		Size: 21.1 MB (21111240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e31c8efa4d57102244c35627faef6bcdf00649b089f2f0a100fdf6d1b2c5c1`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:52fcf561ff6e5b5865d804f64a834dec95be85352d02a2955a88697708aed636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:ad79402c6b21229a146ef1e1f05911342cb25b4dcf2b07de5f9b4f7beb9c78ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eed221e8abe5b945e8d44e012c0650a2f8645b53a4139d30da7985a72fc513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878f73dd8f02d753a4f2990f3e9277024267f002560cacb350e550b19166438`  
		Last Modified: Tue, 29 Mar 2022 16:02:04 GMT  
		Size: 6.8 MB (6824111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc915cbe95f635e80584b41c3d800a495fa492211fe98af0ba24868f73b1522c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70155890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1420a43cf047a2037e665447c200d167cec0cfd12cec229b21eaf5f7d1c9310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:27:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e84da3ac4c997d7b350e908b8516ae22d0523bf8b7c0844b94ae73a7079f50`  
		Last Modified: Tue, 29 Mar 2022 08:29:07 GMT  
		Size: 6.9 MB (6933045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:e975b7c270f2a35f16d48b91e2ab5f0eff84a690da1fcedab97e7157d0b3a5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:6e21edf269ee8beed4808bae91f5cc840ad2a042a19a6eb6de13c97e3053906b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8520b3fc85f5fe47604cbba4353f8b2feda30bcf041e26848bd6d812173f4444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:7dad83861f0b28bd6a0b281dc5f72144927b9f8173e388e461c8feba6be20bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:aa4dc93183c9fb765d7cc0711f36b76ef87bea3dd8da75a23db3b4f7c4981cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d65aad428d30878e893e86ddfd74979979b0d2a03894069bab1b118a73370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9f067566960231408895cb3e9624a89075b8686eb1e256764c30722b7e2f6f2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52727829a8a5c9f4af7070ed9e1989de3a18dcc5fdbd1da2b8a3cea534d8624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:e816908591767e57b84fec6b5edb483cfdae5309c2446d2164c4a5bde44f26b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:f298d13e26555aee67cae3fa5a583d46d5b0371af9441d9cac1c32ca3287c536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b4360e0d3d89d8818540cbaf23f53ddf20517464b4c91f7965b9412eab73c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d74f218351f4e28fb0570e6d0d36c122f464720c6ec7ed72f62a4ac3c73bd3b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69843447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99507798763b8d6e8a8b59538c8ee2a4ad0b8d5ef7d5d6643e1c733ce56e3765`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:c31cd994528547d39cca0c316543d48755dd35c84f3aada0cb57555105016a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2f0b85d045b57c599d7e708caf9d8c58c3e89759e2ffefb45bda432297f79215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654d75e6897e0f11556600d5f6d0f726b36d9f218e8a3609d7b0670816300b3b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
# Tue, 29 Mar 2022 16:00:19 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 16:00:20 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 16:00:20 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 16:00:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 16:00:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbffe6c06b16254032b389fa3f86818cca4e9a213a119635c91a5e898144a834`  
		Last Modified: Tue, 29 Mar 2022 16:01:43 GMT  
		Size: 1.2 MB (1161977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307c773a4b3a5fde8358db70594c0b2eb70e29cb705abd7a9f5f37e7a8dbcacb`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a39d77abf76ca975b2d7bf4bd8cfd2c64d3cad5bd02b3b9f677bbc27ac608a`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07fe32ef27e29e4dba3ed88d5bef111de510f7be0c2cc8bcafe20c0c62bb82e`  
		Last Modified: Tue, 29 Mar 2022 16:01:45 GMT  
		Size: 19.1 MB (19131836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eb12ffa47b1c5d4d06f6fdace1e2865d2e8ca129b07af04424e73777114d4c`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7de587d995b63425b4259e844f4b7fae2da8aace781cef932a9527543d848276
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cd8574e21f5c51c032be3097f830805605216e2002fc98285c751e5c876d39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
# Tue, 29 Mar 2022 08:26:54 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 08:26:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 08:26:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 08:26:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 08:27:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 08:27:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9cd2d9598f1fe4d3e31f530b587846630feeddf9f81e758bc6e2be58dfee75`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.2 MB (1177968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f04c0a5e9bca029e1cb5248b4a3b240b8076292c568464ebad797be38ccd1b7`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab7129a628a3e4c5ee9c74357935e9145f0a302df09d25c508ba16215018a05`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af21fbff071b5dfc4a65fcfd9c1bd353541f4e0fed929a4a68e3cf594e3c00b5`  
		Last Modified: Tue, 29 Mar 2022 08:28:47 GMT  
		Size: 21.1 MB (21111240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e31c8efa4d57102244c35627faef6bcdf00649b089f2f0a100fdf6d1b2c5c1`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:52fcf561ff6e5b5865d804f64a834dec95be85352d02a2955a88697708aed636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:ad79402c6b21229a146ef1e1f05911342cb25b4dcf2b07de5f9b4f7beb9c78ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eed221e8abe5b945e8d44e012c0650a2f8645b53a4139d30da7985a72fc513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878f73dd8f02d753a4f2990f3e9277024267f002560cacb350e550b19166438`  
		Last Modified: Tue, 29 Mar 2022 16:02:04 GMT  
		Size: 6.8 MB (6824111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc915cbe95f635e80584b41c3d800a495fa492211fe98af0ba24868f73b1522c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70155890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1420a43cf047a2037e665447c200d167cec0cfd12cec229b21eaf5f7d1c9310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:27:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e84da3ac4c997d7b350e908b8516ae22d0523bf8b7c0844b94ae73a7079f50`  
		Last Modified: Tue, 29 Mar 2022 08:29:07 GMT  
		Size: 6.9 MB (6933045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:e975b7c270f2a35f16d48b91e2ab5f0eff84a690da1fcedab97e7157d0b3a5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:6e21edf269ee8beed4808bae91f5cc840ad2a042a19a6eb6de13c97e3053906b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8520b3fc85f5fe47604cbba4353f8b2feda30bcf041e26848bd6d812173f4444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `docker:20.10-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14`

```console
$ docker pull docker@sha256:7dad83861f0b28bd6a0b281dc5f72144927b9f8173e388e461c8feba6be20bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.14` - linux; amd64

```console
$ docker pull docker@sha256:aa4dc93183c9fb765d7cc0711f36b76ef87bea3dd8da75a23db3b4f7c4981cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d65aad428d30878e893e86ddfd74979979b0d2a03894069bab1b118a73370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9f067566960231408895cb3e9624a89075b8686eb1e256764c30722b7e2f6f2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52727829a8a5c9f4af7070ed9e1989de3a18dcc5fdbd1da2b8a3cea534d8624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-alpine3.15`

```console
$ docker pull docker@sha256:7dad83861f0b28bd6a0b281dc5f72144927b9f8173e388e461c8feba6be20bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.14-alpine3.15` - linux; amd64

```console
$ docker pull docker@sha256:aa4dc93183c9fb765d7cc0711f36b76ef87bea3dd8da75a23db3b4f7c4981cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d65aad428d30878e893e86ddfd74979979b0d2a03894069bab1b118a73370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9f067566960231408895cb3e9624a89075b8686eb1e256764c30722b7e2f6f2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52727829a8a5c9f4af7070ed9e1989de3a18dcc5fdbd1da2b8a3cea534d8624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-dind`

```console
$ docker pull docker@sha256:e816908591767e57b84fec6b5edb483cfdae5309c2446d2164c4a5bde44f26b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.14-dind` - linux; amd64

```console
$ docker pull docker@sha256:f298d13e26555aee67cae3fa5a583d46d5b0371af9441d9cac1c32ca3287c536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b4360e0d3d89d8818540cbaf23f53ddf20517464b4c91f7965b9412eab73c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d74f218351f4e28fb0570e6d0d36c122f464720c6ec7ed72f62a4ac3c73bd3b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69843447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99507798763b8d6e8a8b59538c8ee2a4ad0b8d5ef7d5d6643e1c733ce56e3765`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-dind-alpine3.15`

```console
$ docker pull docker@sha256:e816908591767e57b84fec6b5edb483cfdae5309c2446d2164c4a5bde44f26b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.14-dind-alpine3.15` - linux; amd64

```console
$ docker pull docker@sha256:f298d13e26555aee67cae3fa5a583d46d5b0371af9441d9cac1c32ca3287c536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b4360e0d3d89d8818540cbaf23f53ddf20517464b4c91f7965b9412eab73c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14-dind-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d74f218351f4e28fb0570e6d0d36c122f464720c6ec7ed72f62a4ac3c73bd3b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69843447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99507798763b8d6e8a8b59538c8ee2a4ad0b8d5ef7d5d6643e1c733ce56e3765`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-dind-rootless`

```console
$ docker pull docker@sha256:c31cd994528547d39cca0c316543d48755dd35c84f3aada0cb57555105016a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.14-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2f0b85d045b57c599d7e708caf9d8c58c3e89759e2ffefb45bda432297f79215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654d75e6897e0f11556600d5f6d0f726b36d9f218e8a3609d7b0670816300b3b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
# Tue, 29 Mar 2022 16:00:19 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 16:00:20 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 16:00:20 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 16:00:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 16:00:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbffe6c06b16254032b389fa3f86818cca4e9a213a119635c91a5e898144a834`  
		Last Modified: Tue, 29 Mar 2022 16:01:43 GMT  
		Size: 1.2 MB (1161977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307c773a4b3a5fde8358db70594c0b2eb70e29cb705abd7a9f5f37e7a8dbcacb`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a39d77abf76ca975b2d7bf4bd8cfd2c64d3cad5bd02b3b9f677bbc27ac608a`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07fe32ef27e29e4dba3ed88d5bef111de510f7be0c2cc8bcafe20c0c62bb82e`  
		Last Modified: Tue, 29 Mar 2022 16:01:45 GMT  
		Size: 19.1 MB (19131836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eb12ffa47b1c5d4d06f6fdace1e2865d2e8ca129b07af04424e73777114d4c`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7de587d995b63425b4259e844f4b7fae2da8aace781cef932a9527543d848276
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cd8574e21f5c51c032be3097f830805605216e2002fc98285c751e5c876d39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
# Tue, 29 Mar 2022 08:26:54 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 08:26:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 08:26:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 08:26:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 08:27:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 08:27:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9cd2d9598f1fe4d3e31f530b587846630feeddf9f81e758bc6e2be58dfee75`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.2 MB (1177968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f04c0a5e9bca029e1cb5248b4a3b240b8076292c568464ebad797be38ccd1b7`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab7129a628a3e4c5ee9c74357935e9145f0a302df09d25c508ba16215018a05`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af21fbff071b5dfc4a65fcfd9c1bd353541f4e0fed929a4a68e3cf594e3c00b5`  
		Last Modified: Tue, 29 Mar 2022 08:28:47 GMT  
		Size: 21.1 MB (21111240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e31c8efa4d57102244c35627faef6bcdf00649b089f2f0a100fdf6d1b2c5c1`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-git`

```console
$ docker pull docker@sha256:52fcf561ff6e5b5865d804f64a834dec95be85352d02a2955a88697708aed636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.14-git` - linux; amd64

```console
$ docker pull docker@sha256:ad79402c6b21229a146ef1e1f05911342cb25b4dcf2b07de5f9b4f7beb9c78ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eed221e8abe5b945e8d44e012c0650a2f8645b53a4139d30da7985a72fc513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878f73dd8f02d753a4f2990f3e9277024267f002560cacb350e550b19166438`  
		Last Modified: Tue, 29 Mar 2022 16:02:04 GMT  
		Size: 6.8 MB (6824111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc915cbe95f635e80584b41c3d800a495fa492211fe98af0ba24868f73b1522c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70155890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1420a43cf047a2037e665447c200d167cec0cfd12cec229b21eaf5f7d1c9310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:27:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e84da3ac4c997d7b350e908b8516ae22d0523bf8b7c0844b94ae73a7079f50`  
		Last Modified: Tue, 29 Mar 2022 08:29:07 GMT  
		Size: 6.9 MB (6933045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-windowsservercore`

```console
$ docker pull docker@sha256:e975b7c270f2a35f16d48b91e2ab5f0eff84a690da1fcedab97e7157d0b3a5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `docker:20.10.14-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.14-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-windowsservercore-1809`

```console
$ docker pull docker@sha256:6e21edf269ee8beed4808bae91f5cc840ad2a042a19a6eb6de13c97e3053906b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `docker:20.10.14-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.14-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8520b3fc85f5fe47604cbba4353f8b2feda30bcf041e26848bd6d812173f4444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `docker:20.10.14-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:e816908591767e57b84fec6b5edb483cfdae5309c2446d2164c4a5bde44f26b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:f298d13e26555aee67cae3fa5a583d46d5b0371af9441d9cac1c32ca3287c536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76137277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337b4360e0d3d89d8818540cbaf23f53ddf20517464b4c91f7965b9412eab73c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d74f218351f4e28fb0570e6d0d36c122f464720c6ec7ed72f62a4ac3c73bd3b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69843447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99507798763b8d6e8a8b59538c8ee2a4ad0b8d5ef7d5d6643e1c733ce56e3765`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:c31cd994528547d39cca0c316543d48755dd35c84f3aada0cb57555105016a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2f0b85d045b57c599d7e708caf9d8c58c3e89759e2ffefb45bda432297f79215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654d75e6897e0f11556600d5f6d0f726b36d9f218e8a3609d7b0670816300b3b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 16:00:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:14 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 16:00:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 16:00:15 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:15 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 16:00:15 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 16:00:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:16 GMT
CMD []
# Tue, 29 Mar 2022 16:00:19 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 16:00:20 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 16:00:20 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 16:00:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 16:00:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 16:00:24 GMT
USER rootless
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd3af411b22620487b010d6a0173f523f90e4c3002aa258b686d777526a4f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:21 GMT  
		Size: 6.7 MB (6734756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8df0982966c01b95064e7b7ad18684f0110d00514408e00e8eba5bda95d97`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e43d81c122840bbeb22c6eae35078742fbb992bf3d96e48e2ee6d4f53f78f8`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5aeec5230d59fd6d941185b5450ad9e1e7b35cb3ac695854a750b13e009e3d`  
		Last Modified: Tue, 29 Mar 2022 16:01:20 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbffe6c06b16254032b389fa3f86818cca4e9a213a119635c91a5e898144a834`  
		Last Modified: Tue, 29 Mar 2022 16:01:43 GMT  
		Size: 1.2 MB (1161977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307c773a4b3a5fde8358db70594c0b2eb70e29cb705abd7a9f5f37e7a8dbcacb`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a39d77abf76ca975b2d7bf4bd8cfd2c64d3cad5bd02b3b9f677bbc27ac608a`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07fe32ef27e29e4dba3ed88d5bef111de510f7be0c2cc8bcafe20c0c62bb82e`  
		Last Modified: Tue, 29 Mar 2022 16:01:45 GMT  
		Size: 19.1 MB (19131836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eb12ffa47b1c5d4d06f6fdace1e2865d2e8ca129b07af04424e73777114d4c`  
		Last Modified: Tue, 29 Mar 2022 16:01:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7de587d995b63425b4259e844f4b7fae2da8aace781cef932a9527543d848276
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cd8574e21f5c51c032be3097f830805605216e2002fc98285c751e5c876d39`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:26:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 29 Mar 2022 08:26:38 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:39 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 29 Mar 2022 08:26:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 29 Mar 2022 08:26:42 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:42 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Mar 2022 08:26:43 GMT
EXPOSE 2375 2376
# Tue, 29 Mar 2022 08:26:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:45 GMT
CMD []
# Tue, 29 Mar 2022 08:26:54 GMT
RUN apk add --no-cache iproute2
# Tue, 29 Mar 2022 08:26:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 29 Mar 2022 08:26:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 29 Mar 2022 08:26:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 29 Mar 2022 08:26:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 29 Mar 2022 08:27:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Mar 2022 08:27:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d864000173cc86daa6e55100b01d994be24f6b8c559c5e76ef99bde7be746d`  
		Last Modified: Tue, 29 Mar 2022 08:28:23 GMT  
		Size: 6.6 MB (6615610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9335a5b964e837fcf57af4a0bb908694439e5c2353921af801ef7bf8c6e85a`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0095e6dad21f8818c0137577f1ca43ac3aec53dea5ae540842f0aa5f3876e78`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e754d309d56b8d770f6b3859fc6c3996c840f31decd785e6c644d432c93ab458`  
		Last Modified: Tue, 29 Mar 2022 08:28:22 GMT  
		Size: 2.7 KB (2745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9cd2d9598f1fe4d3e31f530b587846630feeddf9f81e758bc6e2be58dfee75`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.2 MB (1177968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f04c0a5e9bca029e1cb5248b4a3b240b8076292c568464ebad797be38ccd1b7`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab7129a628a3e4c5ee9c74357935e9145f0a302df09d25c508ba16215018a05`  
		Last Modified: Tue, 29 Mar 2022 08:28:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af21fbff071b5dfc4a65fcfd9c1bd353541f4e0fed929a4a68e3cf594e3c00b5`  
		Last Modified: Tue, 29 Mar 2022 08:28:47 GMT  
		Size: 21.1 MB (21111240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e31c8efa4d57102244c35627faef6bcdf00649b089f2f0a100fdf6d1b2c5c1`  
		Last Modified: Tue, 29 Mar 2022 08:28:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:52fcf561ff6e5b5865d804f64a834dec95be85352d02a2955a88697708aed636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:ad79402c6b21229a146ef1e1f05911342cb25b4dcf2b07de5f9b4f7beb9c78ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76221613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eed221e8abe5b945e8d44e012c0650a2f8645b53a4139d30da7985a72fc513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 16:00:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878f73dd8f02d753a4f2990f3e9277024267f002560cacb350e550b19166438`  
		Last Modified: Tue, 29 Mar 2022 16:02:04 GMT  
		Size: 6.8 MB (6824111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dc915cbe95f635e80584b41c3d800a495fa492211fe98af0ba24868f73b1522c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70155890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1420a43cf047a2037e665447c200d167cec0cfd12cec229b21eaf5f7d1c9310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
# Tue, 29 Mar 2022 08:27:09 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e84da3ac4c997d7b350e908b8516ae22d0523bf8b7c0844b94ae73a7079f50`  
		Last Modified: Tue, 29 Mar 2022 08:29:07 GMT  
		Size: 6.9 MB (6933045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:7dad83861f0b28bd6a0b281dc5f72144927b9f8173e388e461c8feba6be20bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:aa4dc93183c9fb765d7cc0711f36b76ef87bea3dd8da75a23db3b4f7c4981cd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69397502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3d65aad428d30878e893e86ddfd74979979b0d2a03894069bab1b118a73370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 15:59:59 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 15:59:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 15:59:59 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 16:00:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 16:00:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 16:00:07 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 16:00:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 16:00:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 16:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 16:00:07 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6755b13d2d75e21ca54152b606f7ad8b3f521d89f495bace00c594084e80c1c`  
		Last Modified: Tue, 29 Mar 2022 16:00:52 GMT  
		Size: 2.0 MB (1969529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426f946f707af38e61b744a86edb34657d8084fcff1544399a62e3bfa3f43bb`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15b211fd3b69e972a7694bcb6aa96f823c95cb72eca2907c812dd45a2d5fa6`  
		Last Modified: Tue, 29 Mar 2022 16:01:01 GMT  
		Size: 64.6 MB (64611600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c17c6257b1a3de99e7fe88316daff2f3671c17786d5608fdf3f961098db87`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd4cb587535a3828c0d5bfbc077f924bcf57c15c219d287eb1cd2bd6f48ba91`  
		Last Modified: Tue, 29 Mar 2022 16:00:49 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0012ebcf146c81dfe7edc4f75e810369ef7787290d0b0e20ab7987ebef9e7861`  
		Last Modified: Tue, 29 Mar 2022 16:00:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:9f067566960231408895cb3e9624a89075b8686eb1e256764c30722b7e2f6f2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52727829a8a5c9f4af7070ed9e1989de3a18dcc5fdbd1da2b8a3cea534d8624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 29 Mar 2022 08:26:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 08:26:15 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 29 Mar 2022 08:26:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 29 Mar 2022 08:26:23 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 29 Mar 2022 08:26:24 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 29 Mar 2022 08:26:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Mar 2022 08:26:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 29 Mar 2022 08:26:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Mar 2022 08:26:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8992fcbba1f8070f63d991ae72bed38408b25db7ffa00f7221352fe9275c5`  
		Last Modified: Tue, 29 Mar 2022 08:27:55 GMT  
		Size: 1.9 MB (1938918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedb10a1343d3055a1a213063d8f8f6ea1882b01069a44faf0453b0041a802d`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f3009765e88f09be3c6e87a57258d5bea877cf248e4b0a6acd198692f300ef`  
		Last Modified: Tue, 29 Mar 2022 08:28:02 GMT  
		Size: 58.6 MB (58565750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae115253e7c71f61aa1bcdfde46cc38e0de6c3fb34bf4d1cebeca0b9bc91cc4`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3afcdfd642c0cd2ac3c0e03dfccaf3352874a7ccf06e91ce2e8c9d5a5a513`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971d2cdfcd569d13d88d038acf7b68fdc926a532b0f7e7480c3c80ebcf05bd31`  
		Last Modified: Tue, 29 Mar 2022 08:27:52 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e975b7c270f2a35f16d48b91e2ab5f0eff84a690da1fcedab97e7157d0b3a5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `docker:windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:6e21edf269ee8beed4808bae91f5cc840ad2a042a19a6eb6de13c97e3053906b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull docker@sha256:034598e549b6c0f2bb1ff47cbb638cb9785ab1456144eb4c0da198e075e70a9d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769426444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2374652d04922dbe838fbdac11dc741534c504b1213d1110bcf7ab3ce0075be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:57:30 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:16:22 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:16:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:17:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc556e75fc2ee0a56749fd9ec604591d58c7dcfbf6ddd1389aedfe0faa926127`  
		Last Modified: Wed, 09 Mar 2022 19:00:27 GMT  
		Size: 353.8 KB (353787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a37839ee100e0b4b77379ec17ab118f0b377c9d7f73de9b4fdfce26e5910d07`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a35b5cdb293ca7295865a746b962b396382293a16a843862f866ad76d49b7d`  
		Last Modified: Thu, 24 Mar 2022 05:18:49 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791bcb5d614f3fbb4d6ff0b29ce1877c53e05d3b8536fe0fa4b549f20c0b6730`  
		Last Modified: Thu, 24 Mar 2022 05:19:47 GMT  
		Size: 53.6 MB (53615927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8520b3fc85f5fe47604cbba4353f8b2feda30bcf041e26848bd6d812173f4444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull docker@sha256:aefae8d2bf575204b17f88589c7741c350281048d96844f9fd3316a80ec2940e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275653601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723b6471c336c441aa997a1c5d0672ef1de87fe45687edb769c52bd0edce4e81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:55:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 24 Mar 2022 05:15:29 GMT
ENV DOCKER_VERSION=20.10.14
# Thu, 24 Mar 2022 05:15:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.14.zip
# Thu, 24 Mar 2022 05:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfaa4c2639ecdc27410a570e2dcb2efe02bcbec37d6ad750d15a97aac6990236`  
		Last Modified: Wed, 09 Mar 2022 18:59:14 GMT  
		Size: 598.3 KB (598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0181d328453c16ef4bf5dfa86a118c96a8325d7a3e58637e504f5425c5ea7ae2`  
		Last Modified: Thu, 24 Mar 2022 05:18:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e48a2566f0d50346970f29a77bd1cbfde2d33a34fc25d9227a8900f494b136a`  
		Last Modified: Thu, 24 Mar 2022 05:18:24 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cd9d001a2232e2f5406882e91758565fec1809573168d4e31cafa909ea5d4f`  
		Last Modified: Thu, 24 Mar 2022 05:18:35 GMT  
		Size: 53.8 MB (53804106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
