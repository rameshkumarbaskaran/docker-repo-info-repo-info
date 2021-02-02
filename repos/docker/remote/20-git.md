## `docker:20-git`

```console
$ docker pull docker@sha256:71b3378741289cdc74c9d82334b0e565f16191be49ab624f22be86111e8d47ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-git` - linux; amd64

```console
$ docker pull docker@sha256:c3ecec7652aedd51401a58920553b3666e2243250388eeba47a744f5613ac504
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82615376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6623ebd8af8380d0274da05d7db6d66e5f56fc6d462cd29d6a0fcb48aa8112b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

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
# Tue, 05 Jan 2021 20:28:58 GMT
RUN apk add --no-cache git
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
	-	`sha256:6ef141bca7ba2e1de472b7f3d9a6801ad9dcb3a6f5f7d09569f89d709e3907dd`  
		Last Modified: Tue, 05 Jan 2021 20:30:36 GMT  
		Size: 8.3 MB (8312053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f50e160aec2b3c2084868d88c8fd12405b7c821b4d1eb3f6d0f212f7ab229ca4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74828139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f1bd1f86381bfb83fdd88698657ba8dfb6e246bf7c53e4d037d743306d3e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 28 Jan 2021 23:39:33 GMT
ADD file:fecabe41deaeb72acdd63023566d87ae48b013ef80c97fdd993b55d6c727da93 in / 
# Thu, 28 Jan 2021 23:39:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Feb 2021 01:07:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Tue, 02 Feb 2021 01:07:30 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Feb 2021 01:07:31 GMT
ENV DOCKER_VERSION=20.10.3
# Tue, 02 Feb 2021 01:07:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.3.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 02 Feb 2021 01:07:39 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 02 Feb 2021 01:07:40 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 02 Feb 2021 01:07:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 02 Feb 2021 01:07:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 02 Feb 2021 01:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Feb 2021 01:07:43 GMT
CMD ["sh"]
# Tue, 02 Feb 2021 01:08:10 GMT
RUN apk add --no-cache git
```

-	Layers:
	-	`sha256:2914792bc417803b2106001990194cc00cdd4b6fd97cd21a368f26148bc8e722`  
		Last Modified: Thu, 28 Jan 2021 23:40:10 GMT  
		Size: 2.7 MB (2711261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756c677dae0e125b184b702e022e81dc6b58d852d919ce87d18f784a02a7a061`  
		Last Modified: Tue, 02 Feb 2021 01:09:23 GMT  
		Size: 2.1 MB (2068024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318712088e33177a73cbc991c387c8cab1c194c7c0ab69e07303a3121a2298dc`  
		Last Modified: Tue, 02 Feb 2021 01:09:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ea4215e87a19277d3ad5191bd33bbc874d53668f5bab1d078e9be7be8fb12`  
		Last Modified: Tue, 02 Feb 2021 01:09:39 GMT  
		Size: 63.6 MB (63572234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afbccbf4e53fe57125e562dbb66792d01e4166e117597e31e419cab29894e3d`  
		Last Modified: Tue, 02 Feb 2021 01:09:21 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b11151c2bc89ee34a665c25ced3ff48ae5a22718436d3ece90d6312884a09aa`  
		Last Modified: Tue, 02 Feb 2021 01:09:21 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6a033d54e332e1f5c93adab630e5bd10f71a41174a5969dd6e3cac4ca58f5`  
		Last Modified: Tue, 02 Feb 2021 01:09:21 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a55270903e654573ef5353863992734f533829903b93363b870b2e95ae7ed8`  
		Last Modified: Tue, 02 Feb 2021 01:10:02 GMT  
		Size: 6.5 MB (6474756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
