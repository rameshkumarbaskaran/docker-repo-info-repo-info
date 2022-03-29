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
