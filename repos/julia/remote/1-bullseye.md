## `julia:1-bullseye`

```console
$ docker pull julia@sha256:bcb2ffd23d31febef82b2b386ba907b5e1265d35a58c5acbc20c24ccd5dbfe79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:074227d71fb273ae650c04fa9bc5543c36ffa4ee37f5a2f4b9330242425cd45d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182723811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eceb2675cfd34b512b888df19b35f02175487924230a507357edc44a83e960d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:00:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 20 Sep 2023 06:00:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:00:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 20 Sep 2023 06:01:21 GMT
ENV JULIA_VERSION=1.9.3
# Wed, 20 Sep 2023 06:01:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 20 Sep 2023 06:01:40 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 20 Sep 2023 06:01:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 06:01:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fb88c49f7b83d4855d02c927645b5ca3e4d7c865455789eeb0b0cd5ea70b5`  
		Last Modified: Wed, 20 Sep 2023 06:03:44 GMT  
		Size: 2.4 MB (2426728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5031e8f77295c846526db332a75d2f632a1b9cf4c701f3640f9f5277df14fe`  
		Last Modified: Wed, 20 Sep 2023 06:05:21 GMT  
		Size: 148.9 MB (148879000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb29a3880634998d6a115fead9e09138ec011844d59e516d19da3bf8fd01244`  
		Last Modified: Wed, 20 Sep 2023 06:04:59 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f2a71c9f797c7bf3db6eeace134e4dbaf0d4892b411e5f012276f35b01ccd41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175584234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98504ac1c341349c47060f4a5acef1a9463dbd7e67dab9ca8016e89e6243701c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 12:09:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:09:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 20 Sep 2023 12:09:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 12:09:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 20 Sep 2023 12:09:54 GMT
ENV JULIA_VERSION=1.9.3
# Wed, 20 Sep 2023 12:10:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 20 Sep 2023 12:10:12 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 20 Sep 2023 12:10:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Sep 2023 12:10:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a79191cd5b087ed753f4773aa313f183a381a7b7327a871244596bee4bfa725`  
		Last Modified: Wed, 20 Sep 2023 12:11:52 GMT  
		Size: 2.4 MB (2414375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19aa8e892702bd85d39d18008100d3a063d964c5be9dce531684a45b9475095`  
		Last Modified: Wed, 20 Sep 2023 12:13:07 GMT  
		Size: 143.1 MB (143106617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf5ed98e98fe89a2ecc99fb52a8ffc7d260c7e310e8d2ba1d31068beb97cdae`  
		Last Modified: Wed, 20 Sep 2023 12:12:50 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:0146be33aa3e9db48200c502c83f9eb9419018ddc87a1e44601ae94e3e693027
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172546511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8231f04914ce388e76d6d1abd5a7a958f1fd1af99c771ae50b1c36193f828a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:23 GMT
ADD file:7da3a32fda5f1208b9e4a0151bc02b156c151608c0a2c17b70ca382b4446d87f in / 
# Thu, 07 Sep 2023 00:39:24 GMT
CMD ["bash"]
# Fri, 08 Sep 2023 01:24:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2023 01:24:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Sep 2023 01:24:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2023 01:24:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Sep 2023 01:25:45 GMT
ENV JULIA_VERSION=1.9.3
# Fri, 08 Sep 2023 01:26:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 08 Sep 2023 01:26:12 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Fri, 08 Sep 2023 01:26:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2023 01:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2508d8884943a2a8ff1cc6a8264b3085b7d7637e9de43269faf016019de5c311`  
		Last Modified: Thu, 07 Sep 2023 00:44:37 GMT  
		Size: 32.4 MB (32397335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cdf94e119ca52df0c509d64e2278c99927fa76e98213d152a6f930fc8158eb`  
		Last Modified: Fri, 08 Sep 2023 01:28:28 GMT  
		Size: 2.5 MB (2532533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59e6149989f4876695b401c806a8c4bff528811e096f9b249e12be029a76c91`  
		Last Modified: Fri, 08 Sep 2023 01:30:26 GMT  
		Size: 137.6 MB (137616268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5036e4bf52996329e31820812918d9c667afd60b6c6bb353146384ae65ab77`  
		Last Modified: Fri, 08 Sep 2023 01:29:55 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:80a065ba9bbdfeadfc832a2b357ee36d8277916624d24d1b2202daf0e116812a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171136386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b960bf2139783bbf02acfc08d7efaad86a6a91af6f8fe5adaf4bec7c3c7ca821`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:08:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 07 Sep 2023 01:08:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 01:08:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 07 Sep 2023 01:11:13 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 07 Sep 2023 01:12:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 07 Sep 2023 01:12:14 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:12:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763a9dca659fe70ee1f5710903bfed94beb26f6d9179c949a6683fd983fe4df`  
		Last Modified: Thu, 07 Sep 2023 01:13:35 GMT  
		Size: 2.6 MB (2627565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cb8a431de14cca092929095a60c073bf1a51530f23708fef564c6572bc1a9e`  
		Last Modified: Thu, 07 Sep 2023 01:15:55 GMT  
		Size: 133.2 MB (133217379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9c2aabcf9437494388405be666a9c99223d1a8795b5943248797a02efbd4d4`  
		Last Modified: Thu, 07 Sep 2023 01:15:18 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
