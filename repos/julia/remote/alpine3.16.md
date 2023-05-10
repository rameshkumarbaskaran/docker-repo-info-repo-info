## `julia:alpine3.16`

```console
$ docker pull julia@sha256:763d4fe70f91a882f2bfc9a14685ae955508b713f0038b4669fbdefa8940c93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:73d45ef39386287ad30893ab233a78202c6323069ba188f45cc7038df8efda82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153393111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9851e0604e99e9da441f681c09ddd088a92529b6d93bd1a0546d0718defed1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:05:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 Mar 2023 22:05:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 22:05:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 May 2023 17:54:16 GMT
ENV JULIA_VERSION=1.9.0
# Wed, 10 May 2023 17:54:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.9/julia-1.9.0-musl-x86_64.tar.gz'; 			sha256='2594ff9a69d86415faae2e2e218ec3a5abbeb41ab3590b646b75824221adcb5b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 10 May 2023 17:54:30 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Wed, 10 May 2023 17:54:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 May 2023 17:54:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fc557174d91131e4817ff1cce0b29984273f03d25b2c59eb601d11b94aede5`  
		Last Modified: Wed, 10 May 2023 17:57:18 GMT  
		Size: 150.6 MB (150584936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde2e5bd2b37a2cb69a7d3be364580977d5b4e5054efee42ec5fa4be5242267`  
		Last Modified: Wed, 10 May 2023 17:56:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
