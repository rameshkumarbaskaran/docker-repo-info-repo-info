## `julia:1-alpine3.17`

```console
$ docker pull julia@sha256:b170e1c112cb8d63d123411d7e1ed73d2951811a2c70853acb971e957056d391
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.17` - linux; amd64

```console
$ docker pull julia@sha256:096f5007f03d8483d090033575f0e0450963778d9982e1164346453c213a657c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154357768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca0bc940a79a8e0080432e956b45e23fd6511adf9000132cc5a33e3f95b67cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 24 Aug 2023 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.3-musl-x86_64.tar.gz'; 			sha256='90fbfb8621a523694de0280a1cd5e2040a49f4bd41e403f789caee945e63d03b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c81e50001c6b77fd39a1ccf3aebcacc5c51d202e8bc69d200a700c4f068e89`  
		Last Modified: Fri, 20 Oct 2023 16:03:10 GMT  
		Size: 151.0 MB (150978792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340ec744cc9d251133bc913aea4c6aa89c7056450afe77f4405a1097a09cf790`  
		Last Modified: Fri, 20 Oct 2023 16:03:01 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.17` - unknown; unknown

```console
$ docker pull julia@sha256:0dcf7ca219db4e0024921322ea6eb5f54c8a425b2263a223424706e2784091a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 KB (77212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f77db43f93b5e99585b8ad8afc25251bdffe2d706daf0e995c467c4b1e7414`

```dockerfile
```

-	Layers:
	-	`sha256:3ca26025824d126e6697ea32e886dea77631ee0a1bbc0ea4b79abaa813ca9c49`  
		Last Modified: Fri, 20 Oct 2023 16:03:01 GMT  
		Size: 64.8 KB (64776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d331735bf16ba834ed798fb7030bc9efc79bf01dac565182e27d9239e95f5ea6`  
		Last Modified: Fri, 20 Oct 2023 16:03:01 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json
