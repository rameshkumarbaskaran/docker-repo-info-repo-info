<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:20`](#docker20)
-	[`docker:20-dind`](#docker20-dind)
-	[`docker:20-dind-rootless`](#docker20-dind-rootless)
-	[`docker:20-git`](#docker20-git)
-	[`docker:20-windowsservercore`](#docker20-windowsservercore)
-	[`docker:20-windowsservercore-1809`](#docker20-windowsservercore-1809)
-	[`docker:20.10`](#docker2010)
-	[`docker:20.10-dind`](#docker2010-dind)
-	[`docker:20.10-dind-rootless`](#docker2010-dind-rootless)
-	[`docker:20.10-git`](#docker2010-git)
-	[`docker:20.10-rc`](#docker2010-rc)
-	[`docker:20.10-rc-dind`](#docker2010-rc-dind)
-	[`docker:20.10-rc-dind-rootless`](#docker2010-rc-dind-rootless)
-	[`docker:20.10-rc-git`](#docker2010-rc-git)
-	[`docker:20.10-rc-windowsservercore`](#docker2010-rc-windowsservercore)
-	[`docker:20.10-rc-windowsservercore-1809`](#docker2010-rc-windowsservercore-1809)
-	[`docker:20.10-windowsservercore`](#docker2010-windowsservercore)
-	[`docker:20.10-windowsservercore-1809`](#docker2010-windowsservercore-1809)
-	[`docker:20.10.10-rc1`](#docker201010-rc1)
-	[`docker:20.10.10-rc1-alpine3.14`](#docker201010-rc1-alpine314)
-	[`docker:20.10.10-rc1-dind`](#docker201010-rc1-dind)
-	[`docker:20.10.10-rc1-dind-alpine3.14`](#docker201010-rc1-dind-alpine314)
-	[`docker:20.10.10-rc1-dind-rootless`](#docker201010-rc1-dind-rootless)
-	[`docker:20.10.10-rc1-git`](#docker201010-rc1-git)
-	[`docker:20.10.10-rc1-windowsservercore`](#docker201010-rc1-windowsservercore)
-	[`docker:20.10.10-rc1-windowsservercore-1809`](#docker201010-rc1-windowsservercore-1809)
-	[`docker:20.10.9`](#docker20109)
-	[`docker:20.10.9-alpine3.14`](#docker20109-alpine314)
-	[`docker:20.10.9-dind`](#docker20109-dind)
-	[`docker:20.10.9-dind-alpine3.14`](#docker20109-dind-alpine314)
-	[`docker:20.10.9-dind-rootless`](#docker20109-dind-rootless)
-	[`docker:20.10.9-git`](#docker20109-git)
-	[`docker:20.10.9-windowsservercore`](#docker20109-windowsservercore)
-	[`docker:20.10.9-windowsservercore-1809`](#docker20109-windowsservercore-1809)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:git`](#dockergit)
-	[`docker:latest`](#dockerlatest)
-	[`docker:rc`](#dockerrc)
-	[`docker:rc-dind`](#dockerrc-dind)
-	[`docker:rc-dind-rootless`](#dockerrc-dind-rootless)
-	[`docker:rc-git`](#dockerrc-git)
-	[`docker:rc-windowsservercore`](#dockerrc-windowsservercore)
-	[`docker:rc-windowsservercore-1809`](#dockerrc-windowsservercore-1809)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)

## `docker:20`

```console
$ docker pull docker@sha256:e7c9c600322345ad23160a0cafde129426270f50ae83133f5354c3fe347a36c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a95cba826396eb3fb4b07117bd1386e46bd982834e622a0a73a7c9d4af7e474
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4799c468fbdd4c40fd59367653432a1cd16b199c572b72cc7059f46d20130075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind`

```console
$ docker pull docker@sha256:d20f0866ee1aca6b0eb7bc8bdb0d0c938721c7f79219b1d3bc1aa58666928586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:25a2c533ed67819c4726fad3ccaa5a1fbcfd602149d1b63c663b620714ec13fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4dc61e43a85443d5bc5759e6ddf1035da284ae045c44dd173830b798dbe53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:f06dfdfd278026427fb1ebf15e05d4bde89df85ff3ba2334fc964a71a705d16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:81af51e044194e802cc9e2ff99144cfc2c4988731d4597bdeeeef6e5e7a583d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf6ba3bce99fb59f75ec0438ad494b919f079b40ab77f41c7319cb0cacfd44`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
# Mon, 04 Oct 2021 22:40:03 GMT
RUN apk add --no-cache iproute2
# Mon, 04 Oct 2021 22:40:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 04 Oct 2021 22:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 04 Oct 2021 22:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 04 Oct 2021 22:40:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 04 Oct 2021 22:40:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d22f8eb08ad02090048708d5c999c5952be4c8d02c6dcb805da08d4012c288c`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.2 MB (1168110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a0714a4fdbcb6036fccf4cf380ac24fc7edd6c974ad7a5731f13c1966238bd`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d79b658117c879c9103d01547357c7566fc262750d0b62c30966d4d49defab`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc95b12a74fd36add08fa63f789816fb9cbea1ddc4bbef6a4406364b0c454f2`  
		Last Modified: Mon, 04 Oct 2021 22:42:04 GMT  
		Size: 21.1 MB (21095995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba365bba8d1721288d49e57f54c068465199da261e7f376686e5b2db5c06bf9`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-git`

```console
$ docker pull docker@sha256:61f6baf32667fc13a9850b16bf6c6de6c8a1c1302ba23dda8350127430f48b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:27b5d5b7687d6a932d2bc0230af9c258588b2d962d77de01b2553b121bbca2de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc52e2bf2a201533bcb1dcf4ac4284d848ef238ac5e9acda87bfaa02989e7f59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:40:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bed24c5b37ab30374c66d0fb367cceeaaa68d6483601e0413a8fb1b97f86092`  
		Last Modified: Mon, 04 Oct 2021 22:42:24 GMT  
		Size: 6.7 MB (6739309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20-windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10`

```console
$ docker pull docker@sha256:e7c9c600322345ad23160a0cafde129426270f50ae83133f5354c3fe347a36c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a95cba826396eb3fb4b07117bd1386e46bd982834e622a0a73a7c9d4af7e474
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4799c468fbdd4c40fd59367653432a1cd16b199c572b72cc7059f46d20130075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind`

```console
$ docker pull docker@sha256:d20f0866ee1aca6b0eb7bc8bdb0d0c938721c7f79219b1d3bc1aa58666928586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:25a2c533ed67819c4726fad3ccaa5a1fbcfd602149d1b63c663b620714ec13fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4dc61e43a85443d5bc5759e6ddf1035da284ae045c44dd173830b798dbe53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-dind-rootless`

```console
$ docker pull docker@sha256:f06dfdfd278026427fb1ebf15e05d4bde89df85ff3ba2334fc964a71a705d16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:81af51e044194e802cc9e2ff99144cfc2c4988731d4597bdeeeef6e5e7a583d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf6ba3bce99fb59f75ec0438ad494b919f079b40ab77f41c7319cb0cacfd44`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
# Mon, 04 Oct 2021 22:40:03 GMT
RUN apk add --no-cache iproute2
# Mon, 04 Oct 2021 22:40:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 04 Oct 2021 22:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 04 Oct 2021 22:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 04 Oct 2021 22:40:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 04 Oct 2021 22:40:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d22f8eb08ad02090048708d5c999c5952be4c8d02c6dcb805da08d4012c288c`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.2 MB (1168110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a0714a4fdbcb6036fccf4cf380ac24fc7edd6c974ad7a5731f13c1966238bd`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d79b658117c879c9103d01547357c7566fc262750d0b62c30966d4d49defab`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc95b12a74fd36add08fa63f789816fb9cbea1ddc4bbef6a4406364b0c454f2`  
		Last Modified: Mon, 04 Oct 2021 22:42:04 GMT  
		Size: 21.1 MB (21095995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba365bba8d1721288d49e57f54c068465199da261e7f376686e5b2db5c06bf9`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-git`

```console
$ docker pull docker@sha256:61f6baf32667fc13a9850b16bf6c6de6c8a1c1302ba23dda8350127430f48b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:27b5d5b7687d6a932d2bc0230af9c258588b2d962d77de01b2553b121bbca2de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc52e2bf2a201533bcb1dcf4ac4284d848ef238ac5e9acda87bfaa02989e7f59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:40:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bed24c5b37ab30374c66d0fb367cceeaaa68d6483601e0413a8fb1b97f86092`  
		Last Modified: Mon, 04 Oct 2021 22:42:24 GMT  
		Size: 6.7 MB (6739309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc`

```console
$ docker pull docker@sha256:87bf27b664b5b365a59b1251e238a85244568ea2fe6f3266c14fb01763ed72a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc` - linux; amd64

```console
$ docker pull docker@sha256:3769dd5e09b1795718cec653d648d55558244ebd8fe13955e02e83bba97bb495
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74032061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b076b43daf1313e0b147059fa86500a35771815f9413671c44aceca8c3905722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e0716f2eedb5fb4a01e3ea0af7673d6d49b8ca7bf91f3e0c20ad5400e58b9591
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68097652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc523ae2cb91deebc7eafb00017e0212313880329889d817c55cd5650135c55b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:39:52 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:40:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dae5b67762b76c0efde572669044763d3b69c3bad14e0ee6d3d9f912f07ce4`  
		Last Modified: Thu, 03 Dec 2020 01:41:32 GMT  
		Size: 63.3 MB (63327989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98281331209e8408adfb9a199feb12e1bad2fce0dc2a041461fdfd7fc00c6c1f`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786af83219d1b175697b334e57b54fbda641bfbb47ae6cf8692249088282b7f7`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2c79e2b7e6cd9911e9263c85ede6e3227ce1bf4128be7c0367ebff8d7f493`  
		Last Modified: Thu, 03 Dec 2020 01:41:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-dind`

```console
$ docker pull docker@sha256:3717406977d2633cf217d5538d59210b17e3662249c4cc6348eb7b4746256d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:0805d140b875b9bc8ebfdbae9ea4b26ba60ee90640a636c575713b6825035f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79995526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d8f7c2d7206c43f115c4af423e1637a1f435068bc08c12e23748f21e55af20`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:19:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:19:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:19:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:19:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:19:57 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:57 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:19:58 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:19:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:58 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d41eb34354d9c453eb21d4d874b79246fdde42e242ce3b3946e3fb08cd77b1`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 6.0 MB (5958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e049752a368345c7b7d2d9539852eeac961803cd38f17028532ee69a4294dfa9`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238431a551c0fd0e6304bda8ab6e3806b3407161b0ddaaa51d97ea7c01ee9172`  
		Last Modified: Thu, 03 Dec 2020 01:21:09 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff110f4494d28d0434d2149ac8619524c81c1701c64fce9a08150d3c6134704`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:59da50e521f0751bd9ee2d13a2deadb0179ed85f9ca11d66d1c5f26f6db3aff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74049118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f70e9de382b96dada198d9dec1b6ed89f85c3829203bba38c722015810c2dd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:39:52 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:40:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:08 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:40:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:40:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:40:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:40:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:40:26 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:26 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:40:27 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:40:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:29 GMT
CMD []
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dae5b67762b76c0efde572669044763d3b69c3bad14e0ee6d3d9f912f07ce4`  
		Last Modified: Thu, 03 Dec 2020 01:41:32 GMT  
		Size: 63.3 MB (63327989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98281331209e8408adfb9a199feb12e1bad2fce0dc2a041461fdfd7fc00c6c1f`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786af83219d1b175697b334e57b54fbda641bfbb47ae6cf8692249088282b7f7`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2c79e2b7e6cd9911e9263c85ede6e3227ce1bf4128be7c0367ebff8d7f493`  
		Last Modified: Thu, 03 Dec 2020 01:41:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d435e9f79835d9fda87e76acce7398814b0643e89ecfe227544f3b45822bf7`  
		Last Modified: Thu, 03 Dec 2020 01:41:44 GMT  
		Size: 5.9 MB (5946709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e189b2a2f82e947f68742148a3171115230951d573530d1c5a362d80d20014`  
		Last Modified: Thu, 03 Dec 2020 01:41:43 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf3c79b611750f8a7ccac6de9b767eac85809bb45d6e747408f8ccebe0fec71`  
		Last Modified: Thu, 03 Dec 2020 01:41:44 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dc8efb21839bb2a43dbbe56ae6ddaad78eb8d40bb50a2e35644e94ef8da4cb`  
		Last Modified: Thu, 03 Dec 2020 01:41:43 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-dind-rootless`

```console
$ docker pull docker@sha256:87d687f262c3953aaed3404b70a39a7cc0cf84c09269d317dfbee7a3587d5cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:20.10-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ba9a867298f514f0155fc0015a88624808e42c513196c562d22d8b37dda7e8a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101261107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004b0ab8718ed6fab023f19e76b5bcd1db501061987c8a2d3fb61965d8a62c25`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:19:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:19:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:19:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:19:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:19:57 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:57 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:19:58 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:19:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:58 GMT
CMD []
# Thu, 03 Dec 2020 01:20:03 GMT
RUN apk add --no-cache iproute2
# Thu, 03 Dec 2020 01:20:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 03 Dec 2020 01:20:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:20:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 03 Dec 2020 01:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 03 Dec 2020 01:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Dec 2020 01:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d41eb34354d9c453eb21d4d874b79246fdde42e242ce3b3946e3fb08cd77b1`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 6.0 MB (5958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e049752a368345c7b7d2d9539852eeac961803cd38f17028532ee69a4294dfa9`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238431a551c0fd0e6304bda8ab6e3806b3407161b0ddaaa51d97ea7c01ee9172`  
		Last Modified: Thu, 03 Dec 2020 01:21:09 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff110f4494d28d0434d2149ac8619524c81c1701c64fce9a08150d3c6134704`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbfa1b4e2ec98111aa0501360a509205fbf16bc526d399cfa670d0c35b6046`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 1.1 MB (1092668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f728936c6fdb24935e0bb1366ed702b917e9581519d22efab93f8728513a259a`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b638cd1abd59f9f12d28d5d6227cdb991c66c16fd6f9b00dc39564d1583b251`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cac38aa50f31cfa5934d05e52f6ff76d5b8809a374846c9b36af98c8f5a822`  
		Last Modified: Thu, 03 Dec 2020 01:21:21 GMT  
		Size: 20.2 MB (20171300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbc24424926ce09c4f9387a3510fe8d83e0d537f83a25565d4d6f8eb4a43a50`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-git`

```console
$ docker pull docker@sha256:dc3a29ddb605e3f57587c3f95def6b77b62d45ab371733fe5649502fb6483ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10-rc-git` - linux; amd64

```console
$ docker pull docker@sha256:50da362dfee957933c12cf5c491ce74186d4649909508ea62d1071d6ca95d82e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82344149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f16515870a2368ced3032e3241b1ddcfef531d220a78ee33fe20dc4dae86f12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:20:14 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb412ed0bbeb7d18fa0721ca6ebdff49ee36167e163ff98e4340081383937f5`  
		Last Modified: Thu, 03 Dec 2020 01:21:29 GMT  
		Size: 8.3 MB (8312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10-rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7eb555a28260d5d2f332f7cbba3376b9c0f3af26d7ad57919fcef2d11cb293c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76601053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fee96193f4c63cc4f6c5ea730101d8581a380a567b7747a82b1b372b7433c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:39:52 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:40:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:08 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:40:41 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dae5b67762b76c0efde572669044763d3b69c3bad14e0ee6d3d9f912f07ce4`  
		Last Modified: Thu, 03 Dec 2020 01:41:32 GMT  
		Size: 63.3 MB (63327989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98281331209e8408adfb9a199feb12e1bad2fce0dc2a041461fdfd7fc00c6c1f`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786af83219d1b175697b334e57b54fbda641bfbb47ae6cf8692249088282b7f7`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2c79e2b7e6cd9911e9263c85ede6e3227ce1bf4128be7c0367ebff8d7f493`  
		Last Modified: Thu, 03 Dec 2020 01:41:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcba67047bd912ef5667bd37cd8f4c9d787f98464532b942ab796118d567983`  
		Last Modified: Thu, 03 Dec 2020 01:41:54 GMT  
		Size: 8.5 MB (8503401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-rc-windowsservercore`

**does not exist** (yet?)

## `docker:20.10-rc-windowsservercore-1809`

**does not exist** (yet?)

## `docker:20.10-windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10-windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.10-rc1`

**does not exist** (yet?)

## `docker:20.10.10-rc1-alpine3.14`

**does not exist** (yet?)

## `docker:20.10.10-rc1-dind`

**does not exist** (yet?)

## `docker:20.10.10-rc1-dind-alpine3.14`

**does not exist** (yet?)

## `docker:20.10.10-rc1-dind-rootless`

**does not exist** (yet?)

## `docker:20.10.10-rc1-git`

**does not exist** (yet?)

## `docker:20.10.10-rc1-windowsservercore`

**does not exist** (yet?)

## `docker:20.10.10-rc1-windowsservercore-1809`

**does not exist** (yet?)

## `docker:20.10.9`

```console
$ docker pull docker@sha256:e7c9c600322345ad23160a0cafde129426270f50ae83133f5354c3fe347a36c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a95cba826396eb3fb4b07117bd1386e46bd982834e622a0a73a7c9d4af7e474
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4799c468fbdd4c40fd59367653432a1cd16b199c572b72cc7059f46d20130075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-alpine3.14`

```console
$ docker pull docker@sha256:e7c9c600322345ad23160a0cafde129426270f50ae83133f5354c3fe347a36c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a95cba826396eb3fb4b07117bd1386e46bd982834e622a0a73a7c9d4af7e474
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4799c468fbdd4c40fd59367653432a1cd16b199c572b72cc7059f46d20130075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-dind`

```console
$ docker pull docker@sha256:d20f0866ee1aca6b0eb7bc8bdb0d0c938721c7f79219b1d3bc1aa58666928586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:25a2c533ed67819c4726fad3ccaa5a1fbcfd602149d1b63c663b620714ec13fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4dc61e43a85443d5bc5759e6ddf1035da284ae045c44dd173830b798dbe53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-dind-alpine3.14`

```console
$ docker pull docker@sha256:d20f0866ee1aca6b0eb7bc8bdb0d0c938721c7f79219b1d3bc1aa58666928586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-dind-alpine3.14` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-dind-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:25a2c533ed67819c4726fad3ccaa5a1fbcfd602149d1b63c663b620714ec13fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4dc61e43a85443d5bc5759e6ddf1035da284ae045c44dd173830b798dbe53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-dind-rootless`

```console
$ docker pull docker@sha256:f06dfdfd278026427fb1ebf15e05d4bde89df85ff3ba2334fc964a71a705d16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:81af51e044194e802cc9e2ff99144cfc2c4988731d4597bdeeeef6e5e7a583d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf6ba3bce99fb59f75ec0438ad494b919f079b40ab77f41c7319cb0cacfd44`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
# Mon, 04 Oct 2021 22:40:03 GMT
RUN apk add --no-cache iproute2
# Mon, 04 Oct 2021 22:40:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 04 Oct 2021 22:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 04 Oct 2021 22:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 04 Oct 2021 22:40:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 04 Oct 2021 22:40:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d22f8eb08ad02090048708d5c999c5952be4c8d02c6dcb805da08d4012c288c`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.2 MB (1168110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a0714a4fdbcb6036fccf4cf380ac24fc7edd6c974ad7a5731f13c1966238bd`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d79b658117c879c9103d01547357c7566fc262750d0b62c30966d4d49defab`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc95b12a74fd36add08fa63f789816fb9cbea1ddc4bbef6a4406364b0c454f2`  
		Last Modified: Mon, 04 Oct 2021 22:42:04 GMT  
		Size: 21.1 MB (21095995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba365bba8d1721288d49e57f54c068465199da261e7f376686e5b2db5c06bf9`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-git`

```console
$ docker pull docker@sha256:61f6baf32667fc13a9850b16bf6c6de6c8a1c1302ba23dda8350127430f48b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20.10.9-git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20.10.9-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:27b5d5b7687d6a932d2bc0230af9c258588b2d962d77de01b2553b121bbca2de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc52e2bf2a201533bcb1dcf4ac4284d848ef238ac5e9acda87bfaa02989e7f59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:40:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bed24c5b37ab30374c66d0fb367cceeaaa68d6483601e0413a8fb1b97f86092`  
		Last Modified: Mon, 04 Oct 2021 22:42:24 GMT  
		Size: 6.7 MB (6739309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10.9-windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:20.10.9-windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:20.10.9-windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind`

```console
$ docker pull docker@sha256:d20f0866ee1aca6b0eb7bc8bdb0d0c938721c7f79219b1d3bc1aa58666928586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:24628ded7711e48db56af875236ac30a8950305ac461332955b3375ac5a87e1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74967424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efbbff84703848e1c787073a954e8e3f0146836d94673f2d54f3672296bf82f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:25a2c533ed67819c4726fad3ccaa5a1fbcfd602149d1b63c663b620714ec13fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68779507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f4dc61e43a85443d5bc5759e6ddf1035da284ae045c44dd173830b798dbe53`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:f06dfdfd278026427fb1ebf15e05d4bde89df85ff3ba2334fc964a71a705d16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:75acfc77a83d9b4d557aab529432058b78ac6d629325c9d61c385cd2fc48fe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4aec2427ffe9836431bca031ae4354053a010dae4736917b174d52da90dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Oct 2021 17:32:37 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:38 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Oct 2021 17:32:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Oct 2021 17:32:39 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:39 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Oct 2021 17:32:39 GMT
EXPOSE 2375 2376
# Tue, 05 Oct 2021 17:32:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:40 GMT
CMD []
# Tue, 05 Oct 2021 17:32:44 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Oct 2021 17:32:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Oct 2021 17:32:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Oct 2021 17:32:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Oct 2021 17:32:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Oct 2021 17:32:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Oct 2021 17:32:50 GMT
USER rootless
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec67a583a94bdc153dacab38a9b85a032e58cd332069a169388b45727d5a03c`  
		Last Modified: Tue, 05 Oct 2021 17:33:49 GMT  
		Size: 6.5 MB (6521405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28a20c97b2389ddc8160afed72508ba7d5ae1464e5837dd19905c4e7130c4e5`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170df0071614602fcd5820d60cc7c9a73f8e10a616928d111e25041951c3507d`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfeb3c70a4f70f3868998e1000a4907ec50a8303595dbf0e96bdd03d59e086c`  
		Last Modified: Tue, 05 Oct 2021 17:33:48 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418f850bf44d36d532f71a72ed317e54531b904953d99821dd316e73e777d23c`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.1 MB (1148745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03facf1a1e41afef60e2e7bad46f0fbd44f5b2b3a3328337c3e0a6049120dd8`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f919e685bb3723d38cd895248bb1c99de9588af3aba7f57ef5cb72eca54106a9`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79573e4e685e01787d1e021ea1cecb99cdbf78577b160037c6ed2c7f8f2b304`  
		Last Modified: Tue, 05 Oct 2021 17:34:11 GMT  
		Size: 19.1 MB (19118054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7054ab8c007ff95ebed9750aae6c97b9f692ed317ea464234611c57db8601634`  
		Last Modified: Tue, 05 Oct 2021 17:34:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:81af51e044194e802cc9e2ff99144cfc2c4988731d4597bdeeeef6e5e7a583d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91045329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf6ba3bce99fb59f75ec0438ad494b919f079b40ab77f41c7319cb0cacfd44`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:39:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Mon, 04 Oct 2021 22:39:53 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:39:53 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Mon, 04 Oct 2021 22:39:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Mon, 04 Oct 2021 22:39:54 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:54 GMT
VOLUME [/var/lib/docker]
# Mon, 04 Oct 2021 22:39:54 GMT
EXPOSE 2375 2376
# Mon, 04 Oct 2021 22:39:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:55 GMT
CMD []
# Mon, 04 Oct 2021 22:40:03 GMT
RUN apk add --no-cache iproute2
# Mon, 04 Oct 2021 22:40:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Mon, 04 Oct 2021 22:40:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Mon, 04 Oct 2021 22:40:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Mon, 04 Oct 2021 22:40:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Mon, 04 Oct 2021 22:40:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 04 Oct 2021 22:40:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6df64ef29bdc4a4edaabe9dba4c929323e0fb59f04d2c4157d1614bd477b4c`  
		Last Modified: Mon, 04 Oct 2021 22:41:38 GMT  
		Size: 6.4 MB (6418544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab2a956e5b959cab7be1b5014e743e67aa28c92a3a2b095fa35e0ad32dcb269`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660c7d1ec1ea400226cdcfba7d06bc6bdf859f3f39fbf91d93258c1b90b37368`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eedd8c550c3dd9f5a5cb146b38007c1f143f1c3abc63edb69c622d288eb6cd`  
		Last Modified: Mon, 04 Oct 2021 22:41:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d22f8eb08ad02090048708d5c999c5952be4c8d02c6dcb805da08d4012c288c`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.2 MB (1168110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a0714a4fdbcb6036fccf4cf380ac24fc7edd6c974ad7a5731f13c1966238bd`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d79b658117c879c9103d01547357c7566fc262750d0b62c30966d4d49defab`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc95b12a74fd36add08fa63f789816fb9cbea1ddc4bbef6a4406364b0c454f2`  
		Last Modified: Mon, 04 Oct 2021 22:42:04 GMT  
		Size: 21.1 MB (21095995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba365bba8d1721288d49e57f54c068465199da261e7f376686e5b2db5c06bf9`  
		Last Modified: Mon, 04 Oct 2021 22:42:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:git`

```console
$ docker pull docker@sha256:61f6baf32667fc13a9850b16bf6c6de6c8a1c1302ba23dda8350127430f48b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:3bf13c54edb2a2b817bcad4ae459bf6d8b867930b5026d1f51d4593f598495fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed61dfae734a45e9440fbd932eeb2b244f0079a45398e33dd1478f62a4f3be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
# Tue, 05 Oct 2021 17:32:54 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22895e9057604af4145b328a599ef34ed98eee9085de276ad33fe1adf50f5f`  
		Last Modified: Tue, 05 Oct 2021 17:34:29 GMT  
		Size: 6.6 MB (6630406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:27b5d5b7687d6a932d2bc0230af9c258588b2d962d77de01b2553b121bbca2de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69095380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc52e2bf2a201533bcb1dcf4ac4284d848ef238ac5e9acda87bfaa02989e7f59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
# Mon, 04 Oct 2021 22:40:16 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bed24c5b37ab30374c66d0fb367cceeaaa68d6483601e0413a8fb1b97f86092`  
		Last Modified: Mon, 04 Oct 2021 22:42:24 GMT  
		Size: 6.7 MB (6739309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:latest`

```console
$ docker pull docker@sha256:e7c9c600322345ad23160a0cafde129426270f50ae83133f5354c3fe347a36c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:62302357e804b152e157d3603ce7a97c3f368a626ce027eee1d1e02b5ae924f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68441124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6448e722e510f9bb0bb5c2f65ef99295fc2321b656c00f088078ccf6564372b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 22:19:34 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 22:19:35 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Oct 2021 17:32:23 GMT
ENV DOCKER_VERSION=20.10.9
# Tue, 05 Oct 2021 17:32:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Oct 2021 17:32:29 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Oct 2021 17:32:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Oct 2021 17:32:30 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Oct 2021 17:32:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:32:31 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14df950e5a796f46eb6615169002a1c428bd908141de49fb35ec026c206e77aa`  
		Last Modified: Wed, 01 Sep 2021 22:20:33 GMT  
		Size: 1.9 MB (1935099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a31cc9e913427e8959328b7d290bdcc639a9f84c11956c33c0ce112788cf19`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e88c3a8ccafbb819665e363fc6947b47a896d85170e8b267c6c12176385b3c`  
		Last Modified: Tue, 05 Oct 2021 17:33:31 GMT  
		Size: 63.7 MB (63689714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843e00801cfc09a8e327c9cced9fbc94f179e9f03caf50d0ac1c01ae1ca92c3b`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a43c1017099b38ffcabb7b27169d9ca7821bbfea77b15059c969020a0acfd`  
		Last Modified: Tue, 05 Oct 2021 17:33:20 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b52f4e484f770e1039348c98519c8610f67ba16969fb9ab93afae3f4421f7d1`  
		Last Modified: Tue, 05 Oct 2021 17:33:19 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3a95cba826396eb3fb4b07117bd1386e46bd982834e622a0a73a7c9d4af7e474
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4799c468fbdd4c40fd59367653432a1cd16b199c572b72cc7059f46d20130075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 21:39:27 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Wed, 01 Sep 2021 21:39:28 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 04 Oct 2021 22:39:36 GMT
ENV DOCKER_VERSION=20.10.9
# Mon, 04 Oct 2021 22:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.9.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Mon, 04 Oct 2021 22:39:41 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Mon, 04 Oct 2021 22:39:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 04 Oct 2021 22:39:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Mon, 04 Oct 2021 22:39:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Oct 2021 22:39:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b53fc582fabf462979a1e3b92dd264069a8c4db48d483900b12ffaf539203`  
		Last Modified: Wed, 01 Sep 2021 21:41:00 GMT  
		Size: 1.9 MB (1909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6288aa69581811c8fced6884b0ce72c344df8f72b9317062be7b6672c538444`  
		Last Modified: Wed, 01 Sep 2021 21:40:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2addeb3702952172db1a24220381e0ef6580b99177900ac4d13119b213c2fcfc`  
		Last Modified: Mon, 04 Oct 2021 22:41:15 GMT  
		Size: 57.7 MB (57733347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb723bbe59439dde838001146817815fb936b405e719e023874e6c96f0a10c3f`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da7ad22416e3ba9ff03eac3fe069bd73b06cdac1fd584e932e9f35270fae50`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97dbd9a21f6258fbc117eeddf6fb34a1172588deb227ce6ffb2ab00321631af`  
		Last Modified: Mon, 04 Oct 2021 22:41:05 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc`

```console
$ docker pull docker@sha256:8630d7cc63ba4708cfe81a746863eb588d604875f066978c8be5e187a174bd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:rc` - linux; amd64

```console
$ docker pull docker@sha256:3769dd5e09b1795718cec653d648d55558244ebd8fe13955e02e83bba97bb495
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74032061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b076b43daf1313e0b147059fa86500a35771815f9413671c44aceca8c3905722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm variant v6

```console
$ docker pull docker@sha256:b50cd9618f77ebb37c77bfbc7159787900f8449bff5ebd16ef4314439e1905d5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64876994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996aeccdec0200978b3055ef8f213be775fcfb814206e90b5f451dbf28002f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Jan 2020 19:49:55 GMT
ENV DOCKER_CHANNEL=test
# Fri, 07 Feb 2020 01:49:30 GMT
ENV DOCKER_VERSION=19.03.6-rc2
# Fri, 07 Feb 2020 01:49:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 07 Feb 2020 01:49:43 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 07 Feb 2020 01:49:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:49:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2020 01:49:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 07 Feb 2020 01:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 01:49:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c50d9f5ebbcdc846f18771ee330450b7fff603f6f3f0a162f827feefea9b2d`  
		Last Modified: Fri, 07 Feb 2020 01:51:56 GMT  
		Size: 59.9 MB (59902162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ca6425cb3f176b096d64b01e6281be81bd13df81b50ffa27a95239e4511d5`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e48b798c3734357d6c87dfca18e0ae77f15e69e877cbc3c2370ac2ef004efe`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0fffc54c09bd0c9388338ccbf469ccc15bce13951638c2b07e9a64f7d7d761`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm variant v7

```console
$ docker pull docker@sha256:eb32cec8343a12b521cc18b3f20bd834c93fd78d5ad364ae5f16375d396a2d9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64565553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d565c546476b27e22955e7eba0558a217cdec7677161d7d758e8e5a484873a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Jan 2020 19:57:32 GMT
ENV DOCKER_CHANNEL=test
# Fri, 07 Feb 2020 02:39:45 GMT
ENV DOCKER_VERSION=19.03.6-rc2
# Fri, 07 Feb 2020 02:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 07 Feb 2020 02:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 07 Feb 2020 02:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 07 Feb 2020 02:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2020 02:40:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 07 Feb 2020 02:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 02:40:05 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9015c180d6e38c780d7ffae8ed1360cba3fc384f560587a6092c42317740318`  
		Last Modified: Fri, 07 Feb 2020 02:41:38 GMT  
		Size: 59.9 MB (59889736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa23b1a26f3312c0b9b21381b8b9ed57002efaf12478275d8dfa252dcb55926`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9659cd7acc802bc16b7c635d6c4f4829612219506fb5a8c358c7e3ffe55ae0b1`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6e1d50e985217559261a740df789190ce04f211a9669c1e08ea0cf4d40ce4`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e0716f2eedb5fb4a01e3ea0af7673d6d49b8ca7bf91f3e0c20ad5400e58b9591
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68097652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc523ae2cb91deebc7eafb00017e0212313880329889d817c55cd5650135c55b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:39:52 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:40:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:08 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dae5b67762b76c0efde572669044763d3b69c3bad14e0ee6d3d9f912f07ce4`  
		Last Modified: Thu, 03 Dec 2020 01:41:32 GMT  
		Size: 63.3 MB (63327989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98281331209e8408adfb9a199feb12e1bad2fce0dc2a041461fdfd7fc00c6c1f`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786af83219d1b175697b334e57b54fbda641bfbb47ae6cf8692249088282b7f7`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2c79e2b7e6cd9911e9263c85ede6e3227ce1bf4128be7c0367ebff8d7f493`  
		Last Modified: Thu, 03 Dec 2020 01:41:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind`

```console
$ docker pull docker@sha256:c177ed083616880b3fa8db04c837976633edf142ebaa35f318ed1bf6f83358bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:0805d140b875b9bc8ebfdbae9ea4b26ba60ee90640a636c575713b6825035f66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79995526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d8f7c2d7206c43f115c4af423e1637a1f435068bc08c12e23748f21e55af20`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:19:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:19:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:19:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:19:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:19:57 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:57 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:19:58 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:19:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:58 GMT
CMD []
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d41eb34354d9c453eb21d4d874b79246fdde42e242ce3b3946e3fb08cd77b1`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 6.0 MB (5958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e049752a368345c7b7d2d9539852eeac961803cd38f17028532ee69a4294dfa9`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238431a551c0fd0e6304bda8ab6e3806b3407161b0ddaaa51d97ea7c01ee9172`  
		Last Modified: Thu, 03 Dec 2020 01:21:09 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff110f4494d28d0434d2149ac8619524c81c1701c64fce9a08150d3c6134704`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a1e9f065ea4b31de9aeed07048cf820a64b8637262393b24a4216450da46b7d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68096981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da59f11687039721cafbe22807b6e85c9b11ca0111b044128dc645ce8d41395`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Jan 2020 19:49:55 GMT
ENV DOCKER_CHANNEL=test
# Fri, 07 Feb 2020 01:49:30 GMT
ENV DOCKER_VERSION=19.03.6-rc2
# Fri, 07 Feb 2020 01:49:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 07 Feb 2020 01:49:43 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 07 Feb 2020 01:49:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:49:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2020 01:49:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 07 Feb 2020 01:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 01:49:57 GMT
CMD ["sh"]
# Fri, 07 Feb 2020 01:50:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 07 Feb 2020 01:50:21 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 07 Feb 2020 01:50:22 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 07 Feb 2020 01:50:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 07 Feb 2020 01:50:25 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:50:26 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Feb 2020 01:50:27 GMT
EXPOSE 2375 2376
# Fri, 07 Feb 2020 01:50:27 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Feb 2020 01:50:28 GMT
CMD []
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c50d9f5ebbcdc846f18771ee330450b7fff603f6f3f0a162f827feefea9b2d`  
		Last Modified: Fri, 07 Feb 2020 01:51:56 GMT  
		Size: 59.9 MB (59902162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ca6425cb3f176b096d64b01e6281be81bd13df81b50ffa27a95239e4511d5`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e48b798c3734357d6c87dfca18e0ae77f15e69e877cbc3c2370ac2ef004efe`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0fffc54c09bd0c9388338ccbf469ccc15bce13951638c2b07e9a64f7d7d761`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb980a31655ba58abb32f83560d0ef7f88661301b94ccaa175d2e313bc6aed7`  
		Last Modified: Fri, 07 Feb 2020 01:52:09 GMT  
		Size: 3.2 MB (3215389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce42f22e41480fa85926bef938310586295987a9f0722602ffd0b2d0eb4cd9c`  
		Last Modified: Fri, 07 Feb 2020 01:52:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112fde20474ec85e4d421e2dd65099e4243260fa1e46d7b1e01f106ad335d3b6`  
		Last Modified: Fri, 07 Feb 2020 01:52:09 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a0e541a9bb4780f1028d69eab8221e95d376c201eaee002c22de1367512015`  
		Last Modified: Fri, 07 Feb 2020 01:52:09 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2d945bded57825feb19e9c37871c849a56d1761c01274f9f1efecdc0b3be3e50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67448688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cd21cfa9c1ccacf612a7233e0e0627b92209be24b4b900f213c786105b3f05`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Jan 2020 19:57:32 GMT
ENV DOCKER_CHANNEL=test
# Fri, 07 Feb 2020 02:39:45 GMT
ENV DOCKER_VERSION=19.03.6-rc2
# Fri, 07 Feb 2020 02:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 07 Feb 2020 02:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 07 Feb 2020 02:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 07 Feb 2020 02:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2020 02:40:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 07 Feb 2020 02:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 02:40:05 GMT
CMD ["sh"]
# Fri, 07 Feb 2020 02:40:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 07 Feb 2020 02:40:22 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 07 Feb 2020 02:40:24 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 07 Feb 2020 02:40:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 07 Feb 2020 02:40:27 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 07 Feb 2020 02:40:27 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Feb 2020 02:40:28 GMT
EXPOSE 2375 2376
# Fri, 07 Feb 2020 02:40:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Feb 2020 02:40:30 GMT
CMD []
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9015c180d6e38c780d7ffae8ed1360cba3fc384f560587a6092c42317740318`  
		Last Modified: Fri, 07 Feb 2020 02:41:38 GMT  
		Size: 59.9 MB (59889736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa23b1a26f3312c0b9b21381b8b9ed57002efaf12478275d8dfa252dcb55926`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9659cd7acc802bc16b7c635d6c4f4829612219506fb5a8c358c7e3ffe55ae0b1`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6e1d50e985217559261a740df789190ce04f211a9669c1e08ea0cf4d40ce4`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c49d89b3df9a5ae048f9b8a28125a3d03d349de05c21b3f612bf50b8cbff70`  
		Last Modified: Fri, 07 Feb 2020 02:41:50 GMT  
		Size: 2.9 MB (2878541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a736423d9f5ee6704eb47d7eea5a10369e429a6bf29bb1a3753a24928f41b28e`  
		Last Modified: Fri, 07 Feb 2020 02:41:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6d201bed75e9b686968aac568ea8cce3ebe49784cb654e9498110d113174c`  
		Last Modified: Fri, 07 Feb 2020 02:41:49 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e666991900d250a1b261fec470825cf883317a26a234d9336f995cb182db3e8c`  
		Last Modified: Fri, 07 Feb 2020 02:41:49 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:59da50e521f0751bd9ee2d13a2deadb0179ed85f9ca11d66d1c5f26f6db3aff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74049118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f70e9de382b96dada198d9dec1b6ed89f85c3829203bba38c722015810c2dd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:39:52 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:40:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:08 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:40:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:40:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:40:22 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:40:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:40:26 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:26 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:40:27 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:40:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:29 GMT
CMD []
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dae5b67762b76c0efde572669044763d3b69c3bad14e0ee6d3d9f912f07ce4`  
		Last Modified: Thu, 03 Dec 2020 01:41:32 GMT  
		Size: 63.3 MB (63327989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98281331209e8408adfb9a199feb12e1bad2fce0dc2a041461fdfd7fc00c6c1f`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786af83219d1b175697b334e57b54fbda641bfbb47ae6cf8692249088282b7f7`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2c79e2b7e6cd9911e9263c85ede6e3227ce1bf4128be7c0367ebff8d7f493`  
		Last Modified: Thu, 03 Dec 2020 01:41:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d435e9f79835d9fda87e76acce7398814b0643e89ecfe227544f3b45822bf7`  
		Last Modified: Thu, 03 Dec 2020 01:41:44 GMT  
		Size: 5.9 MB (5946709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e189b2a2f82e947f68742148a3171115230951d573530d1c5a362d80d20014`  
		Last Modified: Thu, 03 Dec 2020 01:41:43 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf3c79b611750f8a7ccac6de9b767eac85809bb45d6e747408f8ccebe0fec71`  
		Last Modified: Thu, 03 Dec 2020 01:41:44 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dc8efb21839bb2a43dbbe56ae6ddaad78eb8d40bb50a2e35644e94ef8da4cb`  
		Last Modified: Thu, 03 Dec 2020 01:41:43 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:87d687f262c3953aaed3404b70a39a7cc0cf84c09269d317dfbee7a3587d5cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ba9a867298f514f0155fc0015a88624808e42c513196c562d22d8b37dda7e8a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101261107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004b0ab8718ed6fab023f19e76b5bcd1db501061987c8a2d3fb61965d8a62c25`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:19:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 03 Dec 2020 01:19:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:19:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 03 Dec 2020 01:19:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 03 Dec 2020 01:19:57 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:57 GMT
VOLUME [/var/lib/docker]
# Thu, 03 Dec 2020 01:19:58 GMT
EXPOSE 2375 2376
# Thu, 03 Dec 2020 01:19:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:58 GMT
CMD []
# Thu, 03 Dec 2020 01:20:03 GMT
RUN apk add --no-cache iproute2
# Thu, 03 Dec 2020 01:20:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 03 Dec 2020 01:20:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 03 Dec 2020 01:20:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 03 Dec 2020 01:20:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 03 Dec 2020 01:20:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 03 Dec 2020 01:20:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d41eb34354d9c453eb21d4d874b79246fdde42e242ce3b3946e3fb08cd77b1`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 6.0 MB (5958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e049752a368345c7b7d2d9539852eeac961803cd38f17028532ee69a4294dfa9`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238431a551c0fd0e6304bda8ab6e3806b3407161b0ddaaa51d97ea7c01ee9172`  
		Last Modified: Thu, 03 Dec 2020 01:21:09 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff110f4494d28d0434d2149ac8619524c81c1701c64fce9a08150d3c6134704`  
		Last Modified: Thu, 03 Dec 2020 01:21:10 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dbfa1b4e2ec98111aa0501360a509205fbf16bc526d399cfa670d0c35b6046`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 1.1 MB (1092668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f728936c6fdb24935e0bb1366ed702b917e9581519d22efab93f8728513a259a`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b638cd1abd59f9f12d28d5d6227cdb991c66c16fd6f9b00dc39564d1583b251`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cac38aa50f31cfa5934d05e52f6ff76d5b8809a374846c9b36af98c8f5a822`  
		Last Modified: Thu, 03 Dec 2020 01:21:21 GMT  
		Size: 20.2 MB (20171300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbc24424926ce09c4f9387a3510fe8d83e0d537f83a25565d4d6f8eb4a43a50`  
		Last Modified: Thu, 03 Dec 2020 01:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-git`

```console
$ docker pull docker@sha256:839bd7e66b87ac6499da290c1d402b445378e0522e91da9d053f342e84632a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `docker:rc-git` - linux; amd64

```console
$ docker pull docker@sha256:50da362dfee957933c12cf5c491ce74186d4649909508ea62d1071d6ca95d82e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82344149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f16515870a2368ced3032e3241b1ddcfef531d220a78ee33fe20dc4dae86f12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:15:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 03:15:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:19:40 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:19:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:19:47 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:19:47 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:19:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:19:48 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:20:14 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457`  
		Last Modified: Thu, 22 Oct 2020 03:16:47 GMT  
		Size: 2.0 MB (2039054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658`  
		Last Modified: Thu, 22 Oct 2020 03:16:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fd8b7f6d785daed3820c5e1498e61167583e9045feac86ffb7e44cc08a098`  
		Last Modified: Thu, 03 Dec 2020 01:21:03 GMT  
		Size: 69.2 MB (69194310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db597305dcaeb9a5ab05768839f670f942793156b7b3b3936ce746314bfca19`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103a137d36f54bc2da72b6de7a354e8ac532e331da4fa7cea3061e707ee631d6`  
		Last Modified: Thu, 03 Dec 2020 01:20:49 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3157e29d9bca4123fa681ea84dd51dad3441b7f2ac7a8d8cb09865df9f7c7fbd`  
		Last Modified: Thu, 03 Dec 2020 01:20:50 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb412ed0bbeb7d18fa0721ca6ebdff49ee36167e163ff98e4340081383937f5`  
		Last Modified: Thu, 03 Dec 2020 01:21:29 GMT  
		Size: 8.3 MB (8312088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:caea4a7d7fe378ba510788faec30405dbde23cd5abb507bcb8e3966138d0b7a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72712203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f7f7d70a46d9515d127312836386c98c3502b16759fafb0b11878763e19606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:52:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 05:52:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Jan 2020 19:49:55 GMT
ENV DOCKER_CHANNEL=test
# Fri, 07 Feb 2020 01:49:30 GMT
ENV DOCKER_VERSION=19.03.6-rc2
# Fri, 07 Feb 2020 01:49:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 07 Feb 2020 01:49:43 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 07 Feb 2020 01:49:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 07 Feb 2020 01:49:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2020 01:49:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 07 Feb 2020 01:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 01:49:57 GMT
CMD ["sh"]
# Fri, 07 Feb 2020 01:50:49 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c86f804e7b5cc2f1f9d87340dfef1fcc13615f2cbd25bda470e513c1e4a627`  
		Last Modified: Sat, 18 Jan 2020 05:54:22 GMT  
		Size: 2.4 MB (2355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d84775c03f92068112e3757afd6ddab1b2c0a3d1073e91b182620b6ec239f7`  
		Last Modified: Sat, 18 Jan 2020 05:54:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c50d9f5ebbcdc846f18771ee330450b7fff603f6f3f0a162f827feefea9b2d`  
		Last Modified: Fri, 07 Feb 2020 01:51:56 GMT  
		Size: 59.9 MB (59902162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ca6425cb3f176b096d64b01e6281be81bd13df81b50ffa27a95239e4511d5`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e48b798c3734357d6c87dfca18e0ae77f15e69e877cbc3c2370ac2ef004efe`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0fffc54c09bd0c9388338ccbf469ccc15bce13951638c2b07e9a64f7d7d761`  
		Last Modified: Fri, 07 Feb 2020 01:51:32 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2308e8328aef9a6de84f7410e943d859481a88aa7636d5297a2d35b9961566a8`  
		Last Modified: Fri, 07 Feb 2020 01:52:25 GMT  
		Size: 7.8 MB (7835209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:c310a56efb22f8697c34b441cf87b45e30e64369a5fca5967dc3938e57be5818
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71638357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12fb892d7c3e2cafe92f04437154f38313f159a6d959942d02a7dfd255090ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:01:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 03:01:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 29 Jan 2020 19:57:32 GMT
ENV DOCKER_CHANNEL=test
# Fri, 07 Feb 2020 02:39:45 GMT
ENV DOCKER_VERSION=19.03.6-rc2
# Fri, 07 Feb 2020 02:39:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 07 Feb 2020 02:40:00 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 07 Feb 2020 02:40:01 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 07 Feb 2020 02:40:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2020 02:40:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 07 Feb 2020 02:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2020 02:40:05 GMT
CMD ["sh"]
# Fri, 07 Feb 2020 02:40:38 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5014010b799b2f3cc6305fd21cc4b096dd28ad093e165cea5976f92ccb8c462`  
		Last Modified: Sat, 18 Jan 2020 03:03:27 GMT  
		Size: 2.3 MB (2254397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f49247ef05003d569c198c4908b849fdadd330bf360c04360ae48fd0d68b6d`  
		Last Modified: Sat, 18 Jan 2020 03:03:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9015c180d6e38c780d7ffae8ed1360cba3fc384f560587a6092c42317740318`  
		Last Modified: Fri, 07 Feb 2020 02:41:38 GMT  
		Size: 59.9 MB (59889736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa23b1a26f3312c0b9b21381b8b9ed57002efaf12478275d8dfa252dcb55926`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9659cd7acc802bc16b7c635d6c4f4829612219506fb5a8c358c7e3ffe55ae0b1`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6e1d50e985217559261a740df789190ce04f211a9669c1e08ea0cf4d40ce4`  
		Last Modified: Fri, 07 Feb 2020 02:41:15 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67e887d6c365daa130725d5bdcf3e4f4b4d8c2d3479c8677ebc0919dacd6432`  
		Last Modified: Fri, 07 Feb 2020 02:42:08 GMT  
		Size: 7.1 MB (7072804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7eb555a28260d5d2f332f7cbba3376b9c0f3af26d7ad57919fcef2d11cb293c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76601053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fee96193f4c63cc4f6c5ea730101d8581a380a567b7747a82b1b372b7433c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:50:30 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 22 Oct 2020 02:50:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 03 Dec 2020 01:39:52 GMT
ENV DOCKER_VERSION=20.10.0-rc2
# Thu, 03 Dec 2020 01:40:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-20.10.0-rc2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-20.10.0-rc2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-20.10.0-rc2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-20.10.0-rc2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 03 Dec 2020 01:40:04 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 03 Dec 2020 01:40:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 03 Dec 2020 01:40:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 03 Dec 2020 01:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 03 Dec 2020 01:40:08 GMT
CMD ["sh"]
# Thu, 03 Dec 2020 01:40:41 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85db56a0506354d758e7aa37b41ef4fff997520e3bad443abf5a31e7e71d779f`  
		Last Modified: Thu, 22 Oct 2020 02:51:51 GMT  
		Size: 2.1 MB (2061246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb67d6aeaaac2f2df73d644bd7912b4e92743c2520751feb04af77d3c76ff5b`  
		Last Modified: Thu, 22 Oct 2020 02:51:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dae5b67762b76c0efde572669044763d3b69c3bad14e0ee6d3d9f912f07ce4`  
		Last Modified: Thu, 03 Dec 2020 01:41:32 GMT  
		Size: 63.3 MB (63327989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98281331209e8408adfb9a199feb12e1bad2fce0dc2a041461fdfd7fc00c6c1f`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786af83219d1b175697b334e57b54fbda641bfbb47ae6cf8692249088282b7f7`  
		Last Modified: Thu, 03 Dec 2020 01:41:15 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2c79e2b7e6cd9911e9263c85ede6e3227ce1bf4128be7c0367ebff8d7f493`  
		Last Modified: Thu, 03 Dec 2020 01:41:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcba67047bd912ef5667bd37cd8f4c9d787f98464532b942ab796118d567983`  
		Last Modified: Thu, 03 Dec 2020 01:41:54 GMT  
		Size: 8.5 MB (8503401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:9d8a8d97c2c15e56f7d60f2dd0dd4e39081dbd83fa68c123763ab767c755f293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.1884; amd64

### `docker:rc-windowsservercore` - windows version 10.0.14393.1884; amd64

```console
$ docker pull docker@sha256:ecb33e06762179b8a50fc3204702e18b0d5631710f3c5f51e865103eea6a4413
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5372790933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03cd7d97ead7d0f7646b6c4466ae43a81295dbb77a1330ef15034c0a5df311fe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 13 Nov 2017 21:42:13 GMT
RUN Install update 10.0.14393.1884
# Wed, 15 Nov 2017 03:14:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Nov 2017 19:27:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Nov 2017 19:27:11 GMT
ENV DOCKER_CHANNEL=test
# Wed, 15 Nov 2017 19:27:12 GMT
ENV DOCKER_VERSION=17.11.0-ce-rc3
# Wed, 15 Nov 2017 19:28:13 GMT
RUN $url = ('https://download.docker.com/win/static/{0}/x86_64/docker-{1}.zip' -f $env:DOCKER_CHANNEL, $env:DOCKER_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ead9f4ead3c5a712cb213a5318f4a8bf3604bc16e16ce4f7cf0b66f7d2073282`  
		Last Modified: Tue, 18 Sep 2018 00:42:16 GMT  
		Size: 1.3 GB (1286993027 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4bd6cd94ee2a374930b7554f113d83a6d2d7c4fc6059acd6f2f60e0f29d2f26`  
		Last Modified: Wed, 15 Nov 2017 10:26:12 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a6bca6ca4a5af1b9ecee7c5d06eed25aaf7d650400c816faf8118c069fcdc6`  
		Last Modified: Wed, 15 Nov 2017 19:30:54 GMT  
		Size: 4.9 MB (4876193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5674b5976285ba892ab4f5b91e7a35ff744c5cf8dbb16ed3b48c2218b651af0`  
		Last Modified: Wed, 15 Nov 2017 19:30:53 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e6c9be57254dd1dd8a2fe6f99bf9322b4fdb1bc8e76149adf4d0e3619786b`  
		Last Modified: Wed, 15 Nov 2017 19:30:53 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a52471cc70e65173105c24345a376c017bf2459a5152685139bdca4ee598ff`  
		Last Modified: Wed, 15 Nov 2017 19:30:56 GMT  
		Size: 10.9 MB (10932220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:rc-windowsservercore-1809`

**does not exist** (yet?)

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:windowsservercore` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:e4eec512a2de95c6783851f85f38652b37fce108fb3171a6d7ace46e15f76047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull docker@sha256:00d1af6859be90ae81443923948f91023c5d9c98c3b0cd509930967d25cc3ab9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2737551444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b153058557f1f2ed347f423229e946823c10252f6f64941f859b7dcfe91bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Oct 2021 02:43:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Oct 2021 02:43:14 GMT
ENV DOCKER_VERSION=20.10.9
# Thu, 14 Oct 2021 02:43:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-20.10.9.zip
# Thu, 14 Oct 2021 02:44:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd874ac08ee111fe2cf114d0c6cde1f454b67345e21ce092adcb65291fa3d020`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 347.3 KB (347273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858e26c2cf09cac487c279dce052648a24ae14d8277ac08dd52848b19b2667e`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4954d9c2f7e3575c7c1b370f79b942a39a290b5d8969aae868db3a4b859b0218`  
		Last Modified: Thu, 14 Oct 2021 02:44:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bb3747e628070f796fc97248f1ffaf64c4dfbb3b02e00d9b52f4acdf6ec4e0`  
		Last Modified: Thu, 14 Oct 2021 02:45:09 GMT  
		Size: 50.9 MB (50881403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
