## `julia:1-buster`

```console
$ docker pull julia@sha256:e73574570e9e24031a40c78e4c9462ba918efd0e4e8b690efab6ce158d569ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:c1dbf642041dc26fe7d653494e891567db2a01a0532b82a7171e2bb57b6236f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164828356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37870c090815160e5863b60807a9d48f1512f7447e2309852700faa875dc11f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:31:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 14:31:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:31:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 14:32:43 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 14:32:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 14:33:00 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:33:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874b20cef7bab861045118287da23b6e32edca29d752001c9cfce5c4afea1667`  
		Last Modified: Sat, 04 Feb 2023 14:35:13 GMT  
		Size: 4.5 MB (4470342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3088e24b09e56848899eb49fb103d1d93505b413c5ea8c007d08583cd936f6b`  
		Last Modified: Sat, 04 Feb 2023 14:36:46 GMT  
		Size: 133.2 MB (133217285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baecddd339f5dc735df51a8b06184ef7f48866294c1f4355b15109704ba7ec9`  
		Last Modified: Sat, 04 Feb 2023 14:36:24 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fff4363262879cf48bb3ed597e9400403b62e1c3c722d5520da2f53ad07ad436
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157258024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4d55656305ad488158fcd16b12c4769d97cf652f7b8de3c235bb65029c9e9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:54 GMT
ADD file:cf6ecb1d6b034b0d4fc309542cb25fff0c997661b323f524ecc258ac323e43f6 in / 
# Sat, 04 Feb 2023 06:17:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:30:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 08:30:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 08:30:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 08:31:05 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 08:31:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 08:31:22 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 08:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 08:31:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd2853c1424a5596deda2f31e1f82920613a03c667c3ff58cb461340b7bb89cd`  
		Last Modified: Sat, 04 Feb 2023 06:22:04 GMT  
		Size: 25.9 MB (25922631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7b8a68c3a4fcf7be203f3081237c9d56a6f6712134055121da5049be63c5bf`  
		Last Modified: Sat, 04 Feb 2023 08:32:59 GMT  
		Size: 4.3 MB (4348655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed51eca53582d05dbdf9bd28499478df76f472a4f448f69b619e90ff5b964571`  
		Last Modified: Sat, 04 Feb 2023 08:34:12 GMT  
		Size: 127.0 MB (126986366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b8a8f5f866066677cadafcefe4585904f1a93ff5d5831f024226a5e8176511`  
		Last Modified: Sat, 04 Feb 2023 08:33:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:db3a0b9115908b989e62ace911a8369352e268d03ecba65d2f60b5fcde909238
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367dc7d746a0afae4432376777025bd80409e4415e8d600115486a865141527c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:48 GMT
ADD file:060bbacc8df3d1b157ff409535b3ea29dd0b5667425e3dcf6e60556dcfa4e7f1 in / 
# Sat, 04 Feb 2023 07:49:48 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:59:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:59:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 09:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 09:59:40 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 10:00:39 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 10:00:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 10:01:00 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 10:01:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 10:01:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e0d975bedf8c90406704c677df48435cd2d53449ac9ab15a876323ceb95ff8f`  
		Last Modified: Sat, 04 Feb 2023 07:55:52 GMT  
		Size: 27.8 MB (27798503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc92db1da0811a9b2524f9ebc20218a075afbb70b2cdb47ba40872e24ae5e49a`  
		Last Modified: Sat, 04 Feb 2023 10:03:27 GMT  
		Size: 4.6 MB (4620127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa1b35ac86b8600994c83c78ff8b93adea11dc087de02f511eb0ea0b61532c3`  
		Last Modified: Sat, 04 Feb 2023 10:04:51 GMT  
		Size: 130.0 MB (129993512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d262ac51be707621c02c45d81a4e743e7dd61f201d62bdb8c0cdd9048b5b8775`  
		Last Modified: Sat, 04 Feb 2023 10:04:33 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
