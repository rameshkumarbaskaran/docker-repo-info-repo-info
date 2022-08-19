## `julia:1-buster`

```console
$ docker pull julia@sha256:bad8213a39ef668a52aeefe43c3df110ada607febe1a79f8098dcf0c29a75584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:0e5f95af03902d13b15ce512c0c7634396fbc0eb2e236a220da26bb2c30ebb78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179295713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab3485bd21a5316fd823a32e687db27e5234b1b3a1777ff03c0903e8465d8c5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:38:44 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 04:38:44 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:38:44 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 19 Aug 2022 00:29:02 GMT
ENV JULIA_VERSION=1.8.0
# Fri, 19 Aug 2022 00:29:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-linux-x86_64.tar.gz'; 			sha256='e80d732ccb7f79e000d798cb8b656dc3641ab59516d6e4e52e16765017892a00'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-linux-aarch64.tar.gz'; 			sha256='e003cfb8680af1a65c3be55b53a48cc5186300adaaba8926209800b4d1f4ca7a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-linux-i686.tar.gz'; 			sha256='68866069969aec0c249fedc23eecceaa818a83cc92650d3561d4d47d8a586301'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 19 Aug 2022 00:29:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8199b03a9d2e34dc5c935e04e2b8c29c83f49b58d2b73b8ff7d08f0da2275c7b`  
		Last Modified: Tue, 02 Aug 2022 04:41:59 GMT  
		Size: 4.5 MB (4468198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb83bb8e7f122e7ac22457b9c87db8f233c192043b21fc093744882b73e8dccb`  
		Last Modified: Fri, 19 Aug 2022 00:31:50 GMT  
		Size: 147.7 MB (147687432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d7a4cf23145cb78c00cf48309c7117a955725e6e6329fca9fa977d415bc1b142
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155537800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339a42285c14a2ed5f336b270aa547642b4142e528994b1d1b0ba452ca77319f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:49:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:49:40 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 03:49:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 03:49:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Aug 2022 03:50:31 GMT
ENV JULIA_VERSION=1.7.3
# Tue, 02 Aug 2022 03:50:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.3-linux-x86_64.tar.gz'; 			sha256='9b2f4fa12d92b4dcc5d11dc66fb118c47681a76d3df8da064cc97573f2f5c739'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.7/julia-1.7.3-linux-armv7l.tar.gz'; 			sha256='e9de15c56b9b62727c69d10da4b8e90fa6609d2e94e9cfb9f99128dfb59a8677'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.3-linux-aarch64.tar.gz'; 			sha256='d9e8b342c80ad1371520ed6d11f55b78aa60746737fbf57ecafd6a23b52dd71d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.3-linux-i686.tar.gz'; 			sha256='c1e1a4f9a53affee269c7e740cb8bd46740f9021414459c3ab3bb2c540d9d499'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 02 Aug 2022 03:50:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a9d4e1f7e99b17668fb01c387a1578e85d8241bed9785743ee1bf2fcc0c777`  
		Last Modified: Tue, 02 Aug 2022 03:53:00 GMT  
		Size: 4.3 MB (4346885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa0f596a551894696b641999c405fbf836df3903e8ea6c9c584afaed32fce7c`  
		Last Modified: Tue, 02 Aug 2022 03:54:37 GMT  
		Size: 125.3 MB (125276552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:1bc28b92bfd9454001f83150c48613f24b85a8fe3597efa1c2abd8a76c6710e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176960642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6816e9d552e76dc7b45b7ee7647a05586aacf9e87423f21cfffad5b6e3419ee`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:47 GMT
ADD file:e8057ee44359188db14ad06a6f8e9cab7a301b479e0f7e0e61810abb0ecf48dd in / 
# Tue, 02 Aug 2022 00:39:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:53:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:53:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 15:53:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 15:53:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 19 Aug 2022 00:39:06 GMT
ENV JULIA_VERSION=1.8.0
# Fri, 19 Aug 2022 00:39:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-linux-x86_64.tar.gz'; 			sha256='e80d732ccb7f79e000d798cb8b656dc3641ab59516d6e4e52e16765017892a00'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-linux-aarch64.tar.gz'; 			sha256='e003cfb8680af1a65c3be55b53a48cc5186300adaaba8926209800b4d1f4ca7a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-linux-i686.tar.gz'; 			sha256='68866069969aec0c249fedc23eecceaa818a83cc92650d3561d4d47d8a586301'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 19 Aug 2022 00:39:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0481fdd8148a195a336acc1d5b3d6b0f7fe46395e01c9b674e3ff6974b6ac5a7`  
		Last Modified: Tue, 02 Aug 2022 00:46:14 GMT  
		Size: 27.8 MB (27799555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96087b500a32fa726187f32bd1dabd1c652b1c065185c8e6db82196db8ee9f4`  
		Last Modified: Tue, 02 Aug 2022 15:56:45 GMT  
		Size: 4.6 MB (4616221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50669d9209e325e6c59a19f9b1009bb6a89e93e11949283d1c1231d3dd76a711`  
		Last Modified: Fri, 19 Aug 2022 00:41:19 GMT  
		Size: 144.5 MB (144544866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
