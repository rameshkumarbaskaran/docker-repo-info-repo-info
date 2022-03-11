## `docker:git`

```console
$ docker pull docker@sha256:26780f07a886b87084ac6f1dfa3fd04694083f9b495acc1ceed49c4d9aafb05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:git` - linux; amd64

```console
$ docker pull docker@sha256:7383e8c2efcd6846670dd96ca1b6af84b7a4098fd778b85cee0ae2739301a79c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76237387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f328899fc7a17e58951f5523f603df43687ea162ad1f8f04eed66b876e9480ea`
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
# Fri, 11 Mar 2022 00:19:37 GMT
ENV DOCKER_VERSION=20.10.13
# Fri, 11 Mar 2022 00:19:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Mar 2022 00:19:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Mar 2022 00:19:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Mar 2022 00:19:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Mar 2022 00:19:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Mar 2022 00:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Mar 2022 00:19:42 GMT
CMD ["sh"]
# Fri, 11 Mar 2022 00:20:00 GMT
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
	-	`sha256:fdbbd0a7b1dec526be119d73f0018052afa23e65ea79e09049a54a5954f2a374`  
		Last Modified: Fri, 11 Mar 2022 00:20:32 GMT  
		Size: 64.6 MB (64612571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317ecb07c86c68358ba3d763bea251b7baf1befde793d08f074abf2743a388dc`  
		Last Modified: Fri, 11 Mar 2022 00:20:21 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52850491ed6a707afb12e76035b1a36f408c071e00d1de77b26ec2cb178c9a8a`  
		Last Modified: Fri, 11 Mar 2022 00:20:21 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2b84e11d9e63efd7d7cad8459ac6f5326f44d93991a59380b186824079bdf`  
		Last Modified: Fri, 11 Mar 2022 00:20:21 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc827496373a4a4176b9c5e48d8ea6bb5823b745c62a5ddd68e6b201ae7341d`  
		Last Modified: Fri, 11 Mar 2022 00:21:30 GMT  
		Size: 6.8 MB (6824133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1b0ddebf5e4263b6e1d58479e9aaeec0c9246480f6722df6df2e6650b3fb92a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70165369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ea32ca04049d38f105491861a124076410406bd5987d2f1d6254767f6f7d5d`
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
# Fri, 11 Mar 2022 00:39:35 GMT
ENV DOCKER_VERSION=20.10.13
# Fri, 11 Mar 2022 00:39:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.13.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.13.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.13.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.13.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 11 Mar 2022 00:39:41 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 11 Mar 2022 00:39:42 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 11 Mar 2022 00:39:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 11 Mar 2022 00:39:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 11 Mar 2022 00:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Mar 2022 00:39:45 GMT
CMD ["sh"]
# Fri, 11 Mar 2022 00:40:26 GMT
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
	-	`sha256:6561b7705fefb0b49b335b56a2b49274f9ff6b55220626bd898f2c2d0be00eb4`  
		Last Modified: Fri, 11 Mar 2022 00:41:15 GMT  
		Size: 58.6 MB (58565241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d2cb917414c2052fac63a7dedd59be928c94d5cc572b24406d235f6990010`  
		Last Modified: Fri, 11 Mar 2022 00:41:06 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250af0478077d2d3407f9444430c3a215d0d39ff3a77f230331773e1c3f44daf`  
		Last Modified: Fri, 11 Mar 2022 00:41:06 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a445181e9f39b44e6f761cd46ca2a0d56de49eb3c85bd2b43086ca8141bbb9fd`  
		Last Modified: Fri, 11 Mar 2022 00:41:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106fd0f2e5cee984d907f022557607f7315b84febe31d09c9fe4aedcab520de6`  
		Last Modified: Fri, 11 Mar 2022 00:42:24 GMT  
		Size: 6.9 MB (6933319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
