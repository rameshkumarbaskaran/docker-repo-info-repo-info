## `julia:1-bullseye`

```console
$ docker pull julia@sha256:ec9bd14999e923a334969781efd1bf6ab019ba9eff74832de66efc9caed61d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a7e6663e06e77310a96f9dd8a27fe690c9871b2d40b5ec89e3a2b1e0f73c0c06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166310398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320b83a392c3dfd4b5496ad78b14b77e70d6788abc48d32b96ab166cfbc25960`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:30:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 21 Dec 2021 02:30:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:30:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 21 Dec 2021 02:30:54 GMT
ENV JULIA_VERSION=1.7.0
# Tue, 21 Dec 2021 02:31:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 21 Dec 2021 02:31:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a58d5e20d588d9a869aa25ce8aba77d1a7796193dc38a36b69b55074b24e87c`  
		Last Modified: Tue, 21 Dec 2021 02:33:57 GMT  
		Size: 2.4 MB (2425460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7618c2541ccc0fd14e51a83d4ec88c1935c9b9acebf833e4efdc3b88d047774`  
		Last Modified: Tue, 21 Dec 2021 02:34:19 GMT  
		Size: 132.5 MB (132527314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:de18595623cbcec7a6ad96ba8afd08e06191dbd50dec1fe7d0d9e9d9545c5e66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157910600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735a3e2b48573b5b82762f3ccb336b2147159b7762e0f02ab2a7c1fa7bddc698`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 16:38:03 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 16:38:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 16:38:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f6f04f105d9f85c46214e930256815cb332021975a1709a52fcf43a1c0c1da`  
		Last Modified: Fri, 03 Dec 2021 16:40:32 GMT  
		Size: 125.6 MB (125645335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:c42fee23ce0d8989b1fae05221cb13f302a534f69d8694d7dfb10b391edec22e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163547956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f337267b9eda98feb111c7eb2db3c792a22c0bd54728cd0945164de5c82df9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 07:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 07:44:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 21 Dec 2021 07:44:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 07:44:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 21 Dec 2021 07:44:12 GMT
ENV JULIA_VERSION=1.7.0
# Tue, 21 Dec 2021 07:44:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 21 Dec 2021 07:44:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fcb5545b246aed9c9865e6d387c4698008abdd695e268ab79f090186bc2f34`  
		Last Modified: Tue, 21 Dec 2021 07:48:03 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512240f3e9e0915eb11395d1bd6764c39e5702610619a48fa2cfb12b7332044b`  
		Last Modified: Tue, 21 Dec 2021 07:48:39 GMT  
		Size: 128.6 MB (128647610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
