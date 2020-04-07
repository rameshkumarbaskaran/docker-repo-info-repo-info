## `julia:1-buster`

```console
$ docker pull julia@sha256:85eafa2ead425cdbc9142fe6c40ac518e90c26cb43dd58376b707927e0c7f77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:98b9f4174aee469d83a3d6c8c46d0fd9c1a6ef95f7fcf0a3e8e1b20aa01d4988
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138323266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18183d0f0d8119399633e1baabfd1092b030b9b48d98290b15676c3cfa06b283`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:09:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:09:45 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 31 Mar 2020 03:09:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 03:09:45 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 31 Mar 2020 03:09:46 GMT
ENV JULIA_VERSION=1.4.0
# Mon, 06 Apr 2020 23:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='30d126dc3598f3cd0942de21cc38493658037ccc40eb0882b3b4c418770ca751' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='6f7f9407485c8f1380e34a751305eb70a1da9d05af8f882ffaed4e1a09effd56' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='576481accadd441655edf963b81c28cbeaa327b423ec58a77eab103cf830a65a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='41ed8cce4cb8a66dd84095f713bc50d85342e6794fb5f35ac6dafba3276d119d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 06 Apr 2020 23:20:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72b71d3134af3728e710f1dd85497919cd05a5f63d8732281a8f599f71252e6`  
		Last Modified: Tue, 31 Mar 2020 03:11:39 GMT  
		Size: 4.4 MB (4436584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364e671b6375d1b6ec0a9a1d40cdab37905fa8dfaa094127586381c6f867ae36`  
		Last Modified: Mon, 06 Apr 2020 23:20:50 GMT  
		Size: 106.8 MB (106794820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:f115556c990dad0bfc42b9fe6efcf2377dbac7dd88c7c0f4aa02ecd0b722bb07
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123498112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a60dd245e263b81581706493a2f2a9ce7bf04fa90707b5e434109b5aa5df4f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:10:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:10:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 31 Mar 2020 04:10:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 04:10:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 06 Apr 2020 23:58:04 GMT
ENV JULIA_VERSION=1.4.0
# Mon, 06 Apr 2020 23:58:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='30d126dc3598f3cd0942de21cc38493658037ccc40eb0882b3b4c418770ca751' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='6f7f9407485c8f1380e34a751305eb70a1da9d05af8f882ffaed4e1a09effd56' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='576481accadd441655edf963b81c28cbeaa327b423ec58a77eab103cf830a65a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='41ed8cce4cb8a66dd84095f713bc50d85342e6794fb5f35ac6dafba3276d119d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 06 Apr 2020 23:58:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58090fd97742d3492c6c9f9ae45598cdf22e20d11f3c386348831ed9ef75e431`  
		Last Modified: Tue, 31 Mar 2020 04:12:36 GMT  
		Size: 3.8 MB (3783651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94939648b9b33a255e424e4027fbf90c98ecc2d9836c38fe7a179ae4e48f76a6`  
		Last Modified: Mon, 06 Apr 2020 23:59:33 GMT  
		Size: 97.0 MB (97014730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a10a693db14af0d554aa7b98379fc4b4c8717d239186ea58c5f36f999e038229
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119875470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102fa2b9dd57d9ddb7762e531e4757d83f221990dee3606caa028c6839c2908f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:33 GMT
ADD file:47ab456123ae97a527249191ff2bc0014e7ef0ae186aec91bf6a63eb077ecb91 in / 
# Tue, 31 Mar 2020 02:05:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 05:01:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 05:01:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 31 Mar 2020 05:01:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 05:01:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 31 Mar 2020 05:01:25 GMT
ENV JULIA_VERSION=1.4.0
# Tue, 07 Apr 2020 00:44:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='30d126dc3598f3cd0942de21cc38493658037ccc40eb0882b3b4c418770ca751' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='6f7f9407485c8f1380e34a751305eb70a1da9d05af8f882ffaed4e1a09effd56' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='576481accadd441655edf963b81c28cbeaa327b423ec58a77eab103cf830a65a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='41ed8cce4cb8a66dd84095f713bc50d85342e6794fb5f35ac6dafba3276d119d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 07 Apr 2020 00:44:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a6c32b8bc1ce2b374630673ded1d5ef5a98936d045bf0632fcf599dc2229d493`  
		Last Modified: Tue, 31 Mar 2020 02:12:15 GMT  
		Size: 25.9 MB (25851645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2839d96f3fc4180c714a825b5c1a24f2f93217a76c3714bd55165a88e05d91`  
		Last Modified: Tue, 31 Mar 2020 05:04:00 GMT  
		Size: 4.3 MB (4315510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e431814eaafc5d057cf00cdcafa51c860fb428bf78ff92489102a2e0f9712c8`  
		Last Modified: Tue, 07 Apr 2020 00:45:18 GMT  
		Size: 89.7 MB (89708315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:fb09607a2c0f0ff09e2ca51ffe314721d2708313b20bb41d05edbbad1b0285ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135745740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d0a3d12891fdd339b3bb182b7db7ecfc83e0979dc3ad4f6a914ae74a3f96f6`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:42 GMT
ADD file:a453117866661af4ddfa21203d65ce6661efeaeca2a1704e09747c83b4c58e47 in / 
# Tue, 31 Mar 2020 00:39:42 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:05:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 31 Mar 2020 01:05:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 01:05:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 31 Mar 2020 01:05:27 GMT
ENV JULIA_VERSION=1.4.0
# Mon, 06 Apr 2020 23:38:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='30d126dc3598f3cd0942de21cc38493658037ccc40eb0882b3b4c418770ca751' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='6f7f9407485c8f1380e34a751305eb70a1da9d05af8f882ffaed4e1a09effd56' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='576481accadd441655edf963b81c28cbeaa327b423ec58a77eab103cf830a65a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='41ed8cce4cb8a66dd84095f713bc50d85342e6794fb5f35ac6dafba3276d119d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 06 Apr 2020 23:38:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2314106a15e49c7908bebb2c697dcaf3d6a1626b70fe72bc0c0cb71eb216ddc3`  
		Last Modified: Tue, 31 Mar 2020 00:45:31 GMT  
		Size: 27.7 MB (27747648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583fde8d7ec1bbaa2b4b31dceffabe4dc5a10339fbd48d0479f927f186ef0689`  
		Last Modified: Tue, 31 Mar 2020 01:06:55 GMT  
		Size: 4.6 MB (4586375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f23a5e87a61c1beb0e0fbcbd325e86d325f9d2737b674c120dd486c8699396`  
		Last Modified: Mon, 06 Apr 2020 23:39:33 GMT  
		Size: 103.4 MB (103411717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
