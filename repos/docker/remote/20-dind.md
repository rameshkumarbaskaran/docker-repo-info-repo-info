## `docker:20-dind`

```console
$ docker pull docker@sha256:c8a8ca4fb9841eb0cb2ef61ddceb30809f66420b089b63bf766d27c760def3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind` - linux; amd64

```console
$ docker pull docker@sha256:903b889a009176428a2c11ad1b0e72135d07fd51f56db7042b8119eafb808112
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72561611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d106d317b2ddf45e60b5ba90a53082d306fac5c96e36ef3f2ad48e9719adb`
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
# Wed, 01 Sep 2021 22:19:35 GMT
ENV DOCKER_VERSION=20.10.8
# Wed, 01 Sep 2021 22:19:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.8.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.8.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 01 Sep 2021 22:19:40 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 01 Sep 2021 22:19:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 01 Sep 2021 22:19:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 01 Sep 2021 22:19:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 01 Sep 2021 22:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 22:19:42 GMT
CMD ["sh"]
# Wed, 01 Sep 2021 22:19:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 01 Sep 2021 22:19:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 01 Sep 2021 22:19:49 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Wed, 01 Sep 2021 22:19:49 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Wed, 01 Sep 2021 22:19:50 GMT
COPY file:89f2c7c1492b0cb067fc6be48e1edf3f04c0b6063371da4a48cd4ca35aa098d7 in /usr/local/bin/ 
# Wed, 01 Sep 2021 22:19:50 GMT
VOLUME [/var/lib/docker]
# Wed, 01 Sep 2021 22:19:50 GMT
EXPOSE 2375 2376
# Wed, 01 Sep 2021 22:19:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 01 Sep 2021 22:19:50 GMT
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
	-	`sha256:f7a4137012260e097fc6b4bf6d75ba3b193acb399fb1276687303dea63ba519c`  
		Last Modified: Wed, 01 Sep 2021 22:20:40 GMT  
		Size: 61.3 MB (61283898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d92eaf14165f5a5883286b050c77b9c7022efbde954c3b7e96e92565515f0a`  
		Last Modified: Wed, 01 Sep 2021 22:20:29 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e701314a31132c239baf0de9d4922559fc419c445e13c9ce7ffd8b4518b4f98e`  
		Last Modified: Wed, 01 Sep 2021 22:20:29 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bea1be2ff281d99199cd048ef3bf1464615aec1ca9abfc20e73838913432dc0`  
		Last Modified: Wed, 01 Sep 2021 22:20:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb11622685e894072cc7fb1688ea686f6b0c903c25fda9d6f41915b279ce29`  
		Last Modified: Wed, 01 Sep 2021 22:21:00 GMT  
		Size: 6.5 MB (6521412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3448405a219f5e629e26687cfb38c611068e556983153df486257e8cf73a99`  
		Last Modified: Wed, 01 Sep 2021 22:20:59 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf064520bf422a76e00ad9efafcb13da5dbd3054b24b434db5b60bfb36f7ade6`  
		Last Modified: Wed, 01 Sep 2021 22:20:59 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d24f2f3cafbe18c3b4670d84f15a678aa265a9b90de016ff565157a15c7acc3`  
		Last Modified: Wed, 01 Sep 2021 22:20:59 GMT  
		Size: 2.6 KB (2614 bytes)  
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
