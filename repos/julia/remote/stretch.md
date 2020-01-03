## `julia:stretch`

```console
$ docker pull julia@sha256:8b8ee3518e988ac6e40048bafbe63f4fa37f1ea6b053ca565ba87eb557dbaf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:stretch` - linux; amd64

```console
$ docker pull julia@sha256:6d722d5a5e5083282d6155cc59f955951559c385070a84cd53ef15b65efe87ca
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133452226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc32377d28a4967899f2033678aade53114f6db9f95f11831184506c4364b6c8`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 13:54:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 28 Dec 2019 13:54:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 13:54:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Jan 2020 01:24:05 GMT
ENV JULIA_VERSION=1.3.1
# Fri, 03 Jan 2020 01:24:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Jan 2020 01:24:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6aef362d0b91076dc5819a1b925f776504ec063851be5395cadb471b9f3881e`  
		Last Modified: Sat, 28 Dec 2019 13:57:02 GMT  
		Size: 7.6 MB (7555513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f45cf4d1ba90ccf8f09241bd5b6990e107599646d7cc5033bb3161498b6579d`  
		Last Modified: Fri, 03 Jan 2020 01:25:40 GMT  
		Size: 103.4 MB (103372104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:stretch` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e77757891729d3e36560eb870a2035cfcbf9b36a8277477ca01e7795eb12ebd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113207597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bca92b7eee089f5bd1ca5286bc2eeb00d133a01b670bfa14cc61b5ef7d7040`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:36 GMT
ADD file:ba40f5080cbd89c576c350bfe5acfe16f2ec59636fdb082efc3a8cef66ae7cb7 in / 
# Sat, 28 Dec 2019 04:43:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:34:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 28 Dec 2019 08:34:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:34:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Jan 2020 01:43:28 GMT
ENV JULIA_VERSION=1.3.1
# Fri, 03 Jan 2020 01:43:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Jan 2020 01:43:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:588374d57fdb5120d024340eef3d8927af23a5b806d41b4f049ee430a153c0b4`  
		Last Modified: Sat, 28 Dec 2019 04:49:14 GMT  
		Size: 20.4 MB (20385801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8800f1f8f3e7df8ea70c864fa05a2684a6c1c1d20167f3b9dec0c5814feed1`  
		Last Modified: Sat, 28 Dec 2019 08:37:39 GMT  
		Size: 6.5 MB (6526590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e4a9c3c7f2fe493b69a8c3c2d51517334fc138f303cf4648c29cebd64e3706`  
		Last Modified: Fri, 03 Jan 2020 01:45:26 GMT  
		Size: 86.3 MB (86295206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:stretch` - linux; 386

```console
$ docker pull julia@sha256:1ddad7f3323f65be0227e7e681b57508dc0be2f02b7ae4e922a6be32d0efafaf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130011765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdd4df3dbd07c2ee2d646ce79f4cb36521e74bc77425fc929c432275d4dc011`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:49:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 28 Dec 2019 08:49:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:49:44 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Jan 2020 01:43:10 GMT
ENV JULIA_VERSION=1.3.1
# Fri, 03 Jan 2020 01:43:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Jan 2020 01:43:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac678d514844f6878e3aea38bf67468dde5568f022bd6450d93c65628e3cc30a`  
		Last Modified: Sat, 28 Dec 2019 08:51:58 GMT  
		Size: 7.6 MB (7582356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890370330c3955ced3ef176c2ec08910a7d68e35b53c08d81735e7b639b42350`  
		Last Modified: Fri, 03 Jan 2020 01:44:49 GMT  
		Size: 99.3 MB (99277267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
