## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d581512e4b4bac2ba289cae190e928074fc5f0bf4c8c71f309314709ebe0a8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ec2140865f2bc0705f6d17a575b2036e5d60a768007321245faa9eebdc031488
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92828157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ff4e7c8157ca219e02e8525c28f1a8350b01b405a72860e2c926a26a8e9d6b`
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
# Wed, 01 Sep 2021 22:19:55 GMT
RUN apk add --no-cache iproute2
# Wed, 01 Sep 2021 22:19:56 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Wed, 01 Sep 2021 22:19:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Wed, 01 Sep 2021 22:19:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.8.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.8.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Wed, 01 Sep 2021 22:19:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Wed, 01 Sep 2021 22:20:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 01 Sep 2021 22:20:00 GMT
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
	-	`sha256:34ee8eb2774788b07752bfe9bada2565d0759149471b1e1184fe1b8b9b723291`  
		Last Modified: Wed, 01 Sep 2021 22:21:20 GMT  
		Size: 1.1 MB (1148735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4811cca51263afbb69cb08a00b9ced312530c69efdd89d18432a10d708b9793`  
		Last Modified: Wed, 01 Sep 2021 22:21:20 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196b78c6ec13dfea9317ce19a5c0297ffa1b7bb71c9cbdcbd8898a7d1c488fe`  
		Last Modified: Wed, 01 Sep 2021 22:21:20 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951aa128211fa2e81475296d3178c72f82de1b9b0fca6577a41522b421d33333`  
		Last Modified: Wed, 01 Sep 2021 22:21:23 GMT  
		Size: 19.1 MB (19116094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b58b08848076b0b593d64fb903397d255b9467bb9f93f4492d852beb23532af`  
		Last Modified: Wed, 01 Sep 2021 22:21:20 GMT  
		Size: 219.0 B  
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
