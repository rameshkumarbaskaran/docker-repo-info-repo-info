## `julia:rc-buster`

```console
$ docker pull julia@sha256:806acbcfc9253b8b6b77a719e59899823fafd51386a08fd4aae37c9a168f49cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:f7d2a0ddade368088506825440e8b7a51dfdbc4d727cfd6904d87f416521620c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178717010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d238524b44186dbd4e817c3dc75052210ed7c6156315db04eaf5c1af7b94ad3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 07:13:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 07:13:42 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 09 Feb 2023 07:13:42 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 07:13:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 09 Feb 2023 07:13:42 GMT
ENV JULIA_VERSION=1.9.0-beta3
# Thu, 09 Feb 2023 07:14:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta3-linux-x86_64.tar.gz'; 			sha256='7b1a595c33e8fdf6e6dc04a9cecea90ca56dd8cc1e3a5a78a8e62bb22a02fbeb'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta3-linux-aarch64.tar.gz'; 			sha256='e44cafb91ab811ae01e702e50dfcd1176f4506101b274807fca49c6e80b442ab'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta3-linux-i686.tar.gz'; 			sha256='b6bb6d60753da455055f85fbdfa56ce749e28148891087dffd9e7ba11726fb82'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-beta3-linux-ppc64le.tar.gz'; 			sha256='b1694cd02f99c6d6cee769ebaf44b7e6ab112ec8a31ae3e115a5a29544fe7c90'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 09 Feb 2023 07:14:01 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 09 Feb 2023 07:14:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 07:14:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49333788b4e8f94f2c6012bf25eb919cce9607f9ce86f3240f5445d05d90aca1`  
		Last Modified: Thu, 09 Feb 2023 07:17:06 GMT  
		Size: 4.5 MB (4470371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d353b9d4fcc543c34b5b2a78709a8ac6ca830ba8282e30fd008d439919ae50ee`  
		Last Modified: Thu, 09 Feb 2023 07:17:29 GMT  
		Size: 147.1 MB (147105732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115b8974a25c3a4a44e726c139451aef158baa53c64f52df71ff33a2629656b8`  
		Last Modified: Thu, 09 Feb 2023 07:17:05 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:569b70ea2f0d7db403fc35c1d6cde9b3506c4349e89a00fff62b3f8d8179c729
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171360287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2591661f6b9d1253de65e8daa1ec7f44b8f646f2d67b47bdc871fa47cd54170a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:41:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:41:00 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 09 Feb 2023 13:41:00 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 13:41:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 09 Feb 2023 13:41:00 GMT
ENV JULIA_VERSION=1.9.0-beta3
# Thu, 09 Feb 2023 13:41:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta3-linux-x86_64.tar.gz'; 			sha256='7b1a595c33e8fdf6e6dc04a9cecea90ca56dd8cc1e3a5a78a8e62bb22a02fbeb'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta3-linux-aarch64.tar.gz'; 			sha256='e44cafb91ab811ae01e702e50dfcd1176f4506101b274807fca49c6e80b442ab'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta3-linux-i686.tar.gz'; 			sha256='b6bb6d60753da455055f85fbdfa56ce749e28148891087dffd9e7ba11726fb82'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-beta3-linux-ppc64le.tar.gz'; 			sha256='b1694cd02f99c6d6cee769ebaf44b7e6ab112ec8a31ae3e115a5a29544fe7c90'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 09 Feb 2023 13:41:18 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 09 Feb 2023 13:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:41:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b5328a5574a49c9747471386eb9c91ffdf7d3e3e46bcf777d7c7b6b1190b7a`  
		Last Modified: Thu, 09 Feb 2023 13:43:37 GMT  
		Size: 4.3 MB (4348747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52914ae9a5ff0b8ad570ac14ceda90f83cd3a64f84bf97426047decfdf96c7b1`  
		Last Modified: Thu, 09 Feb 2023 13:43:54 GMT  
		Size: 141.1 MB (141088340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8730c2c7fd0c6c714e0f711b8cc8a068f8db64a055b3c35638b2741b06d3097f`  
		Last Modified: Thu, 09 Feb 2023 13:43:37 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; 386

```console
$ docker pull julia@sha256:8781a03ade0b5a4ab68067eb0323f52c1bcc03c53e161f925c648e06b4cc43b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176828586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66030c5378502784bb846f62e4255f2d808653a2921a6e01eae70865d0f6142`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 09 Feb 2023 05:13:20 GMT
ADD file:2d19c71df422a9624e6fb34d6f87307703e1eaa800067eb1c594dd2b1778980f in / 
# Thu, 09 Feb 2023 05:13:21 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:29:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:29:45 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 09 Feb 2023 12:29:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 12:29:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 09 Feb 2023 12:29:48 GMT
ENV JULIA_VERSION=1.9.0-beta3
# Thu, 09 Feb 2023 12:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-beta3-linux-x86_64.tar.gz'; 			sha256='7b1a595c33e8fdf6e6dc04a9cecea90ca56dd8cc1e3a5a78a8e62bb22a02fbeb'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-beta3-linux-aarch64.tar.gz'; 			sha256='e44cafb91ab811ae01e702e50dfcd1176f4506101b274807fca49c6e80b442ab'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-beta3-linux-i686.tar.gz'; 			sha256='b6bb6d60753da455055f85fbdfa56ce749e28148891087dffd9e7ba11726fb82'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.0-beta3-linux-ppc64le.tar.gz'; 			sha256='b1694cd02f99c6d6cee769ebaf44b7e6ab112ec8a31ae3e115a5a29544fe7c90'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 09 Feb 2023 12:30:10 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 09 Feb 2023 12:30:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:30:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bacc4719e321895e65d456a3375ac7c1f594877d62056057ca20a3229ce824cd`  
		Last Modified: Thu, 09 Feb 2023 05:19:30 GMT  
		Size: 27.8 MB (27798198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a06108e05f745651eb64644f693be79b8ec07b5ec54f95b9fb0bf40eb98e5b`  
		Last Modified: Thu, 09 Feb 2023 12:33:37 GMT  
		Size: 4.6 MB (4620164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95297c35448957410939c4bb14cd0037d4654107b73a95693826c765cfc6140a`  
		Last Modified: Thu, 09 Feb 2023 12:33:56 GMT  
		Size: 144.4 MB (144409849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdd2dd9297711d86026879362f6b5addf150cdaf68f2406ed7d8ead382d514e`  
		Last Modified: Thu, 09 Feb 2023 12:33:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
