## `julia:alpine3.15`

```console
$ docker pull julia@sha256:5a115d135d595fdb6f5cdba845f72eee906dd707e48de61eac72157ac2bf9941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:ff319b672dcbfd21237bb530ba7492aa01c9178a5218917d1b89170c7cfaa5ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c1754b206335a99b344bcc53aacfbb467c4b47f9ad4924de72226e29c04025`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:31:25 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0dfb1f33ed58261036c68d7560d680df65801f4b059a05fe06e948193369c`  
		Last Modified: Mon, 12 Sep 2022 22:34:49 GMT  
		Size: 149.3 MB (149258181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
