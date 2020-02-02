## `golang:1-stretch`

```console
$ docker pull golang@sha256:d91310cde36a02cae412c665c9fe08d6d32bb7a689a0aaf4ad8de1978d13cca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:496453fbfd56353a5caae2802b3798c2072a878402a7567fd940efa9793de51a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288351223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9cd172931892a72b89f94292bfdaeec82d81d375ca32ad14ebf4e32dc83520`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:59:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 06:32:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 21:20:03 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:20:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:20:14 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:20:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:20:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:20:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705a4c4fd310b96bfb3d7928428e65f0d3f5bad0cd0bda1434aee1d89418468`  
		Last Modified: Sat, 28 Dec 2019 05:04:45 GMT  
		Size: 50.1 MB (50072671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb9fad7ab3b1a2714a918921e2c498412dd4cf54c713e4f2ca52d63e1e431ee`  
		Last Modified: Sun, 29 Dec 2019 06:34:57 GMT  
		Size: 57.7 MB (57690913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8c48981da7d0676b702fc61aa0b38a744ee9d10deb1a7410f9c5418fff8f3`  
		Last Modified: Tue, 28 Jan 2020 21:31:48 GMT  
		Size: 120.1 MB (120069435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce3857600ceaf5b6cb46df069fa3ccd3914615719d21933c88a3abc2056e4f5`  
		Last Modified: Tue, 28 Jan 2020 21:31:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:0c79979292266aa65c67630559c427eba7b76581f89165f4369776c36fa54166
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246230833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d3ce8dca44ec3d5ad76fc245e79909fd3c299e73a1b46fcc945ea21b580747`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:03:19 GMT
ADD file:5692a55e4805d33baa21e559cc0bb86fb91422171345ddd332fa5514285a3401 in / 
# Sat, 28 Dec 2019 05:03:25 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:59:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:00:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:00:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 03:43:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 21:58:38 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:58:56 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:59:01 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:59:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:59:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:59:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b531ae4a39253d883a11291e842b7e1aa9dae38f9d9b77ddea55b2625ce986e3`  
		Last Modified: Sat, 28 Dec 2019 05:10:53 GMT  
		Size: 42.1 MB (42108124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22754f6fc5d5a244119c0928ebf7d851d276d7f095f07e6bf435fa7afbcab8a8`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 9.5 MB (9498197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2155e4b3456accbea4b6873247312dd288feb477ec966ed48637e031aba558`  
		Last Modified: Sat, 28 Dec 2019 07:11:03 GMT  
		Size: 3.9 MB (3918728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad0ae2287846b9d91f237a798b6ae550ff58e33efb804be1ca049f9fd7a480f`  
		Last Modified: Sat, 28 Dec 2019 07:11:24 GMT  
		Size: 46.4 MB (46399839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2023c29cd927acbf16637195e35e121b4b6e49b7cdf9de5cc4ae894ad9d9bd`  
		Last Modified: Sun, 29 Dec 2019 03:47:55 GMT  
		Size: 46.0 MB (46027023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c45b9814a9d74edcfaced51abeb2a1d07ae67902a4a43aadbf5a4d6184186b`  
		Last Modified: Tue, 28 Jan 2020 22:12:46 GMT  
		Size: 98.3 MB (98278766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491b332cdae80292b2a71e5af2f8e28432f9e53b190c05e1ed8228ee0591e12a`  
		Last Modified: Tue, 28 Jan 2020 22:12:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:031f5dbf4b2e91f2fac81278bfe75aeb16fee2abd5214c4773b05041caff2d63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251734413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d677626d25414f9d91cad3c6739544591ee506d5fa722d453787c7919395dcd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:30:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:10:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:10:29 GMT
ENV GOLANG_VERSION=1.13.7
# Sun, 02 Feb 2020 11:10:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sun, 02 Feb 2020 11:10:46 GMT
ENV GOPATH=/go
# Sun, 02 Feb 2020 11:10:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 11:10:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sun, 02 Feb 2020 11:10:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a82fc9ca296b095585ba7f3f6d83566428dbefcbfd284e242039aba97840b2`  
		Last Modified: Sat, 01 Feb 2020 17:39:40 GMT  
		Size: 48.0 MB (48024205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1cf3b66f921e6f0d5e42cf6821f9a4af6cf2bba19118c0275e0c78b66d0a5`  
		Last Modified: Sun, 02 Feb 2020 11:14:56 GMT  
		Size: 49.1 MB (49097963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eddfb2211d9c2324ee06dbab0f35e7a97f6c1a347224286754449b22349492`  
		Last Modified: Sun, 02 Feb 2020 11:15:10 GMT  
		Size: 97.6 MB (97602432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301a3160d8239b229a24381fc03497adac1f0d46c62303e1e006b7136e8e5ae`  
		Last Modified: Sun, 02 Feb 2020 11:14:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:d16d1e0b4021e15dfc17dc58e794ad1e794155abf74c579a4c7b8a2c83ff8682
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276613453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b188347a08abeb444b2cf92efeaf2be62f227e6941812ff347f87d8dc7807a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:53 GMT
ADD file:bae1646c4e3069e717d1ee4f6c312c249e96a21d795a639cdfaf338d645c8be9 in / 
# Sat, 01 Feb 2020 16:41:53 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:38:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:39:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:43:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 10:43:42 GMT
ENV GOLANG_VERSION=1.13.7
# Sun, 02 Feb 2020 10:43:55 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sun, 02 Feb 2020 10:43:55 GMT
ENV GOPATH=/go
# Sun, 02 Feb 2020 10:43:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 10:43:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sun, 02 Feb 2020 10:43:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:97067fdacc0601fe58a5f782cd09d3c58a214c43b8629a2d92bd7025f46fd265`  
		Last Modified: Sat, 01 Feb 2020 16:47:15 GMT  
		Size: 46.1 MB (46100017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1ac2ac579e53fc74848ab743b53ae2f6e54350989c71359d435c2fef2e5157`  
		Last Modified: Sat, 01 Feb 2020 17:45:45 GMT  
		Size: 10.8 MB (10817587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7b32e68627ad71130644b1646afb1aa0bcf1f440df145526a73fdbd413f3b`  
		Last Modified: Sat, 01 Feb 2020 17:45:43 GMT  
		Size: 4.6 MB (4561467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b926c1ce2d1cf6b99c32683bf0fd0233d4f71f367d38a16de2ba08e9ecbf1cc2`  
		Last Modified: Sat, 01 Feb 2020 17:46:05 GMT  
		Size: 51.6 MB (51595566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183d866e03dcc73d6e128eea16869947ddf4bc3bde45ed98ea05f62bebf7bf77`  
		Last Modified: Sun, 02 Feb 2020 10:47:05 GMT  
		Size: 62.2 MB (62218836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d081bef46ed4c534eb7c740bc9a8fe34d0530f69ad36c84310689b25bef533`  
		Last Modified: Sun, 02 Feb 2020 10:47:12 GMT  
		Size: 101.3 MB (101319854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bc78c983e50e07d694a75f13254c8f8610527ce1c2ef40edc3783fba5be601`  
		Last Modified: Sun, 02 Feb 2020 10:46:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; ppc64le

```console
$ docker pull golang@sha256:c6e4f255e2a428fb249dec98e41810c8e0db4ef02f06a9b52b03b318e591785c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259334747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c481b25b1e8a1032de4a42cf6b7296e2dd44bb0b607e02407805bc467de802e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:59 GMT
ADD file:0da9c5c67cad579be1a33f0f66df515de7f3ad992050c39cbaac281a01be41b3 in / 
# Sat, 28 Dec 2019 04:23:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:12:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:12:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 00:37:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 21:17:42 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:18:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:18:05 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:18:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:18:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:18:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:32185d9fc6268c6a6d87060ea324482fa22129c0f06d0f35e1376ca27b5399a0`  
		Last Modified: Sat, 28 Dec 2019 04:32:44 GMT  
		Size: 45.7 MB (45652475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff48b558393a869138bac45b7d540a1536280a8a4a86a3d0ff0dcab238a6418`  
		Last Modified: Sat, 28 Dec 2019 07:25:43 GMT  
		Size: 10.0 MB (10002000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e334b7fa51f55c0f060923f801160877cc313f1e3e40cf76efd21d94691cd565`  
		Last Modified: Sat, 28 Dec 2019 07:25:41 GMT  
		Size: 4.3 MB (4296599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66ad4e8e64de1e6f91344e81581ac6cbc65550f1561a83333f8367c7c8cee56`  
		Last Modified: Sat, 28 Dec 2019 07:26:11 GMT  
		Size: 50.1 MB (50085193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a62a2535d8434f3781601dd52417f210e59a28a66cd173d86023f73c19130f4`  
		Last Modified: Sun, 29 Dec 2019 00:41:55 GMT  
		Size: 52.9 MB (52867838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27652c8bdcad20c393ceaa4469838c63f75f3823044d1b12650186b7b9880028`  
		Last Modified: Tue, 28 Jan 2020 21:30:58 GMT  
		Size: 96.4 MB (96430486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1300dd19e75122becad668c32cec330b7fee15eded9a63c54be0d1bf99038f7`  
		Last Modified: Tue, 28 Jan 2020 21:30:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; s390x

```console
$ docker pull golang@sha256:b0fd145e7fd215b90af65b6c623176c078d2145b393e59ccf09c29bc57789d73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258583629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d476fec283ca004bcc8de81d46648d2ae8a8ed4fff98a1536e7d91973c302d2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:43 GMT
ADD file:17af4834ca99365d5ecf14eb938572689bd3c3ad5fd8a88da12c4c3474975771 in / 
# Sat, 01 Feb 2020 16:43:45 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:00:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:00:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 23:02:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 23:02:30 GMT
ENV GOLANG_VERSION=1.13.7
# Sat, 01 Feb 2020 23:02:40 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='b3dd4bd781a0271b33168e627f7f43886b4c5d1c794a4015abf34e99c6526ca3' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='ff8b870222d82c38a0108810706811dcbd1fcdbddc877789184a0f903cbdf11a' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='8717de6c662ada01b7bf318f5025c046b57f8c10cd39a88268bdc171cc7e4eab' ;; 		i386) goRelArch='linux-386'; goRelSha256='93e82683f32d9fe7fda9b686415aeee599a92c4e450b69519bb53e1d62144a85' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8fe0aeb41e87fd901845c9598f17f1aae90dca25d2d2744e9664c173fbf7f784' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='7d405e515029d19131bae2820310681c31b665178998335ecc4494e8de01dfeb' ;; 		*) goRelArch='src'; goRelSha256='e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 01 Feb 2020 23:02:45 GMT
ENV GOPATH=/go
# Sat, 01 Feb 2020 23:02:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 Feb 2020 23:02:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 01 Feb 2020 23:02:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb54e9d54b34d992a5c6582a6fe3836692cce3589a408748090bbb916a4cc63d`  
		Last Modified: Sat, 01 Feb 2020 16:47:28 GMT  
		Size: 45.2 MB (45241584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d13d85604945e95d31c38d488a822d8e0b84e7548a10db0c89115cca1887aa`  
		Last Modified: Sat, 01 Feb 2020 18:06:29 GMT  
		Size: 10.3 MB (10325358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b324848b1286794120fbcb3c696328dd955db597ec3e70840b5dc97d794db`  
		Last Modified: Sat, 01 Feb 2020 18:06:33 GMT  
		Size: 4.4 MB (4372596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38645e5b0e6402c091627176f5aed8b9d434ccf323ecc4ca2c66f934acc1a11a`  
		Last Modified: Sat, 01 Feb 2020 18:06:45 GMT  
		Size: 50.5 MB (50499891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555ca4faedcdf5a518aaa854f9752587efa9ed96a7b02a0c1b875b6e09086a90`  
		Last Modified: Sat, 01 Feb 2020 23:05:01 GMT  
		Size: 46.0 MB (45982845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f8268b1ad43b8b3f90827a473fbfbe6ef73cb5bd443b0608fab084eb662656`  
		Last Modified: Sat, 01 Feb 2020 23:05:24 GMT  
		Size: 102.2 MB (102161199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd96b6bf4019d99cb26c7d954360c489783e6990ca47d5be0b571f2668a722b`  
		Last Modified: Sat, 01 Feb 2020 23:05:21 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
