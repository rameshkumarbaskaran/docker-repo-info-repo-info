## `julia:1-alpine`

```console
$ docker pull julia@sha256:f58269c268bbc3ee2868201064635c8e63f41ad5eafa0fdee1fd58cb17373c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:ada715e8d8f83ef529e2a47f7841110d47e4b2b2e55f35e7d5da30dbd6cde449
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137058350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522cdc1172555f180d9d32a0a52a51069cb290c3e92e2e421be26b21af63dd6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 20:56:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 01 Dec 2022 20:56:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Dec 2022 20:56:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 01 Dec 2022 20:57:15 GMT
ENV JULIA_VERSION=1.8.3
# Thu, 01 Dec 2022 20:57:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.3-musl-x86_64.tar.gz'; 			sha256='6d0e20c9497cbee88b90dfbbbbf3d2701eb5e2902a85693fcaec3412920b63e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 01 Dec 2022 20:57:29 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 01 Dec 2022 20:57:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Dec 2022 20:57:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ba232d17faff1225d07fe482ad93cef095554d19deb5856b0677a3815a8685`  
		Last Modified: Thu, 01 Dec 2022 20:59:52 GMT  
		Size: 133.7 MB (133687270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1433f10ca62224a978e28e19a2ff406c62ca1bf3278dc1327acc71d332a68e8`  
		Last Modified: Thu, 01 Dec 2022 20:59:30 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
