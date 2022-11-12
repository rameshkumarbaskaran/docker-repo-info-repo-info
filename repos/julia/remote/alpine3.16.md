## `julia:alpine3.16`

```console
$ docker pull julia@sha256:dd890c913b91e4952c78302627353632973847f5978e5c488ddbb69a0df19a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:ae79edc9881849c56b096b5bd63c2f215eac4f8d6205185263993c52212be542
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149942296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aac600b90260d60d8676a07de5ed817409e91d18a7eb83f427615169adfc26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:20:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 12 Nov 2022 06:20:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:20:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 12 Nov 2022 06:20:49 GMT
ENV JULIA_VERSION=1.8.2
# Sat, 12 Nov 2022 06:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Sat, 12 Nov 2022 06:21:07 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Sat, 12 Nov 2022 06:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 06:21:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8bbcb55513d2f3441b4cbb0f2a3683a5cc7612a8983399385d007080499444`  
		Last Modified: Sat, 12 Nov 2022 06:22:38 GMT  
		Size: 147.1 MB (147135652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52afb2187c00cc42b45d1e3f88a258e4c7a7c1e774cdf33d5e42e4d9c84962e6`  
		Last Modified: Sat, 12 Nov 2022 06:22:15 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
