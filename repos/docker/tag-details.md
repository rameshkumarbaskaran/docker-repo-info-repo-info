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
-	[`docker:20.10.12`](#docker201012)
-	[`docker:20.10.12-alpine3.15`](#docker201012-alpine315)
-	[`docker:20.10.12-dind`](#docker201012-dind)
-	[`docker:20.10.12-dind-alpine3.15`](#docker201012-dind-alpine315)
-	[`docker:20.10.12-dind-rootless`](#docker201012-dind-rootless)
-	[`docker:20.10.12-git`](#docker201012-git)
-	[`docker:20.10.12-windowsservercore`](#docker201012-windowsservercore)
-	[`docker:20.10.12-windowsservercore-1809`](#docker201012-windowsservercore-1809)
-	[`docker:20.10.12-windowsservercore-ltsc2022`](#docker201012-windowsservercore-ltsc2022)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:20`

```console
$ docker pull docker@sha256:a729cce205a05b0b86dc8dca87823efaffc3f74979fe7dc86a707c2fbf631b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:b15efb5c932fd29acc764a2b8c0e6b1dfda4450f2a67d630c3b9f205785fdb2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68519144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a9bc7c6340df2ac9d6c8196ca1d905180ddf2ca8b29a8d98f5422e2e5ccf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:17db01f277a58c2d70b2a40a8f46607c5319dd2f23c55dcf8c835cd25f7ff746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62414023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4610f8d36c6766d145891417dd49f9b3e6535b43820bae79640d380fb88016b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:6f2ae4a5fd85ccf85cdd829057a34ace894d25d544e5e4d9f2e7109297fedf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:d848d730231a7e8303e538515251f95cfb6ce86ea7385c9d1bfae7cfd7eff179
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75258270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42336ff683d7dadd320ea6fe9d93a5b101474346302d23f96c9b4546cb414d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af0ce9eee4461072754e6f35f18c219ca6981a16c0042c92bbb4823ce753faa2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be435b54cd392da632ac2c026657537d6559f9a9faf496f22bb1ef7f9a97ea17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:a0e30641697ca722c68a26b104cb271c8f1d1bd9ec3431b06c1c31fe32d06709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab2f198889709d2a8c96373c713802ebf718c3d607a5d865339a07fde1351c9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95554039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669719fc32513aae9029a1f8d6de49809af5919a32f08db35e2af61583ef8e19`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
# Fri, 21 Jan 2022 20:33:40 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 20:33:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 20:33:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 20:33:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 20:33:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd98d5908761c9c209aa32ce13b48a2d08571f9259b80a7836bc1f64d1a20d`  
		Last Modified: Fri, 21 Jan 2022 20:34:35 GMT  
		Size: 1.2 MB (1162100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e732110c5c1fe0503e484447374f44fe316487faddd706b7677bef3e7277e61`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73db87b0b5a8a0bc668e24b62e413a751187f963dfe522339421ea6a935ee853`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ab341e7115cfdbece6bf8c6fd568a926610ee00aff041ca3022c00d8a10c8`  
		Last Modified: Fri, 21 Jan 2022 20:34:38 GMT  
		Size: 19.1 MB (19131944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b72a872f74ab4930415afca7a1e77c9db132369ea883da4d8698083f8052d3`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d907b9c8ef192ace2c0e03da806d502d75197c4757243a2847b93d6c18ddb0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91316467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d79195eb6e0317cec176cf13daddf6e000c65a7c0fde8ff2cfde11466fe479`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
# Fri, 21 Jan 2022 21:02:11 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 21:02:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 21:02:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 21:02:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 21:02:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 21:02:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 21:02:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72da0b456f787fdd5045043a954f4535d6dc5fd25623135462e686af51fac330`  
		Last Modified: Fri, 21 Jan 2022 21:03:29 GMT  
		Size: 1.2 MB (1178052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aa8cb2a0b40b6a14458bda499fcfce021f46654814f2055fa7c5a464fbb5d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed441dcdb345cac707a1852c447bf8572017ab247e0ecd8cdac11dd173b718`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54ab9c013e77879ef7a63b0d40774c705e03213cb7627df975b1f544aab723`  
		Last Modified: Fri, 21 Jan 2022 21:03:32 GMT  
		Size: 21.1 MB (21105215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0202deee6aed51b38517aa88783c08700bb12b4f9c59308dbf266a972dc233d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:fe99b62ceb53a90c054c55e86440cf00d13b3ff2f3d99692a0bef4adc1b45c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:44c9a5a828003f5276a952052dc4999b98b0243d0dd1bd7c8e85ea38352077b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75342928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456c635446977ad70607efd5889908b1ccb8b727ae6244dca0569b72c2b63ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:58 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c28794b3e25128706cf6faa48515b023ea6f2d7bfacfe6493fa40b2f1436f1`  
		Last Modified: Wed, 15 Dec 2021 20:21:43 GMT  
		Size: 6.8 MB (6823784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90c29958713df30b15a09c261d26cafc66bab0b23247300298267ef7f066fa67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69346856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab607b2188f06d49d5e0544631eb76703f41790b8928653d0ddb72808181c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:40:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ec878c950532925c0e2a1d397edf1086a25b91f4af6344e9b56a4dbb000c9`  
		Last Modified: Wed, 15 Dec 2021 19:42:24 GMT  
		Size: 6.9 MB (6932833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:ebd5f6aeb57f0cfbb1500c6b5d373ae5de43a098d14e2c107d2e241c3f9d6315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `docker:20-windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:5fd3cd170a59dbb1d11c44c7369f9f7127a8df53ff91167fa063a1c0cbf3a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b623a541075d3ced662fc1f7b5df6eebb524a04efa65353ad5e468d97a42fa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `docker:20-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:a729cce205a05b0b86dc8dca87823efaffc3f74979fe7dc86a707c2fbf631b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:b15efb5c932fd29acc764a2b8c0e6b1dfda4450f2a67d630c3b9f205785fdb2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68519144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a9bc7c6340df2ac9d6c8196ca1d905180ddf2ca8b29a8d98f5422e2e5ccf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:17db01f277a58c2d70b2a40a8f46607c5319dd2f23c55dcf8c835cd25f7ff746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62414023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4610f8d36c6766d145891417dd49f9b3e6535b43820bae79640d380fb88016b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:6f2ae4a5fd85ccf85cdd829057a34ace894d25d544e5e4d9f2e7109297fedf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:d848d730231a7e8303e538515251f95cfb6ce86ea7385c9d1bfae7cfd7eff179
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75258270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42336ff683d7dadd320ea6fe9d93a5b101474346302d23f96c9b4546cb414d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af0ce9eee4461072754e6f35f18c219ca6981a16c0042c92bbb4823ce753faa2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be435b54cd392da632ac2c026657537d6559f9a9faf496f22bb1ef7f9a97ea17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:a0e30641697ca722c68a26b104cb271c8f1d1bd9ec3431b06c1c31fe32d06709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab2f198889709d2a8c96373c713802ebf718c3d607a5d865339a07fde1351c9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95554039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669719fc32513aae9029a1f8d6de49809af5919a32f08db35e2af61583ef8e19`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
# Fri, 21 Jan 2022 20:33:40 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 20:33:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 20:33:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 20:33:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 20:33:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd98d5908761c9c209aa32ce13b48a2d08571f9259b80a7836bc1f64d1a20d`  
		Last Modified: Fri, 21 Jan 2022 20:34:35 GMT  
		Size: 1.2 MB (1162100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e732110c5c1fe0503e484447374f44fe316487faddd706b7677bef3e7277e61`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73db87b0b5a8a0bc668e24b62e413a751187f963dfe522339421ea6a935ee853`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ab341e7115cfdbece6bf8c6fd568a926610ee00aff041ca3022c00d8a10c8`  
		Last Modified: Fri, 21 Jan 2022 20:34:38 GMT  
		Size: 19.1 MB (19131944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b72a872f74ab4930415afca7a1e77c9db132369ea883da4d8698083f8052d3`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d907b9c8ef192ace2c0e03da806d502d75197c4757243a2847b93d6c18ddb0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91316467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d79195eb6e0317cec176cf13daddf6e000c65a7c0fde8ff2cfde11466fe479`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
# Fri, 21 Jan 2022 21:02:11 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 21:02:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 21:02:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 21:02:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 21:02:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 21:02:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 21:02:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72da0b456f787fdd5045043a954f4535d6dc5fd25623135462e686af51fac330`  
		Last Modified: Fri, 21 Jan 2022 21:03:29 GMT  
		Size: 1.2 MB (1178052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aa8cb2a0b40b6a14458bda499fcfce021f46654814f2055fa7c5a464fbb5d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed441dcdb345cac707a1852c447bf8572017ab247e0ecd8cdac11dd173b718`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54ab9c013e77879ef7a63b0d40774c705e03213cb7627df975b1f544aab723`  
		Last Modified: Fri, 21 Jan 2022 21:03:32 GMT  
		Size: 21.1 MB (21105215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0202deee6aed51b38517aa88783c08700bb12b4f9c59308dbf266a972dc233d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:fe99b62ceb53a90c054c55e86440cf00d13b3ff2f3d99692a0bef4adc1b45c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:44c9a5a828003f5276a952052dc4999b98b0243d0dd1bd7c8e85ea38352077b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75342928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456c635446977ad70607efd5889908b1ccb8b727ae6244dca0569b72c2b63ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:58 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c28794b3e25128706cf6faa48515b023ea6f2d7bfacfe6493fa40b2f1436f1`  
		Last Modified: Wed, 15 Dec 2021 20:21:43 GMT  
		Size: 6.8 MB (6823784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90c29958713df30b15a09c261d26cafc66bab0b23247300298267ef7f066fa67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69346856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab607b2188f06d49d5e0544631eb76703f41790b8928653d0ddb72808181c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:40:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ec878c950532925c0e2a1d397edf1086a25b91f4af6344e9b56a4dbb000c9`  
		Last Modified: Wed, 15 Dec 2021 19:42:24 GMT  
		Size: 6.9 MB (6932833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:ebd5f6aeb57f0cfbb1500c6b5d373ae5de43a098d14e2c107d2e241c3f9d6315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:5fd3cd170a59dbb1d11c44c7369f9f7127a8df53ff91167fa063a1c0cbf3a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b623a541075d3ced662fc1f7b5df6eebb524a04efa65353ad5e468d97a42fa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `docker:20.10-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12`

```console
$ docker pull docker@sha256:a729cce205a05b0b86dc8dca87823efaffc3f74979fe7dc86a707c2fbf631b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.12` - linux; amd64

```console
$ docker pull docker@sha256:b15efb5c932fd29acc764a2b8c0e6b1dfda4450f2a67d630c3b9f205785fdb2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68519144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a9bc7c6340df2ac9d6c8196ca1d905180ddf2ca8b29a8d98f5422e2e5ccf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:17db01f277a58c2d70b2a40a8f46607c5319dd2f23c55dcf8c835cd25f7ff746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62414023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4610f8d36c6766d145891417dd49f9b3e6535b43820bae79640d380fb88016b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-alpine3.15`

```console
$ docker pull docker@sha256:a729cce205a05b0b86dc8dca87823efaffc3f74979fe7dc86a707c2fbf631b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.12-alpine3.15` - linux; amd64

```console
$ docker pull docker@sha256:b15efb5c932fd29acc764a2b8c0e6b1dfda4450f2a67d630c3b9f205785fdb2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68519144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a9bc7c6340df2ac9d6c8196ca1d905180ddf2ca8b29a8d98f5422e2e5ccf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:17db01f277a58c2d70b2a40a8f46607c5319dd2f23c55dcf8c835cd25f7ff746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62414023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4610f8d36c6766d145891417dd49f9b3e6535b43820bae79640d380fb88016b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-dind`

```console
$ docker pull docker@sha256:6f2ae4a5fd85ccf85cdd829057a34ace894d25d544e5e4d9f2e7109297fedf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.12-dind` - linux; amd64

```console
$ docker pull docker@sha256:d848d730231a7e8303e538515251f95cfb6ce86ea7385c9d1bfae7cfd7eff179
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75258270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42336ff683d7dadd320ea6fe9d93a5b101474346302d23f96c9b4546cb414d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af0ce9eee4461072754e6f35f18c219ca6981a16c0042c92bbb4823ce753faa2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be435b54cd392da632ac2c026657537d6559f9a9faf496f22bb1ef7f9a97ea17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-dind-alpine3.15`

```console
$ docker pull docker@sha256:6f2ae4a5fd85ccf85cdd829057a34ace894d25d544e5e4d9f2e7109297fedf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.12-dind-alpine3.15` - linux; amd64

```console
$ docker pull docker@sha256:d848d730231a7e8303e538515251f95cfb6ce86ea7385c9d1bfae7cfd7eff179
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75258270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42336ff683d7dadd320ea6fe9d93a5b101474346302d23f96c9b4546cb414d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12-dind-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af0ce9eee4461072754e6f35f18c219ca6981a16c0042c92bbb4823ce753faa2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be435b54cd392da632ac2c026657537d6559f9a9faf496f22bb1ef7f9a97ea17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-dind-rootless`

```console
$ docker pull docker@sha256:a0e30641697ca722c68a26b104cb271c8f1d1bd9ec3431b06c1c31fe32d06709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.12-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab2f198889709d2a8c96373c713802ebf718c3d607a5d865339a07fde1351c9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95554039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669719fc32513aae9029a1f8d6de49809af5919a32f08db35e2af61583ef8e19`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
# Fri, 21 Jan 2022 20:33:40 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 20:33:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 20:33:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 20:33:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 20:33:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd98d5908761c9c209aa32ce13b48a2d08571f9259b80a7836bc1f64d1a20d`  
		Last Modified: Fri, 21 Jan 2022 20:34:35 GMT  
		Size: 1.2 MB (1162100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e732110c5c1fe0503e484447374f44fe316487faddd706b7677bef3e7277e61`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73db87b0b5a8a0bc668e24b62e413a751187f963dfe522339421ea6a935ee853`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ab341e7115cfdbece6bf8c6fd568a926610ee00aff041ca3022c00d8a10c8`  
		Last Modified: Fri, 21 Jan 2022 20:34:38 GMT  
		Size: 19.1 MB (19131944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b72a872f74ab4930415afca7a1e77c9db132369ea883da4d8698083f8052d3`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d907b9c8ef192ace2c0e03da806d502d75197c4757243a2847b93d6c18ddb0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91316467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d79195eb6e0317cec176cf13daddf6e000c65a7c0fde8ff2cfde11466fe479`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
# Fri, 21 Jan 2022 21:02:11 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 21:02:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 21:02:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 21:02:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 21:02:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 21:02:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 21:02:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72da0b456f787fdd5045043a954f4535d6dc5fd25623135462e686af51fac330`  
		Last Modified: Fri, 21 Jan 2022 21:03:29 GMT  
		Size: 1.2 MB (1178052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aa8cb2a0b40b6a14458bda499fcfce021f46654814f2055fa7c5a464fbb5d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed441dcdb345cac707a1852c447bf8572017ab247e0ecd8cdac11dd173b718`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54ab9c013e77879ef7a63b0d40774c705e03213cb7627df975b1f544aab723`  
		Last Modified: Fri, 21 Jan 2022 21:03:32 GMT  
		Size: 21.1 MB (21105215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0202deee6aed51b38517aa88783c08700bb12b4f9c59308dbf266a972dc233d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-git`

```console
$ docker pull docker@sha256:fe99b62ceb53a90c054c55e86440cf00d13b3ff2f3d99692a0bef4adc1b45c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.12-git` - linux; amd64

```console
$ docker pull docker@sha256:44c9a5a828003f5276a952052dc4999b98b0243d0dd1bd7c8e85ea38352077b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75342928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456c635446977ad70607efd5889908b1ccb8b727ae6244dca0569b72c2b63ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:58 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c28794b3e25128706cf6faa48515b023ea6f2d7bfacfe6493fa40b2f1436f1`  
		Last Modified: Wed, 15 Dec 2021 20:21:43 GMT  
		Size: 6.8 MB (6823784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90c29958713df30b15a09c261d26cafc66bab0b23247300298267ef7f066fa67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69346856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab607b2188f06d49d5e0544631eb76703f41790b8928653d0ddb72808181c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:40:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ec878c950532925c0e2a1d397edf1086a25b91f4af6344e9b56a4dbb000c9`  
		Last Modified: Wed, 15 Dec 2021 19:42:24 GMT  
		Size: 6.9 MB (6932833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-windowsservercore`

```console
$ docker pull docker@sha256:ebd5f6aeb57f0cfbb1500c6b5d373ae5de43a098d14e2c107d2e241c3f9d6315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `docker:20.10.12-windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.12-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-windowsservercore-1809`

```console
$ docker pull docker@sha256:5fd3cd170a59dbb1d11c44c7369f9f7127a8df53ff91167fa063a1c0cbf3a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `docker:20.10.12-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.12-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b623a541075d3ced662fc1f7b5df6eebb524a04efa65353ad5e468d97a42fa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `docker:20.10.12-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:6f2ae4a5fd85ccf85cdd829057a34ace894d25d544e5e4d9f2e7109297fedf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:d848d730231a7e8303e538515251f95cfb6ce86ea7385c9d1bfae7cfd7eff179
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75258270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42336ff683d7dadd320ea6fe9d93a5b101474346302d23f96c9b4546cb414d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:af0ce9eee4461072754e6f35f18c219ca6981a16c0042c92bbb4823ce753faa2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69031571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be435b54cd392da632ac2c026657537d6559f9a9faf496f22bb1ef7f9a97ea17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:a0e30641697ca722c68a26b104cb271c8f1d1bd9ec3431b06c1c31fe32d06709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ab2f198889709d2a8c96373c713802ebf718c3d607a5d865339a07fde1351c9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95554039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669719fc32513aae9029a1f8d6de49809af5919a32f08db35e2af61583ef8e19`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 20:19:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 20:19:43 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 20:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 20:33:36 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 20:33:36 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 20:33:36 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 20:33:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 20:33:36 GMT
CMD []
# Fri, 21 Jan 2022 20:33:40 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 20:33:41 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 20:33:42 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 20:33:45 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 20:33:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 20:33:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d28806efd0ea428cf206cb382a31cb6fba2972e2e6e870051723dab28340158`  
		Last Modified: Wed, 15 Dec 2021 20:20:55 GMT  
		Size: 6.7 MB (6734098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97fd78563ff48a3ea4d64328aac35a97ef969306734b403631f8f8fb36d16e5`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaf1aff7f0b5974dc8e7b9ce5119cf168e186a2281887ebdb30b850059c51ec`  
		Last Modified: Wed, 15 Dec 2021 20:20:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403593afa76f9c10bd6e39f3267c5e6de6589a9e8fb0d4530b7792421eca7010`  
		Last Modified: Fri, 21 Jan 2022 20:34:14 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccd98d5908761c9c209aa32ce13b48a2d08571f9259b80a7836bc1f64d1a20d`  
		Last Modified: Fri, 21 Jan 2022 20:34:35 GMT  
		Size: 1.2 MB (1162100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e732110c5c1fe0503e484447374f44fe316487faddd706b7677bef3e7277e61`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73db87b0b5a8a0bc668e24b62e413a751187f963dfe522339421ea6a935ee853`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ab341e7115cfdbece6bf8c6fd568a926610ee00aff041ca3022c00d8a10c8`  
		Last Modified: Fri, 21 Jan 2022 20:34:38 GMT  
		Size: 19.1 MB (19131944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b72a872f74ab4930415afca7a1e77c9db132369ea883da4d8698083f8052d3`  
		Last Modified: Fri, 21 Jan 2022 20:34:34 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d1d907b9c8ef192ace2c0e03da806d502d75197c4757243a2847b93d6c18ddb0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91316467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d79195eb6e0317cec176cf13daddf6e000c65a7c0fde8ff2cfde11466fe479`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:39:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 15 Dec 2021 19:39:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 15 Dec 2021 19:40:00 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 15 Dec 2021 19:40:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 21 Jan 2022 21:02:00 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Fri, 21 Jan 2022 21:02:00 GMT
VOLUME [/var/lib/docker]
# Fri, 21 Jan 2022 21:02:01 GMT
EXPOSE 2375 2376
# Fri, 21 Jan 2022 21:02:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 21 Jan 2022 21:02:03 GMT
CMD []
# Fri, 21 Jan 2022 21:02:11 GMT
RUN apk add --no-cache iproute2
# Fri, 21 Jan 2022 21:02:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 21 Jan 2022 21:02:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 21 Jan 2022 21:02:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 21 Jan 2022 21:02:17 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 21 Jan 2022 21:02:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 21 Jan 2022 21:02:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12055a90557dd8852e5d26b75d39ee8c5bb53795e2df51b883cc60bf8d765aee`  
		Last Modified: Wed, 15 Dec 2021 19:41:39 GMT  
		Size: 6.6 MB (6612548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd11f99968f9c201fb0dcc9d59bcd8653f16ef5b376446a563ca41ec400751`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482d3fe6b24fb02fce911311cdbd9069d2a150c94dca0d5fcc85cf4b30b21b7`  
		Last Modified: Wed, 15 Dec 2021 19:41:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0140feac1c63b0bac6abf7425d60610dd8ce4128496f80182896a6338d579720`  
		Last Modified: Fri, 21 Jan 2022 21:03:07 GMT  
		Size: 2.8 KB (2752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72da0b456f787fdd5045043a954f4535d6dc5fd25623135462e686af51fac330`  
		Last Modified: Fri, 21 Jan 2022 21:03:29 GMT  
		Size: 1.2 MB (1178052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759aa8cb2a0b40b6a14458bda499fcfce021f46654814f2055fa7c5a464fbb5d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed441dcdb345cac707a1852c447bf8572017ab247e0ecd8cdac11dd173b718`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b54ab9c013e77879ef7a63b0d40774c705e03213cb7627df975b1f544aab723`  
		Last Modified: Fri, 21 Jan 2022 21:03:32 GMT  
		Size: 21.1 MB (21105215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0202deee6aed51b38517aa88783c08700bb12b4f9c59308dbf266a972dc233d`  
		Last Modified: Fri, 21 Jan 2022 21:03:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:fe99b62ceb53a90c054c55e86440cf00d13b3ff2f3d99692a0bef4adc1b45c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:44c9a5a828003f5276a952052dc4999b98b0243d0dd1bd7c8e85ea38352077b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75342928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456c635446977ad70607efd5889908b1ccb8b727ae6244dca0569b72c2b63ead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 20:19:58 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c28794b3e25128706cf6faa48515b023ea6f2d7bfacfe6493fa40b2f1436f1`  
		Last Modified: Wed, 15 Dec 2021 20:21:43 GMT  
		Size: 6.8 MB (6823784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:90c29958713df30b15a09c261d26cafc66bab0b23247300298267ef7f066fa67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69346856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab607b2188f06d49d5e0544631eb76703f41790b8928653d0ddb72808181c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
# Wed, 15 Dec 2021 19:40:27 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ec878c950532925c0e2a1d397edf1086a25b91f4af6344e9b56a4dbb000c9`  
		Last Modified: Wed, 15 Dec 2021 19:42:24 GMT  
		Size: 6.9 MB (6932833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:a729cce205a05b0b86dc8dca87823efaffc3f74979fe7dc86a707c2fbf631b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:b15efb5c932fd29acc764a2b8c0e6b1dfda4450f2a67d630c3b9f205785fdb2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68519144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a9bc7c6340df2ac9d6c8196ca1d905180ddf2ca8b29a8d98f5422e2e5ccf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 20:19:26 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 20:19:27 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 20:19:27 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 20:19:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 20:19:33 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 20:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 20:19:34 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 20:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 20:19:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea03e1895df432fba23ac2810a53a408fa25273ecf001276263d810107e1c81`  
		Last Modified: Wed, 15 Dec 2021 20:20:23 GMT  
		Size: 2.0 MB (1980404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff98835b05535c14c9bd8aa0449fd33d147a58c9a9fe7f21b76137065d0f4c5`  
		Last Modified: Wed, 15 Dec 2021 20:20:21 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2dd7b7d653d57dbfc55dcef38007cf7ae05a4c1a226f4465b3723cb2232ed`  
		Last Modified: Wed, 15 Dec 2021 20:20:32 GMT  
		Size: 63.7 MB (63718464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182b62d4a3549bba88c6f8f32c2d7850ca927a7df0682d9a0de05d0c40095e2`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a57db2abd77c0b995c329d7812464e3734bc1af7b829bd1a42d461de77d3b7`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73490af52bd34939d0d8b02fe67c992943d062112c5a1cb41daf43146a25ae1b`  
		Last Modified: Wed, 15 Dec 2021 20:20:20 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:17db01f277a58c2d70b2a40a8f46607c5319dd2f23c55dcf8c835cd25f7ff746
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62414023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4610f8d36c6766d145891417dd49f9b3e6535b43820bae79640d380fb88016b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 19:39:37 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 15 Dec 2021 19:39:37 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 19:39:38 GMT
ENV DOCKER_VERSION=20.10.12
# Wed, 15 Dec 2021 19:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.12.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.12.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.12.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.12.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 15 Dec 2021 19:39:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 15 Dec 2021 19:39:45 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 15 Dec 2021 19:39:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 15 Dec 2021 19:39:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 15 Dec 2021 19:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 19:39:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1339a3be518a98fb1ef64708d14d86fd4039c4bb0a3d1db8c2d4a4c00fb8a2`  
		Last Modified: Wed, 15 Dec 2021 19:41:10 GMT  
		Size: 1.9 MB (1949540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353862b30dd70efe72e0bf55133d47f2a5b000e37f9cdb0e7e4a0178a5f076ec`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3190c06c4855888df747c4f505d0bc7aaecfbb0d9d4acaee685e28bddfb99b`  
		Last Modified: Wed, 15 Dec 2021 19:41:16 GMT  
		Size: 57.7 MB (57747213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55e216c2ebb46ec0635d982e57890ab4c9025c95a940e79a81a0ed8b50c49b6`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a46f33417cc9574bd0139314cc88909fae8f672527fc69f493d406dad1991e1`  
		Last Modified: Wed, 15 Dec 2021 19:41:09 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c99da1af64cbeec415a8ce2302a76874846814f574e07e7d9072e70ad00192`  
		Last Modified: Wed, 15 Dec 2021 19:41:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:ebd5f6aeb57f0cfbb1500c6b5d373ae5de43a098d14e2c107d2e241c3f9d6315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `docker:windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:5fd3cd170a59dbb1d11c44c7369f9f7127a8df53ff91167fa063a1c0cbf3a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull docker@sha256:8f52f52afb77d3fc6a2b8cbc05c4388daa422669276f8ac2744b5038aebf775a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2766875903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ec23dfe6c2593e115a97d6bbd67981501de5615f0812de650b8219c5d73d96`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:17:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:17:53 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:17:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:19:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd159a4c7852336c64f3eb7878ff3a44c6443ec1e650ac624dbfea388ea5cb7`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 354.9 KB (354884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942665726f3a28e0c77d7653713a56e9f6853e7478f7f67e184d2a284d725baf`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9321c204da4904a8adeefa9f27e8db0d8572f59f541930233c2a92214cc0c564`  
		Last Modified: Fri, 21 Jan 2022 20:21:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cf64cc7750fcbd39c586a295ca4e1314341e3158cb461470dfaf6ae3a697e9`  
		Last Modified: Fri, 21 Jan 2022 20:21:25 GMT  
		Size: 53.2 MB (53195250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b623a541075d3ced662fc1f7b5df6eebb524a04efa65353ad5e468d97a42fa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull docker@sha256:670552032efe790bf8d189ffa11d07ceede67620b8231bec0d6cc68e5cdaaa94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261492298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ae53fed01eaeabdb3154308f5f4be34581020a1d0d2285313de9623e963215`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jan 2022 20:14:44 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jan 2022 20:14:45 GMT
ENV DOCKER_VERSION=20.10.12
# Fri, 21 Jan 2022 20:14:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.12.zip
# Fri, 21 Jan 2022 20:15:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f76b2248c501755f352a657dfd3c4eca0448734b059c3adfe257707cc690df5`  
		Last Modified: Fri, 21 Jan 2022 20:20:00 GMT  
		Size: 598.2 KB (598246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2a0ce9ed70f5f0717e730a1d51405464a7a7ea689191973efc3db943aaca35`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bf5690549cd63c8c9b78432d1292e1070c00919af29d0c48224fd2bafa7aa7`  
		Last Modified: Fri, 21 Jan 2022 20:19:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897e0a0c4008eb04f14b6f67d06e63d6304346e5a1735ae3a12484a6b20688d`  
		Last Modified: Fri, 21 Jan 2022 20:20:59 GMT  
		Size: 53.4 MB (53389971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
