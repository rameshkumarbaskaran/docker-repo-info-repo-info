## `julia:bullseye`

```console
$ docker pull julia@sha256:7c4692c52359ca912894b0f50548c376a6649f0359679737aa52c27aaeaccb95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:b133d759a1e353de3652efa8af52803480d409122758e1893505c50d69294249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182215727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a09e5d8906089d309b9d86f32f7befb9503b5fc5119648bf0ea65597fa2f876`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 Nov 2023 18:59:25 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["bash"]
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 14 Nov 2023 18:59:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_VERSION=1.9.4
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.4-linux-x86_64.tar.gz'; 			sha256='07d20c4c2518833e2265ca0acee15b355463361aa4efdab858dad826cf94325c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.4-linux-aarch64.tar.gz'; 			sha256='541d0c5a9378f8d2fc384bb8595fc6ffe20d61054629a6e314fb2f8dfe2f2ade'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.4-linux-i686.tar.gz'; 			sha256='2b045a30c6ed8b14a5f4b7ecfb74ef2af7d70b85c9b513cd347886c8dace39bd'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.4-linux-ppc64le.tar.gz'; 			sha256='a5da86c0f0f4ef6d8645f74d8397a6e833831ee212de9edc52e4aefe8f368494'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c60e057edcfea14e3ce15acccfb621e32dc86818162c17d87964b1d6058ea00`  
		Last Modified: Tue, 19 Dec 2023 03:48:09 GMT  
		Size: 2.2 MB (2223229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fcf5ee0fe65cc872a0f3000365a56af7043ce44ab436341751fee9c5bd1976`  
		Last Modified: Tue, 19 Dec 2023 03:48:13 GMT  
		Size: 148.6 MB (148574254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244be9d8b4a5aec39e0edb8a1c40e37b8367b9b1de8f39018bc0c044d52c2c2`  
		Last Modified: Tue, 19 Dec 2023 03:48:08 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1ff706b81b6d80d7645671db16ff145fac5b2d343b87942c99985484da113c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ae9d38ce5781331ed526afba10ecd292f80914fac65125f70a8556daf8ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:5ac8dcd73346a0927097712ee185e71d5750c54b54d4dc677a609ff120fa639a`  
		Last Modified: Tue, 19 Dec 2023 03:48:09 GMT  
		Size: 2.2 MB (2231395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5637f682da6efb53227011c448b5c2be2fbb7bedc18daee843bab3225908dd`  
		Last Modified: Tue, 19 Dec 2023 03:48:08 GMT  
		Size: 18.2 KB (18152 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e93d5fd6ff2948c8cff1b98829e580a576ad28b018f217ced6083211fa18e344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175006550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430eef67f16dd22475f93edc2c2f16b9c1aa19fcc43feb9e3d1001ac5485762d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 Nov 2023 18:59:25 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["bash"]
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 14 Nov 2023 18:59:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_VERSION=1.9.4
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.4-linux-x86_64.tar.gz'; 			sha256='07d20c4c2518833e2265ca0acee15b355463361aa4efdab858dad826cf94325c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.4-linux-aarch64.tar.gz'; 			sha256='541d0c5a9378f8d2fc384bb8595fc6ffe20d61054629a6e314fb2f8dfe2f2ade'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.4-linux-i686.tar.gz'; 			sha256='2b045a30c6ed8b14a5f4b7ecfb74ef2af7d70b85c9b513cd347886c8dace39bd'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.4-linux-ppc64le.tar.gz'; 			sha256='a5da86c0f0f4ef6d8645f74d8397a6e833831ee212de9edc52e4aefe8f368494'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7125e296ac071a07e741c080fa505548be787bc563978ba1f28cbadf817a297`  
		Last Modified: Wed, 22 Nov 2023 11:43:36 GMT  
		Size: 2.2 MB (2210605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e49f9e29dfad28718cd108a919638b129d2262ff57b91ffe20461688b811be4`  
		Last Modified: Wed, 22 Nov 2023 11:45:31 GMT  
		Size: 142.7 MB (142731447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3400a0265f902d7d8c9e834d5073fe5df92d990c31a31d8b2c6d2558cb20e3`  
		Last Modified: Wed, 22 Nov 2023 11:45:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:fb2d38de8afc145ffbb6332acc6df70e86bc9d2b66b225dad2a6e580798c547d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebd96616f57b741f3fed5df6f64e01b74b1d9dbccea3ad773850dafabeb87e3`

```dockerfile
```

-	Layers:
	-	`sha256:46a6cdaf3cb65d639ac13c503e659475f686beefe4c4cc780d3f259614fcbb14`  
		Last Modified: Wed, 22 Nov 2023 11:45:27 GMT  
		Size: 2.2 MB (2231688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc944b0ea52d05826731138ee3e92df094ad55f33d67212e257f7e4720cf87a`  
		Last Modified: Wed, 22 Nov 2023 11:45:27 GMT  
		Size: 18.0 KB (17995 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:c1cb8017930d63f6849809677be50a0e345ebfe34e8423ecb328abb77ebfbfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172004220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaffddc5ef2c26bdf91d3dd2c1e6e97d8196bcfe0ee7c3a22ee40b32f745a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 Nov 2023 18:59:25 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["bash"]
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 14 Nov 2023 18:59:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_VERSION=1.9.4
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.4-linux-x86_64.tar.gz'; 			sha256='07d20c4c2518833e2265ca0acee15b355463361aa4efdab858dad826cf94325c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.4-linux-aarch64.tar.gz'; 			sha256='541d0c5a9378f8d2fc384bb8595fc6ffe20d61054629a6e314fb2f8dfe2f2ade'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.4-linux-i686.tar.gz'; 			sha256='2b045a30c6ed8b14a5f4b7ecfb74ef2af7d70b85c9b513cd347886c8dace39bd'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.4-linux-ppc64le.tar.gz'; 			sha256='a5da86c0f0f4ef6d8645f74d8397a6e833831ee212de9edc52e4aefe8f368494'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23658c2ab493f94360f6ab5ab17bae8f8d1e60c710db0487be133082644cdc9c`  
		Last Modified: Tue, 19 Dec 2023 03:47:59 GMT  
		Size: 2.3 MB (2328935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224c111ea3aca17bb0e6e4ce062bc7c0221a693dcb42cbc4505b56f4e70f520`  
		Last Modified: Tue, 19 Dec 2023 03:48:02 GMT  
		Size: 137.3 MB (137272228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a377d00a6f248890bf52f866818d681e3b825893b299947f9de2535af33aeda4`  
		Last Modified: Tue, 19 Dec 2023 03:47:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:beed137bab77368c2e96314bbb4a71e7f66730643ef0757f59624869d113bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d1a58789bf8fabf9d3af8ccc49fbb006c5608d2e6ac452b31d5dc470c3050`

```dockerfile
```

-	Layers:
	-	`sha256:51b1ab06cb626333a0ea5d5690391cf6c12f8cfd4cb737346bbdc49992bfa923`  
		Last Modified: Tue, 19 Dec 2023 03:47:58 GMT  
		Size: 17.9 KB (17906 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:ea71c018790103402d2ed6230f4b7977e372cef185f63c8585d5f4ce2f09d0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170706204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c2477050bb558031dcd8a526e0f3771be4a5dc4c4d8431a947b906596048c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 Nov 2023 18:59:25 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["bash"]
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 14 Nov 2023 18:59:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 14 Nov 2023 18:59:25 GMT
ENV JULIA_VERSION=1.9.4
# Tue, 14 Nov 2023 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.4-linux-x86_64.tar.gz'; 			sha256='07d20c4c2518833e2265ca0acee15b355463361aa4efdab858dad826cf94325c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.4-linux-aarch64.tar.gz'; 			sha256='541d0c5a9378f8d2fc384bb8595fc6ffe20d61054629a6e314fb2f8dfe2f2ade'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.4-linux-i686.tar.gz'; 			sha256='2b045a30c6ed8b14a5f4b7ecfb74ef2af7d70b85c9b513cd347886c8dace39bd'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.4-linux-ppc64le.tar.gz'; 			sha256='a5da86c0f0f4ef6d8645f74d8397a6e833831ee212de9edc52e4aefe8f368494'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.9.4","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.9.4?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 18:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dba17251d7ebde32646c984e46b9b02b6f3d7ab559026ad8fd99e5663840030`  
		Last Modified: Wed, 20 Dec 2023 08:36:54 GMT  
		Size: 2.4 MB (2425477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88af52233f1e85a52ae5aed7f74317476b5d691705c11dc3bc08aa1455bae0a`  
		Last Modified: Wed, 20 Dec 2023 08:40:00 GMT  
		Size: 133.0 MB (132986549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7aa19567800598d21ea269d8f2d7f1ec4f8d62811b427962756158943df63`  
		Last Modified: Wed, 20 Dec 2023 08:39:56 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:53636b07ff75020c17727c99a01c89100af29fbb1450abe62687184d642b2f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38564fd9385de46d7e1c05522f0ec24adedf32a80512aedb37d2b872f05618fa`

```dockerfile
```

-	Layers:
	-	`sha256:d215a66b6b394a7b6058070edb9387035bbaaae2f5e9548338d9a8b11c6c9507`  
		Last Modified: Wed, 20 Dec 2023 08:39:56 GMT  
		Size: 2.2 MB (2235898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb078cf22acf59febe4f2175089fd91cedc68962b6513acbf9e6ea86e87e156`  
		Last Modified: Wed, 20 Dec 2023 08:39:56 GMT  
		Size: 18.0 KB (18025 bytes)  
		MIME: application/vnd.in-toto+json
