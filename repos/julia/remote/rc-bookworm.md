## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:f4aeddf36f8fd4ca2e997cff48c4f547399db98ca5205dd5f7349f0d27998f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:98441976b343ed0fbb2b0224054720b7bbb12326cb0426045b9848875387d988
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208909773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089dbf4493532d493178a3d93202a1091a3dbc6a870b49032c1774f0cf9f5acf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:56:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:56:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 28 Jul 2023 01:56:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 01:56:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 28 Jul 2023 01:56:36 GMT
ENV JULIA_VERSION=1.10.0-alpha1
# Fri, 28 Jul 2023 01:56:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-alpha1-linux-x86_64.tar.gz'; 			sha256='9aea120b126e54bf87a5bfcddc1c58d282272f6c7e3534f29e210a3c80290cfd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-alpha1-linux-aarch64.tar.gz'; 			sha256='f56b5fb976621fbc5cdd98fb26c5bcfd94d21997ed0b36f9306b94e62f5e41fa'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-alpha1-linux-i686.tar.gz'; 			sha256='a37e4d5cae9ee39c30dddb3f5beb595c1e93de96867d88d5e1d017b91dfe924f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='6c9ff07b56b847af530e7d2274956e0105765e03cfad4af3d3a7a8a00e17d2e1'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 28 Jul 2023 01:57:00 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:57:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:57:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f396ccff59167002913d510490ff01699857b722ce2c9f5d8f8fcfabf81dae47`  
		Last Modified: Fri, 28 Jul 2023 01:59:49 GMT  
		Size: 5.7 MB (5695805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7fc7252500ce029c10ce4ec8f13b781a52717bcdbccbbd278eb19d9f624bf`  
		Last Modified: Fri, 28 Jul 2023 02:00:13 GMT  
		Size: 174.1 MB (174089063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68119a76085b84d7ab237267093966d2f15545ecc640d3bc94fc44523c2fa7ac`  
		Last Modified: Fri, 28 Jul 2023 01:59:48 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3999c77e0f3a1f4769e163d2bf4e7057840bb5f4d5a6d528d91da8e758f45d6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203343328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b264368dd4c9ad5fa4c97878e5e6563a7f17b4b7389ac80960fb6a1fb5e81d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:35 GMT
ADD file:71fd66666294148382f2e6a09ae5e277d4c4e9c74402ab64b693a79387b67a09 in / 
# Tue, 04 Jul 2023 01:57:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:52:52 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jul 2023 03:52:52 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 03:52:52 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Jul 2023 22:44:50 GMT
ENV JULIA_VERSION=1.10.0-alpha1
# Tue, 11 Jul 2023 22:45:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-alpha1-linux-x86_64.tar.gz'; 			sha256='9aea120b126e54bf87a5bfcddc1c58d282272f6c7e3534f29e210a3c80290cfd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-alpha1-linux-aarch64.tar.gz'; 			sha256='f56b5fb976621fbc5cdd98fb26c5bcfd94d21997ed0b36f9306b94e62f5e41fa'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-alpha1-linux-i686.tar.gz'; 			sha256='a37e4d5cae9ee39c30dddb3f5beb595c1e93de96867d88d5e1d017b91dfe924f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='6c9ff07b56b847af530e7d2274956e0105765e03cfad4af3d3a7a8a00e17d2e1'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 11 Jul 2023 22:45:15 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 11 Jul 2023 22:45:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 22:45:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3ae0c06b4d3aa97d7e0829233dd36cea1666b87074e55fea6bd1ecae066693c7`  
		Last Modified: Tue, 04 Jul 2023 02:01:20 GMT  
		Size: 29.2 MB (29152458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fe3ef433e4417135885378c889772d9214a97384ecddb087c5cd2aec31fc9`  
		Last Modified: Tue, 04 Jul 2023 03:54:38 GMT  
		Size: 5.5 MB (5526511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4345876a92abcbe915cdbfe7fabba15880cd427a5a4bbd340482c475dc8bf9`  
		Last Modified: Tue, 11 Jul 2023 22:46:29 GMT  
		Size: 168.7 MB (168663986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4418b1fb92bee6d3cca4454674e10ce0475e050e3405f2b3b383a6381522698c`  
		Last Modified: Tue, 11 Jul 2023 22:46:09 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:61a5da612251b38ac656e91c3d1280018873e7893e071cb19f1dd4f8b0857e6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196231694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8351cb038034d9498d1bbc63beb34f8839d9e8b30ee70cc2fbad0447db07234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:56 GMT
ADD file:3d6e6f3e900e480a7e060fcaf57313c0f954bf906967a7fa0317567c387cf5aa in / 
# Thu, 27 Jul 2023 23:38:57 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:04:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:04:52 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 28 Jul 2023 00:04:52 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 00:04:52 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 28 Jul 2023 00:04:52 GMT
ENV JULIA_VERSION=1.10.0-alpha1
# Fri, 28 Jul 2023 00:05:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-alpha1-linux-x86_64.tar.gz'; 			sha256='9aea120b126e54bf87a5bfcddc1c58d282272f6c7e3534f29e210a3c80290cfd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-alpha1-linux-aarch64.tar.gz'; 			sha256='f56b5fb976621fbc5cdd98fb26c5bcfd94d21997ed0b36f9306b94e62f5e41fa'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-alpha1-linux-i686.tar.gz'; 			sha256='a37e4d5cae9ee39c30dddb3f5beb595c1e93de96867d88d5e1d017b91dfe924f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='6c9ff07b56b847af530e7d2274956e0105765e03cfad4af3d3a7a8a00e17d2e1'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 28 Jul 2023 00:05:28 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 28 Jul 2023 00:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 00:05:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3a8b0c4b1a83609d978d576be6174f951ff27084d7c9aef91892b60b223a5104`  
		Last Modified: Thu, 27 Jul 2023 23:43:26 GMT  
		Size: 30.1 MB (30141788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017b4dcfaea553337f724c97907de2678e47ea038b04e4dc006657aa31212b37`  
		Last Modified: Fri, 28 Jul 2023 00:08:26 GMT  
		Size: 5.9 MB (5854644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c1e08357c79aa3392b9ea9b2410947d4bf734a1c05acb9f3a5fb7c0627ce13`  
		Last Modified: Fri, 28 Jul 2023 00:08:57 GMT  
		Size: 160.2 MB (160234884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a03a8eb81ec0979424c9eb2cb39694a68c3475cf28f4371fe29410e7ad0c187`  
		Last Modified: Fri, 28 Jul 2023 00:08:24 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:c033a00523c1b65c919a338855307e6513aa59ffcd70014b51348ac20d81523a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197890608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641bec901192868c323b0c3cc8e4073f8604261f00192e9237cff6446846df20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jul 2023 01:17:51 GMT
ADD file:51887002f5002ccc662adbc6ecf1129e3db375a7a77b93da43cc9a8326b3c4b9 in / 
# Tue, 04 Jul 2023 01:17:53 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:40:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:40:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jul 2023 06:40:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:40:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Jul 2023 22:19:46 GMT
ENV JULIA_VERSION=1.10.0-alpha1
# Tue, 11 Jul 2023 22:20:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-alpha1-linux-x86_64.tar.gz'; 			sha256='9aea120b126e54bf87a5bfcddc1c58d282272f6c7e3534f29e210a3c80290cfd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-alpha1-linux-aarch64.tar.gz'; 			sha256='f56b5fb976621fbc5cdd98fb26c5bcfd94d21997ed0b36f9306b94e62f5e41fa'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-alpha1-linux-i686.tar.gz'; 			sha256='a37e4d5cae9ee39c30dddb3f5beb595c1e93de96867d88d5e1d017b91dfe924f'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='6c9ff07b56b847af530e7d2274956e0105765e03cfad4af3d3a7a8a00e17d2e1'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 11 Jul 2023 22:20:45 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 11 Jul 2023 22:20:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 22:20:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ba99a1aa5a92d949d988e66df7723a542fd81bc30eef9d4269e8a899820d4bb2`  
		Last Modified: Tue, 04 Jul 2023 01:24:36 GMT  
		Size: 33.1 MB (33116716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e00614d6b132be437f8e5dd49964584196c1794d22317ffbd448602456fd920`  
		Last Modified: Tue, 04 Jul 2023 06:43:46 GMT  
		Size: 6.2 MB (6229887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f71477eaf8db4882ea7235588d2d4a2b11daa594d350a2a852ab69f5959794`  
		Last Modified: Tue, 11 Jul 2023 22:23:24 GMT  
		Size: 158.5 MB (158543633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a62d83e4c5c32050d5f745951f943a19aec8f0668d21601068034366c893f2e`  
		Last Modified: Tue, 11 Jul 2023 22:22:40 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
