## `julia:rc-buster`

```console
$ docker pull julia@sha256:3d60c81b8d3fa9f2a77973b495e563bc79a980fe57dafb3b51e166bc1df2eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:f5325efa87eaa85e4e6cbded515034e1f8275d7957857ef30ef1162b2f4ae339
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175221549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e43dc3961f478a30695dc7a1126c6bf8243536ff11dd749c98cca0a566726ce`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:37:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 04:37:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 May 2022 04:37:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 04:37:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 May 2022 04:37:48 GMT
ENV JULIA_VERSION=1.8.0-beta3
# Wed, 11 May 2022 04:38:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-beta3-linux-x86_64.tar.gz'; 			sha256='749b2f3c6832a7b34404838e579de94c369173250c07071383cb499f14812655'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-beta3-linux-aarch64.tar.gz'; 			sha256='43d23f114a2a8217f30072bb98613ed45a9930106dbe741577963571f186afc7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-beta3-linux-i686.tar.gz'; 			sha256='4f10e62f02d7969f971f0497ccdd57656615f20d3e5ca4f206d0caf8b64ce1ca'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 11 May 2022 04:38:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f835ab6eeb8f37becd7cbe24d50c8189e7c433230a112166c07b02c7b311119`  
		Last Modified: Wed, 11 May 2022 04:40:54 GMT  
		Size: 4.5 MB (4468152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81100c6275717a02fdd31f916303e853021082e00ad5d4d310704052a079b23c`  
		Last Modified: Wed, 11 May 2022 04:41:15 GMT  
		Size: 143.6 MB (143612675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:156794023134b987ec91f9a1f29bb7a0ef480818029eab7b407358006af70c35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167421141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f5eefdb96a85efeb46ca892d371e5daa17753913839e4ebb9094f35b7157fc`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:34:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 28 May 2022 02:34:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:34:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 28 May 2022 02:34:59 GMT
ENV JULIA_VERSION=1.8.0-beta3
# Sat, 28 May 2022 02:35:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-beta3-linux-x86_64.tar.gz'; 			sha256='749b2f3c6832a7b34404838e579de94c369173250c07071383cb499f14812655'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-beta3-linux-aarch64.tar.gz'; 			sha256='43d23f114a2a8217f30072bb98613ed45a9930106dbe741577963571f186afc7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-beta3-linux-i686.tar.gz'; 			sha256='4f10e62f02d7969f971f0497ccdd57656615f20d3e5ca4f206d0caf8b64ce1ca'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 28 May 2022 02:35:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc371f868dbfc86f00f21fb937bee8a4ad6005b956e2af368cdb394d46bd9d6`  
		Last Modified: Sat, 28 May 2022 02:38:20 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cc87eb28de985c9d4f2115976d5cf026762234ce29cc35acceb2a22524db59`  
		Last Modified: Sat, 28 May 2022 02:38:40 GMT  
		Size: 137.2 MB (137160227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; 386

```console
$ docker pull julia@sha256:da1b6426350bbfd02ab1051d8cf029e90e70823a85f84f76d1d47ea29a504bb1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171115897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16bad6ce719ce6c8dbd82370460acff109dcf098230b48967d4fdf437996d2`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 11 May 2022 01:39:41 GMT
ADD file:fc7b00a8a5b0e703ac3ede5e2e51257f5ee709fcd35fee53e7b99d144cd873e4 in / 
# Wed, 11 May 2022 01:39:42 GMT
CMD ["bash"]
# Wed, 11 May 2022 04:26:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 04:26:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 11 May 2022 04:26:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 04:26:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 11 May 2022 04:26:24 GMT
ENV JULIA_VERSION=1.8.0-beta3
# Wed, 11 May 2022 04:26:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-beta3-linux-x86_64.tar.gz'; 			sha256='749b2f3c6832a7b34404838e579de94c369173250c07071383cb499f14812655'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-beta3-linux-aarch64.tar.gz'; 			sha256='43d23f114a2a8217f30072bb98613ed45a9930106dbe741577963571f186afc7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-beta3-linux-i686.tar.gz'; 			sha256='4f10e62f02d7969f971f0497ccdd57656615f20d3e5ca4f206d0caf8b64ce1ca'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 11 May 2022 04:26:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1c376c64b69c16b8b035dfd04b99bb7769a5afdfb56a1241aa4ec8743e85aa7`  
		Last Modified: Wed, 11 May 2022 01:47:22 GMT  
		Size: 27.8 MB (27799149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44763361e94a796a1177e74a30cf54fcd263fe26bf67befbe53acefd445f7949`  
		Last Modified: Wed, 11 May 2022 04:29:53 GMT  
		Size: 4.6 MB (4615843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6bcf503871045485f7b1921aff141ca16009678fef59f4b0fb0be6ecf72d5f`  
		Last Modified: Wed, 11 May 2022 04:30:12 GMT  
		Size: 138.7 MB (138700905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
