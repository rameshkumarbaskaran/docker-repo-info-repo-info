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
