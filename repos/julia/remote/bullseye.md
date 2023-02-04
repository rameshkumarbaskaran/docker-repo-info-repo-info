## `julia:bullseye`

```console
$ docker pull julia@sha256:fd44046cc6ba562bd74e19327dfd91ca94b66f49205913ce966e0c670f832942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:bc415ca2ca09925f259ae0355da5d41ba26862190aee9e9d21036679dc77350c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167022270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7642cec7d858ee89f9fb328416204d01c53a271b23a77cdd7831e42ae2539e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:31:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 14:31:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:31:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 14:32:19 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 14:32:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 14:32:36 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:32:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:32:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdaf596c9241a85e680c5d9139457b704cd3d0e6c4d0a92777fb3c8f91e2f72`  
		Last Modified: Sat, 04 Feb 2023 14:34:38 GMT  
		Size: 2.4 MB (2426559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bac721e7cf89ff72b2731a384c134cb1256118c343aa5db1be19e727446a6f`  
		Last Modified: Sat, 04 Feb 2023 14:36:12 GMT  
		Size: 133.2 MB (133198415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed0a3a6985ec67e06805f041005ee12251b4cc2a3ae166d68ab1345fe74b3fb`  
		Last Modified: Sat, 04 Feb 2023 14:35:50 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f7e262c3745a35061ac242e7124d4c2dd147b2a8d755ffdc5ee4a3773bac2305
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159430625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7050f11a73ed1a303682d8cde139d15c2ae1ed719f621aff1cad57c08a0885a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:29:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:29:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 08:29:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 08:29:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 08:30:45 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 08:31:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 08:31:02 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 08:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 08:31:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbce9bf528576bb895c59d7b207130ef4e92417f2b708b562d3fd76a4b829f`  
		Last Modified: Sat, 04 Feb 2023 08:32:30 GMT  
		Size: 2.4 MB (2414182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8562475d0e63f6378191b9a2908ae3021b7d058b8a25c51e0f1ea6c1e1e37d5`  
		Last Modified: Sat, 04 Feb 2023 08:33:43 GMT  
		Size: 127.0 MB (126971275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fbc956db2430df7ba77520e27f4ce41516d528b008f43ff2770ef00806411b`  
		Last Modified: Sat, 04 Feb 2023 08:33:27 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:5c2719f0cebe9fe2958e33c2091ebef5fcfdbdde3d9e28074e926fa9f9aec16b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164895790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7316caf5828f89325865deea99d085231afe7b57111f495c86136eecb1b2885e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:22 GMT
ADD file:82af884aad6a87f5b309a7418aa1df69f92180a39818ae6d77d37d072cb6fecb in / 
# Sat, 04 Feb 2023 07:49:22 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:58:53 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 09:58:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 09:58:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 10:00:08 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 10:00:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 10:00:33 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 10:00:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 10:00:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fb99e0a97d653ef9acb2bdac0d1d10a8655b789bd4e8924c4a1c4a2af8adbb4a`  
		Last Modified: Sat, 04 Feb 2023 07:55:04 GMT  
		Size: 32.4 MB (32375772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc613bce2fee944eac78d194e91eff6c3e5b0df148cbb33d397f06b2a37407`  
		Last Modified: Sat, 04 Feb 2023 10:02:54 GMT  
		Size: 2.5 MB (2531770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04aed35a32b7fa7e536edfc106a63b57e914aa43be8634ad10a6e78be7f8e012`  
		Last Modified: Sat, 04 Feb 2023 10:04:17 GMT  
		Size: 130.0 MB (129987870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef7c4d5ab8affe6a556d2be95e6ae47863dc4ff58e566fcc36e24c3e61ba611`  
		Last Modified: Sat, 04 Feb 2023 10:03:59 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:33d6f77b4854ca8abe99e06d300d379ffa453f4e94cd7de10f9f2adb3b8bff75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155921812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153365eabce84f5510e05fe0fcd7190da79ac92e4295574def03fa17383847fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 04 Feb 2023 12:25:55 GMT
ADD file:2c82cc89d7ac2efeaf54e7589e28644e3e8436d66f6909bf295a2b030116ac58 in / 
# Sat, 04 Feb 2023 12:25:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:33:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:33:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 04 Feb 2023 13:33:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 13:33:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 04 Feb 2023 13:34:49 GMT
ENV JULIA_VERSION=1.8.5
# Sat, 04 Feb 2023 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.5-linux-x86_64.tar.gz'; 			sha256='e71a24816e8fe9d5f4807664cbbb42738f5aa9fe05397d35c81d4c5d649b9d05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.5-linux-aarch64.tar.gz'; 			sha256='a1f637b44c71ea9bc96d7c3ef347724c054a1e5227b980adebfc33599e5153a4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.5-linux-i686.tar.gz'; 			sha256='f0edd61970710333cb5ac6491fbbc859436e5e9e84b014ae04f291bddf6a7e21'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.8/julia-1.8.5-linux-ppc64le.tar.gz'; 			sha256='13c121362e73cda8049a9b51b15c6d0d1dc66803db45ab1d5c46ea9c1b7440df'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Sat, 04 Feb 2023 13:35:35 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 04 Feb 2023 13:35:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 13:35:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0604364135762a6c4b3503dd7f0396a51396443bf6052b34b8df7f67679b42c0`  
		Last Modified: Sat, 04 Feb 2023 12:32:12 GMT  
		Size: 35.3 MB (35268795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f9e81f4401abe19efc0a30bca6f819213cda09321b556bde3929d8df216dab`  
		Last Modified: Sat, 04 Feb 2023 13:36:17 GMT  
		Size: 2.6 MB (2627244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2720f00c8a0fd25e0b0a3da535ab5418342bb6bd18fc0089fb42fca3f0a2ccd9`  
		Last Modified: Sat, 04 Feb 2023 13:37:41 GMT  
		Size: 118.0 MB (118025400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb58dd1e101aa0f942108403e6af427d823dedf7e1470156d4c763721ab1ae76`  
		Last Modified: Sat, 04 Feb 2023 13:37:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
