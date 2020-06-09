## `julia:rc-buster`

```console
$ docker pull julia@sha256:46248a18eaaca9b338cb771788352654a272e11f7943ce3fca12b5825ae45619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:d628cd14d721e5da8833471a3be4af381bd37d3529c388bff549acd613f850a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143156349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a825074512bde85b1c95283a8b082691ecb164532847ce3e32b1b38369ad02bf`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 19:26:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 19:26:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 15 May 2020 19:26:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 19:26:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 29 May 2020 00:19:51 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:20:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 29 May 2020 00:20:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31412bedd277e03e6e1952856d07766cf16c2c9a327ce637160a2cdf5eca3793`  
		Last Modified: Fri, 15 May 2020 19:28:24 GMT  
		Size: 4.4 MB (4436593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8f5f384a47cc190d4b6c94a512f7e9bd5bb7d3d8f953030e25c05eb77d24d`  
		Last Modified: Fri, 29 May 2020 00:20:55 GMT  
		Size: 111.6 MB (111621000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; 386

```console
$ docker pull julia@sha256:88b98fa03de5e35693bb37e3fbf641c492a6fa0fd1885530afa0fabc2b99914e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ad81fb14b2fa66800c15e83565b7365e1cbabb6418b12ba12f311506538432`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 18:07:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 15 May 2020 18:07:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 18:07:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 29 May 2020 00:38:41 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:39:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 29 May 2020 00:39:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06815c0e7ea17fa3aef53a4fa131a0dd6f4b6264a2de1ce61cc6b90afe99c466`  
		Last Modified: Fri, 15 May 2020 18:09:04 GMT  
		Size: 4.6 MB (4586399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa0ffe7afdc0c60f49f7998891993aebf444081e886cda69e16be23cedb1196`  
		Last Modified: Fri, 29 May 2020 00:40:16 GMT  
		Size: 108.6 MB (108622508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
