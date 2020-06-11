## `golang:rc-buster`

```console
$ docker pull golang@sha256:664bc01be21b62f1d87727f2cf51ab81a0fe0e3b2292578e4c5ca67f6bcf0d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:rc-buster` - linux; amd64

```console
$ docker pull golang@sha256:c9933d031d66ea1a32d1336184e34935e0d99391744c41483abc8f4f4a210474
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312051096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e522536ac2202af6cfcc4956a3d1912f1c59b7f4305042053e6805a7552997`
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
# Thu, 06 Feb 2020 00:51:02 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 00:51:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 00:51:15 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 00:51:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 00:51:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 00:51:16 GMT
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
	-	`sha256:fd94eeff2da380ac4980b9e134d0fb1bcc74840627cdb21ccf8a4c8292d61165`  
		Last Modified: Thu, 06 Feb 2020 00:55:29 GMT  
		Size: 123.5 MB (123548911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37c020160601da58dc55b8da5665296b7dbdd1b4d6155b132b1c547c391652`  
		Last Modified: Thu, 06 Feb 2020 00:55:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:fedc38a6a2f72254a3fd0e9ad55f4c54f78e0f69b54414f6512cf909b6a88e21
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264276609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbfc9fa38b3e0d39a13bc9651ecc0554903c644a7392233173a29be476f6a2a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:06 GMT
ADD file:a57a312731f174c4b03031908ff95f49d7055d8c196439f0ed07ed9c4834d993 in / 
# Sat, 01 Feb 2020 17:00:08 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:00:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 14:30:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Feb 2020 01:22:46 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 01:23:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 01:23:48 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 01:23:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 01:23:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 01:23:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9bbb41bca8c6254da5088d03354297b1309dc75c2ccc738416025f89709ae5ee`  
		Last Modified: Sat, 01 Feb 2020 17:07:28 GMT  
		Size: 45.9 MB (45859700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239e4acdbc2ab88c89aa359fbab11429ea6d7bd93ea589a22c6bbb833ff82b93`  
		Last Modified: Sat, 01 Feb 2020 18:25:50 GMT  
		Size: 7.1 MB (7096223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6b4707a3c3aff9cb939fc058b869c5412e78c37e43eb0b653565460495537`  
		Last Modified: Sat, 01 Feb 2020 18:25:50 GMT  
		Size: 9.3 MB (9343278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e096c4fc8c629edca6da3ce5a9e95288512cb11e3d3d01a6e49078d19c2acca`  
		Last Modified: Sat, 01 Feb 2020 18:26:13 GMT  
		Size: 47.3 MB (47315591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca29eebbe47938ede4b91d684551d2cd027b2947a5aa2dffb6b64aee43fef432`  
		Last Modified: Sun, 02 Feb 2020 14:36:25 GMT  
		Size: 53.0 MB (52996899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484bc6c7846d4e8a4f750cb73fc9cc4e086cc81a2d67f5a9929f969e54939413`  
		Last Modified: Thu, 06 Feb 2020 01:30:47 GMT  
		Size: 101.7 MB (101664762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb18321ce4e5e0c8d5b563982e189855c1f5d5431566cfc5dc2d159f8b3b628`  
		Last Modified: Thu, 06 Feb 2020 01:29:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4c698ad68998a3a6f9fabdb9bb91354e8304990f75786db3212b3859a0d9d01d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282251561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5602da4b0978a97726fb0bc39626a6e6e8d81e322ed593f2468e0ece32760`
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
# Thu, 06 Feb 2020 01:40:08 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 01:40:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 01:40:41 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 01:40:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 01:40:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 01:40:54 GMT
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
	-	`sha256:f930dfbaa1cf7b2092ecaeb4f4b4cc640e3667a209d0c48efed84fea4b4147ae`  
		Last Modified: Thu, 06 Feb 2020 01:45:38 GMT  
		Size: 100.9 MB (100921394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2462e9ebdbcec6bb610cbb0178b28ccdb578548a4d35b05ad8e41f9eb8c58d`  
		Last Modified: Thu, 06 Feb 2020 01:41:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; 386

```console
$ docker pull golang@sha256:a861102c4bfca6622c9d994d0294254f6aa8d060bfc7c6afcbaddc514c5a3b72
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300973757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba657f2565c85e7a967509a90e28922923395adab20902fd0c1fcbeb7d8fbf5e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:21 GMT
ADD file:b637f96d557a570f8ab83b28f7b9cdd128958359dd30dc2e03df70b799e132aa in / 
# Sat, 01 Feb 2020 16:39:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:23:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:24:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:24:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:42:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Feb 2020 00:38:30 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 00:38:46 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 00:38:47 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 00:38:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 00:38:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 00:38:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2b34644a479c82db66a603c0b0a1d990911345f8646498fa9b050f306d0e6bf2`  
		Last Modified: Sat, 01 Feb 2020 16:44:10 GMT  
		Size: 51.1 MB (51141949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f611c9392c4fe86735b477d61fda0e95ea77486175a737114c51586ecce86`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 8.0 MB (7981506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69713757cc2d87c3255331d40f5061a73ef412208961f1ddd67a59a375397fda`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 10.3 MB (10338479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956cf07a321afcfed99809a380a1905660e378188fd33d97f136551450be347a`  
		Last Modified: Sat, 01 Feb 2020 17:42:36 GMT  
		Size: 53.4 MB (53380753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159d58090764ecf1adf8cab45ec531c80c784798e49d41a42e10b8738ef96ef6`  
		Last Modified: Sun, 02 Feb 2020 10:45:51 GMT  
		Size: 73.4 MB (73391925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196634ae150608dc0afa1e3b41b64a5041d0c11c80364f4f71e36f8a8ffeb752`  
		Last Modified: Thu, 06 Feb 2020 00:43:16 GMT  
		Size: 104.7 MB (104739020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16c942410a76e76b389a4df91acf568eefc2f73965efcf3c1454c3ab8b9b1a7`  
		Last Modified: Thu, 06 Feb 2020 00:42:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:0bcfa39885d1de46d16d7e304d403c54a16595be6b57bed876a2f324322aa1ce
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303687751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786772ab83dbd222dc8dfd077e473bb073d34e818787044ae41f453ef9ec6fe`
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
# Thu, 06 Feb 2020 00:37:52 GMT
ENV GOLANG_VERSION=1.14rc1
# Thu, 06 Feb 2020 00:38:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='69398d41e5f6b87cdf3969aae665be4dfd3cc2ef36a61ab47a261f96130ed788' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='bfe041f7d2a62f895f2d11703a29bdd31a48cca9a3c36418d59680bc1cbb8a6d' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='a5509448b06f02f5198fe8bbf5af88ab483af9c46f231c3f308748016fbc32c9' ;; 		i386) goRelArch='linux-386'; goRelSha256='831087aa0eba8b6dfa221036d00641613996ac66d7c635f1e34c53d5f0922623' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='fe1bf34d2b117d785f2fb33151c44ca8bc2188678c9e903fa0ad30573547b412' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='2302fa0e30144a969cb1879eed8aeb9a82c2b520fcda8aebbb20a539ad427c25' ;; 		*) goRelArch='src'; goRelSha256='76188ea84e95baa502d058c9598020c7654d6adaf40b82cabcf57c68df19963a'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 06 Feb 2020 00:38:30 GMT
ENV GOPATH=/go
# Thu, 06 Feb 2020 00:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2020 00:38:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Feb 2020 00:38:47 GMT
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
	-	`sha256:5af256a452250034bf0eed2b60c2c7eb23187e682dff40e21bc15c4fcaf97a0b`  
		Last Modified: Thu, 06 Feb 2020 00:43:45 GMT  
		Size: 99.8 MB (99755889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cb146d553e59584fe48ad92219660bfce39b8d8bd909ce3f4ee5fc77d71a19`  
		Last Modified: Thu, 06 Feb 2020 00:42:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; s390x

```console
$ docker pull golang@sha256:e86db1228d835597e570c30d366161a26a7f8c697704ba23e12565c67528867d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278778052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d9e0493f2a7ff3d0a92fa7df9d6995e78fd9a07219ae50447de857ef616e85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:21 GMT
ADD file:525b5566f1fb9dfef74a4f49170a50bba0f0ed22a8bd627a8f802803236f1db8 in / 
# Tue, 09 Jun 2020 01:42:23 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:09:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:09:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 11:56:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jun 2020 22:55:05 GMT
ENV GOLANG_VERSION=1.15beta1
# Thu, 11 Jun 2020 22:55:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='11814b7475680a09720f3de32c66bca135289c8d528b2e1132b0ce56b3d9d6d7' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='d4da5c06097be8d14aeeb45bf8440a05c82e93e6de26063a147a31ed1d901ebc' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='2648b7d08fe74d0486ec82b3b539d15f3dd63bb34d79e7e57bebc3e5d06b5a38' ;; 		i386) goRelArch='linux-386'; goRelSha256='83d732a3961006e058f44c9672fde93dbea3d1c3d69e8807d135eeaf21fb80c8' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='33f7bed5ee9d4a0343dc90a5aa4ec7a1db755d0749b624618c15178fd8df4420' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='493b4449e68d0deba559e3f23f611310467e4c70d30b3605ff06852f14477457' ;; 		*) goRelArch='src'; goRelSha256='78cda84d4217ae0fdb8f87848474be28644bdc1aa16579055f852999a4793ac0'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 11 Jun 2020 22:55:21 GMT
ENV GOPATH=/go
# Thu, 11 Jun 2020 22:55:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2020 22:55:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 11 Jun 2020 22:55:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76dae9e9a8f2b69403c29a068363410a0b491d889452a410e1a846db24918418`  
		Last Modified: Tue, 09 Jun 2020 01:46:14 GMT  
		Size: 49.0 MB (48965925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea4ddfd9cac861440dd774171c0df5d003bcf031cc856603f0dcc1a569a7614`  
		Last Modified: Tue, 09 Jun 2020 02:18:01 GMT  
		Size: 7.4 MB (7385198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4340e9fce6caba0ffebdee007c25f4ed849de61e56dcee1ed7e081edbcf1e5`  
		Last Modified: Tue, 09 Jun 2020 02:18:06 GMT  
		Size: 9.9 MB (9882055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89446217dee5ed85681993c919acbdf28494151380677fdefa88b6b5e481573c`  
		Last Modified: Tue, 09 Jun 2020 02:18:19 GMT  
		Size: 51.4 MB (51366573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d6d711085f1e16cb55dd6d39b0fa3cfe5a898d10c02f3fbb3a0c22180f588c`  
		Last Modified: Tue, 09 Jun 2020 12:02:26 GMT  
		Size: 56.7 MB (56714696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9cc6d921b68bdf61fecdfdc8c210b6335fff14f5ee6ef71f0fc9184682d48d`  
		Last Modified: Thu, 11 Jun 2020 22:58:26 GMT  
		Size: 104.5 MB (104463449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2887361c17d23bd7167e07dd3f80082dd58f804f37949ebdf3f040534bafc1c1`  
		Last Modified: Thu, 11 Jun 2020 22:58:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
