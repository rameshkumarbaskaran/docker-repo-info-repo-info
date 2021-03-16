## `julia:1-alpine3.12`

```console
$ docker pull julia@sha256:fe04d7250352d47fdf97ec2c647ca138e42c8b0031e31209921232bc66a58d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `julia:1-alpine3.12` - linux; amd64

```console
$ docker pull julia@sha256:397bdaf984986e9053cbffe76d96e17d1129d1355d053090557a920ef0da0154
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112354718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787cc8d0d7fe9522e9b978792b574d173d48f04c60d395c5e9e1c63f92e6ca62`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 11:10:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 12 Mar 2021 11:10:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 11:10:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 15 Mar 2021 19:21:11 GMT
ENV JULIA_VERSION=1.5.4
# Mon, 15 Mar 2021 19:21:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='7bc70fde541e8f146adfbe1d083c2efbbae2690c1634b2c1947c41cd4b9b2fa3' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 15 Mar 2021 19:21:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07e0f49a31c94cdab1c41f25eeb8bd9366d33790744d6d3330fefbc33d79088`  
		Last Modified: Mon, 15 Mar 2021 19:25:18 GMT  
		Size: 109.6 MB (109555225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
