## `golang:1-buster`

```console
$ docker pull golang@sha256:358b986cf724cacf3f51d1a926506958fc81eae1b7e3222f6c89703c8bf0e2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-buster` - linux; amd64

```console
$ docker pull golang@sha256:c2ca292f4133651fea54596d2eda459dd70cb2c742f91de5b71960a86a1074c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308571001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5a4a2bb2b26e372592472e43f1659f93217e10cee93841b3d97a50c6ed48c1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:08 GMT
ADD file:d6d0bdf8cb07a7a0dc32e9df50ac80ca1a524c3fa48136892ded195061f2194c in / 
# Sat, 28 Dec 2019 04:21:09 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:47:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 06:31:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 21:19:48 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:19:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:19:58 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:19:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:19:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f0fdd3eaac017684c880d836abdaf02f9db7ac8ecca970356482e3d8e315650`  
		Last Modified: Sat, 28 Dec 2019 04:25:39 GMT  
		Size: 50.4 MB (50379720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918eaefd9de8a1595f56900fdb8ab65a03d64b1da1078da7c0b0bf6f7552a14`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 7.8 MB (7811715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf3e3107f525b7dea5b3cdfd15f62666066202105a0aaddbab2a02aefad1f7`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 10.0 MB (9996202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27622921edb2aae9e0cb64f71a81b4a7cfef8f6a6c766514a018815834ba4e14`  
		Last Modified: Sat, 28 Dec 2019 05:02:00 GMT  
		Size: 51.8 MB (51790562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f862a94ee6511b02e1d1306efbc314a27c16f61532d83609be405db52b1fcae3`  
		Last Modified: Sun, 29 Dec 2019 06:34:07 GMT  
		Size: 68.5 MB (68523251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dad0c93774b07cf2ccfdca529c6a69e1ea32e500056d9f318d3c5f4216ebf2`  
		Last Modified: Tue, 28 Jan 2020 21:31:23 GMT  
		Size: 120.1 MB (120069426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a961e419e5c5c93c895aed3984b74f263303931d05d1960ac99ed09c161af92`  
		Last Modified: Tue, 28 Jan 2020 21:31:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:1023878c5f320b1a0a2402fd558900400e2580f57835d4557a367a1bc0ffeb38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260890536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4582f5cd87e5e616b8ef8451db3ed4116cbc541f6a5522301dcaaf3445b8124b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:58:42 GMT
ADD file:26fba5cd6ba1fe45f19fb80d1c8e54eac5189e2b93e521b2ba6d5a6b54175e81 in / 
# Sat, 28 Dec 2019 04:58:45 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:44:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 03:40:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 21:57:58 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:58:18 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:58:22 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:58:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:58:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:58:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:760e5af4a2ec2472d42b6773d075af9d2a006e0b7725ba9992e530f561d326f8`  
		Last Modified: Sat, 28 Dec 2019 05:07:11 GMT  
		Size: 45.9 MB (45859628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc761fecef183bb949ae59f45d1f618cc3e8879cb25946ab48737d1d8a59b0`  
		Last Modified: Sat, 28 Dec 2019 07:07:06 GMT  
		Size: 7.1 MB (7096250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73181b0fe903be79034378988be75730f983b13ada732a04ea4f46f73b332896`  
		Last Modified: Sat, 28 Dec 2019 07:07:06 GMT  
		Size: 9.3 MB (9343271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870abc97e939a1f3c484e5c9aec16d33497f3603c57bd4581d15915528703890`  
		Last Modified: Sat, 28 Dec 2019 07:07:28 GMT  
		Size: 47.3 MB (47315646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82416eb37ad7180f99cbe886fd16f85d209e1609a083a98bd84b164928e02bfa`  
		Last Modified: Sun, 29 Dec 2019 03:46:37 GMT  
		Size: 53.0 MB (52996883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26317466c1df34505ff6708bcaa46921f2aa6542933c58bbf7090a9331f03b5`  
		Last Modified: Tue, 28 Jan 2020 22:12:02 GMT  
		Size: 98.3 MB (98278702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fb417661f675e46a44b14303b504e506cce01364f33abe8f59c8545901aff6`  
		Last Modified: Tue, 28 Jan 2020 22:11:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9277e5655887609441e706e5a7c28e4382a3b512e2f8c2ec48dbc68ea9af7ac6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278932584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30d74e80031513250dfe99512ef9076be0ab2aa70ef18a55a8bd05e58b507a3`
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
# Sun, 02 Feb 2020 11:09:37 GMT
ENV GOLANG_VERSION=1.13.7
# Sun, 02 Feb 2020 11:09:53 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sun, 02 Feb 2020 11:09:57 GMT
ENV GOPATH=/go
# Sun, 02 Feb 2020 11:09:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 11:10:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sun, 02 Feb 2020 11:10:02 GMT
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
	-	`sha256:e86c8339d2b79bd92f500f5d8ed3b1f20e913cfa7beff7dced36487201c727db`  
		Last Modified: Sun, 02 Feb 2020 11:14:34 GMT  
		Size: 97.6 MB (97602416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1266f4979b0e54136482546c9226b697ee0f47d0b50b822dd009f8ec4fd083b3`  
		Last Modified: Sun, 02 Feb 2020 11:14:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:9d8372ff907fd663419df0ed415b1f25caa21dc36be48aad66c7868fe8c76dd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297554541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f5f3967568714c4b76bfb6c506f970ac81e1a4e2b50fa26568c1f8bfa055e7`
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
# Sun, 02 Feb 2020 10:42:59 GMT
ENV GOLANG_VERSION=1.13.7
# Sun, 02 Feb 2020 10:43:21 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sun, 02 Feb 2020 10:43:21 GMT
ENV GOPATH=/go
# Sun, 02 Feb 2020 10:43:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:43:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sun, 02 Feb 2020 10:43:23 GMT
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
	-	`sha256:3bfd640e377524464b6967fa1fbb65db18317e265e71ade1ef9bf9001372f5ed`  
		Last Modified: Sun, 02 Feb 2020 10:46:37 GMT  
		Size: 101.3 MB (101319803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86c114dd1d59b2daacf8220140f9a7208da650c282264fba595bca7100efb52`  
		Last Modified: Sun, 02 Feb 2020 10:46:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:8ecd0e6772d224ed07f03bf9ac6557840e1606d07ca79dfbe14d7f05d1bf7e7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300361490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec47827a5dfb2d9d0fd922bb71ee6407d0ef5a7c5fd39136d03a40b323d1acd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:12 GMT
ADD file:7c5858835ffb42e32df47084d7f85ba9392c5e37ee636e19dfae15d858c5b6c4 in / 
# Sat, 28 Dec 2019 04:20:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:51:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:51:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 00:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 21:16:56 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:17:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:17:26 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:17:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:17:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:17:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9adf09915c3544b1264f206aec99890c8e5e5c358fc4327886fbdab3c9eecc`  
		Last Modified: Sat, 28 Dec 2019 04:27:21 GMT  
		Size: 54.1 MB (54132515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf9e003a90307c0e87a3bace1df7cc0c72889de0f3060d33cc175cd6bd9f40d`  
		Last Modified: Sat, 28 Dec 2019 07:21:47 GMT  
		Size: 8.3 MB (8252099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24889e07923c5eca1933bb3b0b8bdfc25a42834db78bae343f5fdf88cab3a23e`  
		Last Modified: Sat, 28 Dec 2019 07:21:47 GMT  
		Size: 10.7 MB (10727068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7fe26ecc5fde0ab3859074fdead6e20734403e4cbb2f1867793bbd27fe4290`  
		Last Modified: Sat, 28 Dec 2019 07:22:19 GMT  
		Size: 57.4 MB (57391712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d582f8e15dc3ccf533126f7c83f7d5ea00372fbce59ba2f0189a646d7a657`  
		Last Modified: Sun, 29 Dec 2019 00:40:40 GMT  
		Size: 73.4 MB (73427436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b98bd558186d78e1d90582a8f54e3cf2f399ce1c15d0f18cbe3defd0ab50b1`  
		Last Modified: Tue, 28 Jan 2020 21:30:11 GMT  
		Size: 96.4 MB (96430504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d6639654c17450a53c9bdc1a0fa2a60492002870e98d28db1aae14b03a7c30`  
		Last Modified: Tue, 28 Jan 2020 21:29:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; s390x

```console
$ docker pull golang@sha256:053af876b91913aed3c9ac2dd8b595bad22b94416eea6848860df62f3367af60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276297677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405b58165bf06b178dacbf6c969d559fe180cadb2d6f1c75fe0755bdf368aaa0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:14 GMT
ADD file:642aef2e391d18e3999374d6068f29ccc5ad62b25a0d18c852a6b5534daa18f7 in / 
# Sat, 01 Feb 2020 16:42:17 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:50:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:50:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 23:01:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 23:01:53 GMT
ENV GOLANG_VERSION=1.13.7
# Sat, 01 Feb 2020 23:02:08 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 01 Feb 2020 23:02:13 GMT
ENV GOPATH=/go
# Sat, 01 Feb 2020 23:02:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 23:02:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 01 Feb 2020 23:02:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6f3b736b312bfd59fd7947524542ae1d57ed4564aefaafdf0ccfb7d600f7978f`  
		Last Modified: Sat, 01 Feb 2020 16:45:36 GMT  
		Size: 49.0 MB (48954499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca02855c81b470d73964fc93a8a5e484c5ce5dd6782210cc15b8aca2d28684`  
		Last Modified: Sat, 01 Feb 2020 18:03:52 GMT  
		Size: 7.4 MB (7381759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ecd1a9e0aa67e009dc11b696d0a2029c3bb506e5058e13434114e16ad7a290`  
		Last Modified: Sat, 01 Feb 2020 18:03:53 GMT  
		Size: 9.9 MB (9882030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114b7e56002fcad21b16ab9d3774a372824925547f59e9580bc61ec3cee41394`  
		Last Modified: Sat, 01 Feb 2020 18:04:07 GMT  
		Size: 51.3 MB (51326330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba663ac4e1567abd178cbcb653944b168f5b132c1a687c67ef4041d7ed4030d`  
		Last Modified: Sat, 01 Feb 2020 23:04:12 GMT  
		Size: 56.6 MB (56591695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213fb37638ee3945de166769c41785746ccd8b769094a578788eaebd421c0646`  
		Last Modified: Sat, 01 Feb 2020 23:04:41 GMT  
		Size: 102.2 MB (102161209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b56a0d174e1942aa9c4762ba657088d03af1090840f5776077c9784598b3abe`  
		Last Modified: Sat, 01 Feb 2020 23:04:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
