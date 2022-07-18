## `julia:rc-alpine3.16`

```console
$ docker pull julia@sha256:ac2342a06d2e55253c3bdcda1cbcf2ad5d3257bf8e6825188e1f02263d757efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:rc-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:6994fb567ae9359ac32e706e4b1122ae0acc3cad0db3adfafa302affedcdfffa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaccd51cffabbfe395811d88c9b5c365d059a090f040c664cd26b0d9f61cdd`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:03:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 18 Jul 2022 21:03:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 21:03:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Jul 2022 21:03:08 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 21:03:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.0-rc3-musl-x86_64.tar.gz'; 			sha256='815d9d85382360a4caa3dfe39d64539ec32bf935e10098a116de3377a3feb2a6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 18 Jul 2022 21:03:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5a17de565cc1930791dd5fe055bae849d17a984c70b68fec71f7130c6f361e`  
		Last Modified: Mon, 18 Jul 2022 21:05:31 GMT  
		Size: 148.6 MB (148606411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
