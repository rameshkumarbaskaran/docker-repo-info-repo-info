## `docker:20-dind`

```console
$ docker pull docker@sha256:8f4e9ddda1049e6935f9fc7f5cad0bd1001fbf59188616f19b620fd7b6e95ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:12521ff42db0d1e1d99f89c7dea6aa6e2d028c20cb42dad8285503735ddf678d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.3 MB (80305670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7569a61fe0d5af655280b516bb2654a1ef03f7a3d67549543b65d81dbeea372e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 12:37:38 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 17 Dec 2020 12:37:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Jan 2021 20:28:24 GMT
ENV DOCKER_VERSION=20.10.2
# Tue, 05 Jan 2021 20:28:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Jan 2021 20:28:30 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Jan 2021 20:28:30 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Jan 2021 20:28:30 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Jan 2021 20:28:31 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Jan 2021 20:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jan 2021 20:28:32 GMT
CMD ["sh"]
# Tue, 05 Jan 2021 20:28:38 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Jan 2021 20:28:39 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Jan 2021 20:28:40 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Tue, 05 Jan 2021 20:28:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Jan 2021 20:28:41 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Tue, 05 Jan 2021 20:28:41 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Jan 2021 20:28:41 GMT
EXPOSE 2375 2376
# Tue, 05 Jan 2021 20:28:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Jan 2021 20:28:42 GMT
CMD []
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7dc993c79e722bfe2e7f64e7ae30964b200440f94deec6b702314e2c4e233a`  
		Last Modified: Thu, 17 Dec 2020 12:40:18 GMT  
		Size: 2.0 MB (2039162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d95e4997fdf86ea798b96fad5c5eab74bed43cd512a3ecd5dfb4f48bc2371`  
		Last Modified: Thu, 17 Dec 2020 12:40:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae283de69b7d7622815d40f6d45c9b05f3858e760ae29ef158e4a4f45bfc07d7`  
		Last Modified: Tue, 05 Jan 2021 20:30:01 GMT  
		Size: 69.5 MB (69463264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1962c7344fe5724fe1dea0edd44fb0acc6b4bd36d4eed59be51bbd83ad33de71`  
		Last Modified: Tue, 05 Jan 2021 20:29:47 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7a3367c785715e0d08d7fc56b8c6b0bc73c48b438626af67c55534054c629d`  
		Last Modified: Tue, 05 Jan 2021 20:29:47 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e259227d4380d66b9df6b6334025d16153729808f8c42d71dd1fc1d2106632c`  
		Last Modified: Tue, 05 Jan 2021 20:29:47 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38001158edd741c65a3ed125131c9b512015100212693852be53b476dc7b43c`  
		Last Modified: Tue, 05 Jan 2021 20:30:11 GMT  
		Size: 6.0 MB (5997617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837d641dcbc635770b022eaf0f3d0872e35f5d5757f12840588a23e386d0a182`  
		Last Modified: Tue, 05 Jan 2021 20:30:10 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a5813f12bba67bf98a1e61563228898143a9bddc98cd424e06eb0c0fef5b56`  
		Last Modified: Tue, 05 Jan 2021 20:30:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709f1e4daeb7f42a1f90d3cfbdafb7d75a6db94c49053c60894fd198c5dbb81`  
		Last Modified: Tue, 05 Jan 2021 20:30:09 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:009bdea1b7cf4de7f5f7febf8cce1f322b92598927318c78cd2c012d8c0dc866
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74330730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d0c159886920afd8281e6a9c25adfcd96a84c0c040aec2195a05c958ab8996`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Fri, 18 Dec 2020 21:03:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Fri, 18 Dec 2020 21:03:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Jan 2021 20:56:23 GMT
ENV DOCKER_VERSION=20.10.2
# Tue, 05 Jan 2021 20:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.2.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Jan 2021 20:56:44 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Jan 2021 20:56:44 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Jan 2021 20:56:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Jan 2021 20:56:47 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Jan 2021 20:56:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jan 2021 20:56:48 GMT
CMD ["sh"]
# Tue, 05 Jan 2021 20:57:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Jan 2021 20:57:02 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Jan 2021 20:57:03 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Tue, 05 Jan 2021 20:57:05 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Jan 2021 20:57:06 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Tue, 05 Jan 2021 20:57:06 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Jan 2021 20:57:07 GMT
EXPOSE 2375 2376
# Tue, 05 Jan 2021 20:57:08 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Jan 2021 20:57:09 GMT
CMD []
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687389c362907d6cbb42307b7282adbf11252d32f65daf6856fcd793682d51e4`  
		Last Modified: Fri, 18 Dec 2020 21:05:45 GMT  
		Size: 2.1 MB (2061419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e28978939c32b9c7a64f86fcc5fb90cc8443ba29608c41cd5cd6e1105a52b5`  
		Last Modified: Fri, 18 Dec 2020 21:05:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bd9c9fe1b114242c2a05ff2324cb558a4ea9f13ee3bb217b064840746994f1`  
		Last Modified: Tue, 05 Jan 2021 20:58:18 GMT  
		Size: 63.6 MB (63567013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5a7137269a5d82bd93feca2c70ef57151436f679154c45adfd36f19f42afb8`  
		Last Modified: Tue, 05 Jan 2021 20:57:57 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650eeba05d503524e9e4c82701a3d62ec4cbb8dd3566e9394dfc123d2066eda0`  
		Last Modified: Tue, 05 Jan 2021 20:57:57 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283d3dba4d5b3bf9559384bd78c7130fa5d031df18b8e969a14226ea37a13aa5`  
		Last Modified: Tue, 05 Jan 2021 20:57:57 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e78a4172ef96f32b533cbf6801fe149da1b779d89840d83fe886177926f45a`  
		Last Modified: Tue, 05 Jan 2021 20:58:33 GMT  
		Size: 6.0 MB (5986631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1598bd0109f36fbb2b85347bc0cf0a84ab301f28328d2951839311586e8437bd`  
		Last Modified: Tue, 05 Jan 2021 20:58:31 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af010b07f6e310392fcc7c20186421464c4d501cbd34703ebbe38989865183ac`  
		Last Modified: Tue, 05 Jan 2021 20:58:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19648213b3243bb843981aafdcec6d0985a973d0d3aa90bec97d43313946969`  
		Last Modified: Tue, 05 Jan 2021 20:58:31 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
