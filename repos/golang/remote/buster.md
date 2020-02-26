## `golang:buster`

```console
$ docker pull golang@sha256:b4746fbfdddf17d4bafb8f660454ada43b83cd2403d4bbcf1c2754e52b5858bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:40eb5876acf866a593ee68e5f0b48baa2c60a4789c4564346144e646d5aec6d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312051887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3474fb0f20e6da5b61e3e95a762d93005681a40e5b3d0aa787c7d2b305d2c34`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:a5ec219cbfc4e0c31e7df48cc51abd9a5b92754e15403b2ab726e25042041680 in / 
# Sat, 01 Feb 2020 17:20:39 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:18:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:19:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 02 Feb 2020 00:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:05:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 00:24:51 GMT
ENV GOLANG_VERSION=1.14
# Wed, 26 Feb 2020 00:25:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='08df79b46b0adf498ea9f320a0f23d6ec59e9003660b4c9c1ce8e5e2c6f823ca' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b5e682176d7ad3944404619a39b585453a740a2f82683e789f4279ec285b7ecd' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27' ;; 		i386) goRelArch='linux-386'; goRelSha256='cdcdab6c8d1f2dcea3bbec793352ef84db167a2eb6c60ff69e5cf94dca575f9a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b896b5eba616d27fd3bb8218de6bef557cb62221e42f73c84ae4b89cdb602dec' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='22e67470fe872c893face196f02323a11ffe89999260c136b9c50f06619e0243' ;; 		*) goRelArch='src'; goRelSha256='6d643e46ad565058c7a39dac01144172ef9bd476521f42148be59249e4b74389'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 26 Feb 2020 00:25:02 GMT
ENV GOPATH=/go
# Wed, 26 Feb 2020 00:25:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 00:25:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Feb 2020 00:25:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dc65f448a2e2f2ea557e69ed9ac65aa8ac0e16f1bce68f90de910b4d5a2f1ba1`  
		Last Modified: Sat, 01 Feb 2020 17:26:04 GMT  
		Size: 50.4 MB (50379770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346ffb2b67d7b35729673ced818325ed0ea57284e69de67f8bbc48c2bf294716`  
		Last Modified: Sun, 02 Feb 2020 00:37:48 GMT  
		Size: 7.8 MB (7811673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea4ecac934f71d68d4f5edb171f6cff42588edfa3f70ba8709be56e321eeddc`  
		Last Modified: Sun, 02 Feb 2020 00:37:49 GMT  
		Size: 10.0 MB (9996251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac92ddf84b35dac36ef6632f8d5a0c9c2d7038f6018f2d4fa1be056d90bd366`  
		Last Modified: Sun, 02 Feb 2020 00:38:05 GMT  
		Size: 51.8 MB (51791113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca6053833076bc7bd2c5666a847913b0e00163e65c5267e9f5d6e427b9f2b10`  
		Last Modified: Sun, 02 Feb 2020 14:07:58 GMT  
		Size: 68.5 MB (68523253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67fec0d1d12b45891aa76088887659617ca5224ce11421611c7da5b531897f8`  
		Last Modified: Wed, 26 Feb 2020 00:28:36 GMT  
		Size: 123.5 MB (123549701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281d1b27f53d3b6e9fd510d522ceb412e65664f5d0c746666f1c08102ea5b16a`  
		Last Modified: Wed, 26 Feb 2020 00:28:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:f21086d6d97214e2997d927a8f131b0eb520f935e7a092abc1730edeafd02255
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264364027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd528040736c502ad63d0ea25d78674b26f53fd0ee2805c9318c14c24aea32c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:38fdfcc3155e437ce162aa0ed9dcdc5893b8145e2f3ede2858ed2187d79bf718 in / 
# Wed, 26 Feb 2020 00:51:08 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:11:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 02:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:36:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:36:08 GMT
ENV GOLANG_VERSION=1.14
# Wed, 26 Feb 2020 18:36:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='08df79b46b0adf498ea9f320a0f23d6ec59e9003660b4c9c1ce8e5e2c6f823ca' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b5e682176d7ad3944404619a39b585453a740a2f82683e789f4279ec285b7ecd' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27' ;; 		i386) goRelArch='linux-386'; goRelSha256='cdcdab6c8d1f2dcea3bbec793352ef84db167a2eb6c60ff69e5cf94dca575f9a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b896b5eba616d27fd3bb8218de6bef557cb62221e42f73c84ae4b89cdb602dec' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='22e67470fe872c893face196f02323a11ffe89999260c136b9c50f06619e0243' ;; 		*) goRelArch='src'; goRelSha256='6d643e46ad565058c7a39dac01144172ef9bd476521f42148be59249e4b74389'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 26 Feb 2020 18:36:31 GMT
ENV GOPATH=/go
# Wed, 26 Feb 2020 18:36:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 18:36:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Feb 2020 18:36:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3182cf45068cd9734abd8e38dedbb9930ede35ee8c11376ca2684e86f9a1aa85`  
		Last Modified: Wed, 26 Feb 2020 01:07:03 GMT  
		Size: 45.9 MB (45862691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b727ab99a6a790544e023dbba8625605266dd84b3a69acaa541144ad632f4ba`  
		Last Modified: Wed, 26 Feb 2020 02:33:37 GMT  
		Size: 7.1 MB (7096560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab9435f7cf0c46bc6621020fd229e7de8baa61f71059cb9a34b9f681caed9aa`  
		Last Modified: Wed, 26 Feb 2020 02:33:38 GMT  
		Size: 9.3 MB (9343152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2ad791c8431e9b6624239d0b1fee2523df27584a263ec1d8d525201bb44087`  
		Last Modified: Wed, 26 Feb 2020 02:34:01 GMT  
		Size: 47.3 MB (47315030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a879613e63b581fbc31eac1107e244caddc95346001501421594071d0c92b42`  
		Last Modified: Wed, 26 Feb 2020 18:45:16 GMT  
		Size: 53.1 MB (53077536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2de35f8fafe33997a98991002a9f1401f32a015f95fd83fcd50c8851494f151`  
		Last Modified: Wed, 26 Feb 2020 18:45:34 GMT  
		Size: 101.7 MB (101668902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41479b8b145b82ec920e8b18bc9bffa93188b3df23e5a48c8654681be1e3c60`  
		Last Modified: Wed, 26 Feb 2020 18:45:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:15ead6396da635b24be4fe8302b5c35fe63252998eeefe164c1402bc04c59b1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282254050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c3affdcbb62c255d3306c4474a0f3ecd40e7daa89bce2f952454bb25fb1c77`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:50 GMT
ADD file:b423f4b0ed41dfe1334031fe9b21f7e1c88ccb031d7e8f2ff165d618323424d7 in / 
# Sat, 01 Feb 2020 16:40:53 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:18:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:08:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:01:26 GMT
ENV GOLANG_VERSION=1.14
# Wed, 26 Feb 2020 01:01:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='08df79b46b0adf498ea9f320a0f23d6ec59e9003660b4c9c1ce8e5e2c6f823ca' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b5e682176d7ad3944404619a39b585453a740a2f82683e789f4279ec285b7ecd' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27' ;; 		i386) goRelArch='linux-386'; goRelSha256='cdcdab6c8d1f2dcea3bbec793352ef84db167a2eb6c60ff69e5cf94dca575f9a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b896b5eba616d27fd3bb8218de6bef557cb62221e42f73c84ae4b89cdb602dec' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='22e67470fe872c893face196f02323a11ffe89999260c136b9c50f06619e0243' ;; 		*) goRelArch='src'; goRelSha256='6d643e46ad565058c7a39dac01144172ef9bd476521f42148be59249e4b74389'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 26 Feb 2020 01:02:04 GMT
ENV GOPATH=/go
# Wed, 26 Feb 2020 01:02:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 01:02:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Feb 2020 01:02:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bc03a7ced18fc43ea9523dfb256d2c3fbb835dc0bb54bdb7fd309edf936a87e7`  
		Last Modified: Sat, 01 Feb 2020 16:46:06 GMT  
		Size: 49.2 MB (49171687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9d528c1473d79c18b401d44ca06b9733d9c51a8699b98e8325c9de60b9739`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 7.7 MB (7680993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981400d5d268dc989681d5f308b7d2e381809f0bcc82429f443f7539cf6117ba`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 10.0 MB (9983754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2d547b8bc79a444406e56d724fb7d961c953e7f2797de4f55b29abee5605f`  
		Last Modified: Sat, 01 Feb 2020 17:35:22 GMT  
		Size: 52.1 MB (52102938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a606fada5847b27d4f74a29fdf4fb7b8ab9430f363c3f35669cabe7a0daf2`  
		Last Modified: Sun, 02 Feb 2020 11:13:40 GMT  
		Size: 62.4 MB (62390640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc718f4d41f1762235d16fc1abf3b5daaf251167e6d02607052b8d42d0c9b877`  
		Last Modified: Wed, 26 Feb 2020 01:10:43 GMT  
		Size: 100.9 MB (100923882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93608669f53e3d7dee379862be3f09dfc8f92f322bb59e112448fec081fef0`  
		Last Modified: Wed, 26 Feb 2020 01:10:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:6168941901c9b32d3f19f022442ca23e36f2177f733c8fbb59d62580f60dd9ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301056498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9068b7066c0cdfe9729952263d2d73e22c5b64010e9e94c173522b0ff49ad192`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:31:58 GMT
ADD file:1deff975480520310bf2c8d3708554d98c696f82689f0b67f9a834217c861803 in / 
# Wed, 26 Feb 2020 00:31:59 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:07:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:07:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:08:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 19:35:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 19:35:50 GMT
ENV GOLANG_VERSION=1.14
# Wed, 26 Feb 2020 19:36:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='08df79b46b0adf498ea9f320a0f23d6ec59e9003660b4c9c1ce8e5e2c6f823ca' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b5e682176d7ad3944404619a39b585453a740a2f82683e789f4279ec285b7ecd' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27' ;; 		i386) goRelArch='linux-386'; goRelSha256='cdcdab6c8d1f2dcea3bbec793352ef84db167a2eb6c60ff69e5cf94dca575f9a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b896b5eba616d27fd3bb8218de6bef557cb62221e42f73c84ae4b89cdb602dec' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='22e67470fe872c893face196f02323a11ffe89999260c136b9c50f06619e0243' ;; 		*) goRelArch='src'; goRelSha256='6d643e46ad565058c7a39dac01144172ef9bd476521f42148be59249e4b74389'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 26 Feb 2020 19:36:04 GMT
ENV GOPATH=/go
# Wed, 26 Feb 2020 19:36:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 19:36:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Feb 2020 19:36:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9450e7c48681b3ba36935d4e7d891b4b180d4d223a6c938faacb41402857ebd3`  
		Last Modified: Wed, 26 Feb 2020 00:38:12 GMT  
		Size: 51.1 MB (51146129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3b9049fe76610ee534524c2087947a0c92f9d674f7395a2031161e4e448a57`  
		Last Modified: Wed, 26 Feb 2020 01:27:14 GMT  
		Size: 8.0 MB (7981680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e618476b0d787bc3028ca73062991dd8c2c5c71d93e2932eb7f14257541bc005`  
		Last Modified: Wed, 26 Feb 2020 01:27:15 GMT  
		Size: 10.3 MB (10338439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd3ac0f3869d874323567fd1fdb72f8976b62d2dd8d3c9761ab065b2426a6d9`  
		Last Modified: Wed, 26 Feb 2020 01:27:39 GMT  
		Size: 53.4 MB (53382038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c725561cb3eb3e580dbd8f82120f0faab46c6e7eb4461b8c8c9d254184e30d1`  
		Last Modified: Wed, 26 Feb 2020 19:38:24 GMT  
		Size: 73.5 MB (73472469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486dce3795ef139d4e505ff0bbaaafa5def9ea93bf297c4967ebd1ad79cf3c06`  
		Last Modified: Wed, 26 Feb 2020 19:38:29 GMT  
		Size: 104.7 MB (104735616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0b6f37442425dd57ea68a0c6b4ccedae386bfa108446e1f840676078ac8547`  
		Last Modified: Wed, 26 Feb 2020 19:38:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; ppc64le

```console
$ docker pull golang@sha256:ba21c1179e475ff714bedcb67b20bb7682597291871ed78f09671bb7e7a3efbf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303678877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc9ffe4c0d0fb74b2bf5d5a29fdf919f4938f810056e44f77b997b11d9cab4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:17:37 GMT
ADD file:8e8c5417abc372541fe34cddec6fe8625ded93da51d1f5488e0aece309a3fd25 in / 
# Sat, 01 Feb 2020 17:17:45 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:37:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:38:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:39:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:32:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 00:36:52 GMT
ENV GOLANG_VERSION=1.14
# Wed, 26 Feb 2020 00:37:21 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='08df79b46b0adf498ea9f320a0f23d6ec59e9003660b4c9c1ce8e5e2c6f823ca' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b5e682176d7ad3944404619a39b585453a740a2f82683e789f4279ec285b7ecd' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27' ;; 		i386) goRelArch='linux-386'; goRelSha256='cdcdab6c8d1f2dcea3bbec793352ef84db167a2eb6c60ff69e5cf94dca575f9a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b896b5eba616d27fd3bb8218de6bef557cb62221e42f73c84ae4b89cdb602dec' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='22e67470fe872c893face196f02323a11ffe89999260c136b9c50f06619e0243' ;; 		*) goRelArch='src'; goRelSha256='6d643e46ad565058c7a39dac01144172ef9bd476521f42148be59249e4b74389'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 26 Feb 2020 00:37:28 GMT
ENV GOPATH=/go
# Wed, 26 Feb 2020 00:37:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 00:37:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Feb 2020 00:37:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a2d5a5ee40c1df8706e6db684b090e0e4297581ff38256a81222ea8be61180fc`  
		Last Modified: Sat, 01 Feb 2020 17:25:27 GMT  
		Size: 54.1 MB (54132833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f35d9825c38e7e0c3f571e8abe513b3b11599bd64a853ace5494e8c1ebe12a`  
		Last Modified: Sat, 01 Feb 2020 19:17:26 GMT  
		Size: 8.3 MB (8252196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e6d793f7577bc28e3d8da62385244985a340fe31c9eaa920a54185f9d46eb8`  
		Last Modified: Sat, 01 Feb 2020 19:17:26 GMT  
		Size: 10.7 MB (10727116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97a0399500f41c90805413f9dd183cb0036f1446b766e62ad6310e2357d9b8`  
		Last Modified: Sat, 01 Feb 2020 19:18:21 GMT  
		Size: 57.4 MB (57392303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc0eec775fb25dc9e4e753c5a1513055bc30c10976f23b214a4963e8c62e384`  
		Last Modified: Sun, 02 Feb 2020 14:38:40 GMT  
		Size: 73.4 MB (73427259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646fdc7d6331b722f52363eef48fb8fd772461c7af7f7264fd8fdf17ad327d8d`  
		Last Modified: Wed, 26 Feb 2020 00:43:20 GMT  
		Size: 99.7 MB (99747014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877b3617c80b0e76f95da0120c070d3635879364be129d68a1409e6d49475169`  
		Last Modified: Wed, 26 Feb 2020 00:42:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; s390x

```console
$ docker pull golang@sha256:bae42bbc0e0bb4321a0e1ef05e08f146f6b700b5fc2ea52fb11855546cdd9ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279411717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f05de541d5447cb84d97f1dcf5aee389c3ef5cede868d349fc4fe7b1946990`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:42:32 GMT
ADD file:80536bfff518f6b425ad359b86a124f79ccdc82deb3e648f1746a7c87a1fcad0 in / 
# Wed, 26 Feb 2020 00:42:35 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:33:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:33:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 04:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:20:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:20:47 GMT
ENV GOLANG_VERSION=1.14
# Wed, 26 Feb 2020 09:21:09 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='08df79b46b0adf498ea9f320a0f23d6ec59e9003660b4c9c1ce8e5e2c6f823ca' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='b5e682176d7ad3944404619a39b585453a740a2f82683e789f4279ec285b7ecd' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='cd813387f770c07819912f8ff4b9796a4e317dee92548b7226a19e60ac79eb27' ;; 		i386) goRelArch='linux-386'; goRelSha256='cdcdab6c8d1f2dcea3bbec793352ef84db167a2eb6c60ff69e5cf94dca575f9a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='b896b5eba616d27fd3bb8218de6bef557cb62221e42f73c84ae4b89cdb602dec' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='22e67470fe872c893face196f02323a11ffe89999260c136b9c50f06619e0243' ;; 		*) goRelArch='src'; goRelSha256='6d643e46ad565058c7a39dac01144172ef9bd476521f42148be59249e4b74389'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Wed, 26 Feb 2020 09:21:20 GMT
ENV GOPATH=/go
# Wed, 26 Feb 2020 09:21:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 09:21:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Feb 2020 09:21:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a3603da42bb9e22573006a7f894b198954caeab529e2e041660e12c4fe62462`  
		Last Modified: Wed, 26 Feb 2020 00:47:26 GMT  
		Size: 49.0 MB (48958029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a7b142236e4c473f4fd19a0485f74364510f658dc999627e6c41f4684a50d5`  
		Last Modified: Wed, 26 Feb 2020 04:47:32 GMT  
		Size: 7.4 MB (7382213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c5965845a6f2fd1bfaa3a4814a17655d46330b5f60ed861daaa390d5b82a2`  
		Last Modified: Wed, 26 Feb 2020 04:47:37 GMT  
		Size: 9.9 MB (9882220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942858cf91c54d2d1efa88f24491ba2b93cd15ed968d4f5e193c5e26ca4236e1`  
		Last Modified: Wed, 26 Feb 2020 04:47:51 GMT  
		Size: 51.3 MB (51327256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4f5bb4516c3283cf2b8ab45a3231407f9577453fc6a45afc4bdfd62fa05901`  
		Last Modified: Wed, 26 Feb 2020 09:24:29 GMT  
		Size: 56.7 MB (56672934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854d6dc369b604fde2f10ceaf36edac56eb800ab27c01274cf8b910f6aa7f51b`  
		Last Modified: Wed, 26 Feb 2020 09:24:33 GMT  
		Size: 105.2 MB (105188909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d337c53cd5c06be81e5ad800f754e5799d118b8516c148099a51970a7ff805e`  
		Last Modified: Wed, 26 Feb 2020 09:24:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
