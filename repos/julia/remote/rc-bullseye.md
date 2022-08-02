## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:232fd69ca850bf749897afb9bca3f37b8f913cee5d42fb38a29e58e0dcd4ad1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:57492c8f2a161c33935c11d7cfe3800843e7eadb196c48c919bda0cfb8135aa4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180885032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f3cb743ebea2a42462f72a606d4a571752bc0109a27d29f0a9604eab80aa5c`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:38:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 04:38:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:38:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Aug 2022 04:38:15 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Tue, 02 Aug 2022 04:38:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 02 Aug 2022 04:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654fce16cc037ef8e49e9de0d93725a4c38623de2c39f225b0bdc609b3bf8743`  
		Last Modified: Tue, 02 Aug 2022 04:41:24 GMT  
		Size: 2.4 MB (2426463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719e99e0be6c930f3ea263b7ff4d190cff7fbd35ba6f84eca04c19902ec4fe72`  
		Last Modified: Tue, 02 Aug 2022 04:41:47 GMT  
		Size: 147.1 MB (147091812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d7fabc4545fd3213a25fb55fa0ae7a65595723586de5ae601d6b3cc719b70ba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173196241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9138302989fe8e44c97ec30b1534ead459b5bff4dffd87a4718e6b312372995f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:49:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 03:49:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 03:49:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Aug 2022 03:49:04 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Tue, 02 Aug 2022 03:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 02 Aug 2022 03:49:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8642deeb25c491828f0c5aea294f6ea9772e6c31acc0290872b44bc353b1fdae`  
		Last Modified: Tue, 02 Aug 2022 03:52:25 GMT  
		Size: 2.4 MB (2413549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c04260ef618b4b5157ebb402596afa57537704ac75d78234028480109ba16`  
		Last Modified: Tue, 02 Aug 2022 03:52:45 GMT  
		Size: 140.7 MB (140728388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:bb3a486fa405e3b376ce3ffc9a299f4e8c9d6d435476f1c4fe696379205de41a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178966380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75737d68c757cf3ee76e9802b0d53a669bc56e699a401f092203d914018f98e4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:27 GMT
ADD file:7f2bf44013d7848f051407d854b68c0d415a5328a3f5d241fca3150ce23bde65 in / 
# Tue, 12 Jul 2022 00:39:27 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 08:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 08:44:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 12 Jul 2022 08:44:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 08:44:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Jul 2022 18:52:47 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 18:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 18 Jul 2022 18:53:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1c0050b86a85a326857dbfa0456b3321f92df7e98ca468c048ee3e60dd14c923`  
		Last Modified: Tue, 12 Jul 2022 00:45:18 GMT  
		Size: 32.4 MB (32373949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8fcb888b2ca7532f4061b92646a6067a7828bf1ca63281ae9bf80dd400cb558`  
		Last Modified: Tue, 12 Jul 2022 08:47:54 GMT  
		Size: 2.5 MB (2529668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e6c9fadabe69a4c991a0c3de82a95b7246d0363f89db1e6bedacaffa405f79`  
		Last Modified: Mon, 18 Jul 2022 18:55:15 GMT  
		Size: 144.1 MB (144062763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
