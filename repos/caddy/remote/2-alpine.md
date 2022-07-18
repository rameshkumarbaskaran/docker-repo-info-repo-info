## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:3a377931e632e7fba354ce90baa770292ec1857457b72375e289de15aa7d9587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:2bd3f77e2d21db96ae5a1decdb8df220d98b96e7b812cf7d368828b16bf65ae6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17013356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99e5e593f69a4c70d75271117799e5796754e07429560f8f70a6a62a9c09b8e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 13 Jul 2022 07:46:52 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 13 Jul 2022 07:46:54 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Wed, 13 Jul 2022 07:46:54 GMT
ENV CADDY_VERSION=v2.5.2
# Wed, 13 Jul 2022 07:46:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 13 Jul 2022 07:46:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 13 Jul 2022 07:46:57 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 13 Jul 2022 07:46:57 GMT
ENV XDG_DATA_HOME=/data
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Jul 2022 07:46:57 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Jul 2022 07:46:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Jul 2022 07:46:58 GMT
EXPOSE 80
# Wed, 13 Jul 2022 07:46:58 GMT
EXPOSE 443
# Wed, 13 Jul 2022 07:46:58 GMT
EXPOSE 2019
# Wed, 13 Jul 2022 07:46:58 GMT
WORKDIR /srv
# Wed, 13 Jul 2022 07:46:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195e97acbd9f5678e292401c0fae3db777aff49e77f38d9cc3f101265b4cdf43`  
		Last Modified: Wed, 13 Jul 2022 07:47:21 GMT  
		Size: 291.6 KB (291593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441b702741191d81f669709a2af927df34f91029d7bdee74215cf2c65f2270cd`  
		Last Modified: Wed, 13 Jul 2022 07:47:21 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6330f4d2e50b7bf2126496a3e12ab164af1ad5972222a6dd6ad58fd449b11fe`  
		Last Modified: Wed, 13 Jul 2022 07:47:23 GMT  
		Size: 13.9 MB (13916892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acec8070f9fa557cb093f66f0b2af0db792a0452918c52d5528fcb4588ad492`  
		Last Modified: Wed, 13 Jul 2022 07:47:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cfed1b7a1730b6530049f91e299347b35f11e17371ebf5594b5beb6dffc1ce00
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16268387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6502abce0924aa453af3cfe208eaed6b2cc8c5c86a0654401f4b388851557`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 20:14:12 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 18 Jul 2022 20:14:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Mon, 18 Jul 2022 20:14:15 GMT
ENV CADDY_VERSION=v2.5.2
# Mon, 18 Jul 2022 20:14:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 18 Jul 2022 20:14:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 20:14:21 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 18 Jul 2022 20:14:22 GMT
ENV XDG_DATA_HOME=/data
# Mon, 18 Jul 2022 20:14:22 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Mon, 18 Jul 2022 20:14:23 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 18 Jul 2022 20:14:23 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 18 Jul 2022 20:14:23 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 18 Jul 2022 20:14:24 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 18 Jul 2022 20:14:24 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 18 Jul 2022 20:14:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 18 Jul 2022 20:14:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 18 Jul 2022 20:14:25 GMT
EXPOSE 80
# Mon, 18 Jul 2022 20:14:26 GMT
EXPOSE 443
# Mon, 18 Jul 2022 20:14:26 GMT
EXPOSE 2019
# Mon, 18 Jul 2022 20:14:27 GMT
WORKDIR /srv
# Mon, 18 Jul 2022 20:14:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd55c2ffb655db030265de0f3fd76fe026e17e68d87f50465dde4f83572d2498`  
		Last Modified: Mon, 18 Jul 2022 20:15:43 GMT  
		Size: 291.8 KB (291811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c540be71e6dbd54939047b9053bb535c1f1ad83df9da6b7e9ed4d707c27e92f`  
		Last Modified: Mon, 18 Jul 2022 20:15:42 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ebd5e62966b61b854fd1458e479ec41ebfca38b992919a3a4780843e1e1d94`  
		Last Modified: Mon, 18 Jul 2022 20:15:52 GMT  
		Size: 13.4 MB (13364162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b2d6bf21432c63feaa4962f64c274b569467c2f123363805fd62d3e9e85894`  
		Last Modified: Mon, 18 Jul 2022 20:15:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fbe0cafdb711c8750146cf97901295bae9837679fe2ebc7e1dd9fd543bf29d57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16056794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1070a903222f8f7077d3ab1a896a5a95fbcdde697612a691084f49303cb55da7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:14:05 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 18 Jul 2022 22:14:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Mon, 18 Jul 2022 22:14:08 GMT
ENV CADDY_VERSION=v2.5.2
# Mon, 18 Jul 2022 22:14:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 18 Jul 2022 22:14:14 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:14:14 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 18 Jul 2022 22:14:15 GMT
ENV XDG_DATA_HOME=/data
# Mon, 18 Jul 2022 22:14:15 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Mon, 18 Jul 2022 22:14:16 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 18 Jul 2022 22:14:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 18 Jul 2022 22:14:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 18 Jul 2022 22:14:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 18 Jul 2022 22:14:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 18 Jul 2022 22:14:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 18 Jul 2022 22:14:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 18 Jul 2022 22:14:19 GMT
EXPOSE 80
# Mon, 18 Jul 2022 22:14:19 GMT
EXPOSE 443
# Mon, 18 Jul 2022 22:14:20 GMT
EXPOSE 2019
# Mon, 18 Jul 2022 22:14:20 GMT
WORKDIR /srv
# Mon, 18 Jul 2022 22:14:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9805b70d5dfc4d65e1a1e1f659dc0944494a8a6895999dc5b6cc0b2d848334a`  
		Last Modified: Mon, 18 Jul 2022 22:15:36 GMT  
		Size: 290.8 KB (290757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9745c36aa57bfd2f4a283f3fcf69f62e4ff2a9f3e14d3a6f0e5fae2d22a06a49`  
		Last Modified: Mon, 18 Jul 2022 22:15:35 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53157176ed62bc9624354772d3eb073499188dc4f91526e3fcabdb1108148e8e`  
		Last Modified: Mon, 18 Jul 2022 22:15:44 GMT  
		Size: 13.3 MB (13347749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad2d41c7a719516a9ea121138080b9d1d80d21c606c87d9b5dc018ac128ae18`  
		Last Modified: Mon, 18 Jul 2022 22:15:35 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:7542ee62db8e10442071d4e9745bcd98f39619bcf9f516c1c9b4ecfc5cc0f3d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15721249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db56606eb0d00c279248ae38995824f79f994477565532beb03699a02e7f94af`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:18:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 18 Jul 2022 22:18:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Mon, 18 Jul 2022 22:18:33 GMT
ENV CADDY_VERSION=v2.5.2
# Mon, 18 Jul 2022 22:18:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 18 Jul 2022 22:18:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 22:18:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 18 Jul 2022 22:18:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 18 Jul 2022 22:18:39 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Mon, 18 Jul 2022 22:18:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 18 Jul 2022 22:18:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 18 Jul 2022 22:18:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 18 Jul 2022 22:18:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 18 Jul 2022 22:18:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 18 Jul 2022 22:18:45 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 18 Jul 2022 22:18:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 18 Jul 2022 22:18:47 GMT
EXPOSE 80
# Mon, 18 Jul 2022 22:18:48 GMT
EXPOSE 443
# Mon, 18 Jul 2022 22:18:49 GMT
EXPOSE 2019
# Mon, 18 Jul 2022 22:18:50 GMT
WORKDIR /srv
# Mon, 18 Jul 2022 22:18:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6867c1bed7442ba6f8c33877f0a64552b8eb6e640825b2b39521a3ee4d3b7`  
		Last Modified: Mon, 18 Jul 2022 22:19:26 GMT  
		Size: 291.5 KB (291464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d9d0dc3dac6c9ea9c214169993cbf654f21972b33784651a2e35c75b2c3332`  
		Last Modified: Mon, 18 Jul 2022 22:19:26 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818fab46ac8ba80668e14951d7ac785048f4df50fda97f61507062a61e3b1ad`  
		Last Modified: Mon, 18 Jul 2022 22:19:28 GMT  
		Size: 12.7 MB (12729160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef202eac441dd743baac9767af96c921d6a74c7b67ddb0da6989963669cc967`  
		Last Modified: Mon, 18 Jul 2022 22:19:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:8bf33283df3ab62c0987b87b518be60e587e8e8f492f9001c9f513126218c3a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15399196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b6dd61b467dc78c47f12742f5af2367935a9ffb8f6dcc8ce8382764c2d1ab8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 23 May 2022 19:16:51 GMT
ADD file:6a5450c8a7cee3ceda59e7cb350c54df4139b0f7b7cf49c8b31bb9c01646c3cd in / 
# Mon, 23 May 2022 19:16:53 GMT
CMD ["/bin/sh"]
# Wed, 13 Jul 2022 22:09:45 GMT
RUN apk add --no-cache ca-certificates mailcap
# Wed, 13 Jul 2022 22:09:52 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Wed, 13 Jul 2022 22:09:55 GMT
ENV CADDY_VERSION=v2.5.2
# Wed, 13 Jul 2022 22:10:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Wed, 13 Jul 2022 22:10:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 13 Jul 2022 22:10:16 GMT
ENV XDG_CONFIG_HOME=/config
# Wed, 13 Jul 2022 22:10:18 GMT
ENV XDG_DATA_HOME=/data
# Wed, 13 Jul 2022 22:10:21 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Wed, 13 Jul 2022 22:10:22 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Jul 2022 22:10:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Jul 2022 22:10:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Jul 2022 22:10:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Jul 2022 22:10:33 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Jul 2022 22:10:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Jul 2022 22:10:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Jul 2022 22:10:40 GMT
EXPOSE 80
# Wed, 13 Jul 2022 22:10:43 GMT
EXPOSE 443
# Wed, 13 Jul 2022 22:10:44 GMT
EXPOSE 2019
# Wed, 13 Jul 2022 22:10:48 GMT
WORKDIR /srv
# Wed, 13 Jul 2022 22:10:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d3deabf2a506ef6f5fa7c2a68bf27047574cef9908b30a97ff2d01ae539b089a`  
		Last Modified: Mon, 23 May 2022 19:09:13 GMT  
		Size: 2.8 MB (2789745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49126cc0b1f1c1e51c05b6d7443ed73b5fd2577d177ced4eb36ba827a6b9e68c`  
		Last Modified: Wed, 13 Jul 2022 22:12:19 GMT  
		Size: 293.9 KB (293940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f5f92095cf2a8c6afe25b29ea21344778855b89f160fed628effd01704c1c2`  
		Last Modified: Wed, 13 Jul 2022 22:12:18 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f12fbf7d78c1725ab5956092ae9577b979994dc526cbd9f8368c69ce317b692`  
		Last Modified: Wed, 13 Jul 2022 22:12:21 GMT  
		Size: 12.3 MB (12309531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a905929de5f23fe3fc6a3b51fc5e5ae5d69bb42d68a20069887fbae365e82fba`  
		Last Modified: Wed, 13 Jul 2022 22:12:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:28adfc1e1d82c412767e4b170580d554b8dbb36c1cb5b355005e2dc8c2eeb0b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a387c6224fd249160f6c2f8ffd24f60c57c927a1a599ce91609c9c27288434c7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:02:21 GMT
RUN apk add --no-cache ca-certificates mailcap
# Mon, 18 Jul 2022 21:02:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/979e498d6d01e1fe7c22db848a3e3bc65369183f/welcome/index.html"
# Mon, 18 Jul 2022 21:02:25 GMT
ENV CADDY_VERSION=v2.5.2
# Mon, 18 Jul 2022 21:02:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b19eb832e341f7bdb1c6fec2333564745a38f9aa814a14e7843a1b20468e0cdc6547977d3ae5a63d687dd7b9a68f90792e228020bf2481f916d9982322361632' ;; 		armhf)   binArch='armv6'; checksum='de401bdf04f67647df89439292726c3a37d833edd7313a72fe47d45aa18c93aa6ef5b8718ffc8accb70cd356c0e62fc1a18808cd4e2de2357e80d44aef168d19' ;; 		armv7)   binArch='armv7'; checksum='3fda191727748eb23805e0e765b5794333a31c265879d7d54af6ddaa94cef14534c8ea993a231cbf94855c388a9c9a613be64260e2a8add6cc8ae230c218c59e' ;; 		aarch64) binArch='arm64'; checksum='b71a6c7961b4b7acda6ec71b70db2e8695572196a283a56eb910d3da08867e6f298c6cf34c12ebc35235f3de3bc833109596b56a3560b03ca1c3bcdb53b59372' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='5c98c82b64dab878fdbd158d7b162c2bdb36ea9606b1c06b0c04ee2060e6a42f169c876c70eb3558acd37e25395c3ed1764c5753ede79a9e05dbf03cef69d410' ;; 		s390x)   binArch='s390x'; checksum='7c86521e8d3e75899f91106863e46a43be3cd76b5ae63be81e735ad849182b0c08a98b7f8cdd3d975aed9b4e741ed02b42fa8435ca95d893bb00850a53b78a5c' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.2/caddy_2.5.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Mon, 18 Jul 2022 21:02:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 18 Jul 2022 21:02:37 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 18 Jul 2022 21:02:38 GMT
ENV XDG_DATA_HOME=/data
# Mon, 18 Jul 2022 21:02:38 GMT
LABEL org.opencontainers.image.version=v2.5.2
# Mon, 18 Jul 2022 21:02:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 18 Jul 2022 21:02:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 18 Jul 2022 21:02:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 18 Jul 2022 21:02:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 18 Jul 2022 21:02:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 18 Jul 2022 21:02:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 18 Jul 2022 21:02:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 18 Jul 2022 21:02:45 GMT
EXPOSE 80
# Mon, 18 Jul 2022 21:02:45 GMT
EXPOSE 443
# Mon, 18 Jul 2022 21:02:46 GMT
EXPOSE 2019
# Mon, 18 Jul 2022 21:02:46 GMT
WORKDIR /srv
# Mon, 18 Jul 2022 21:02:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01286e5b65105b357bf83e8daa3cbc0a1a069a4d14af918fcd5475246f6af1b`  
		Last Modified: Mon, 18 Jul 2022 21:03:38 GMT  
		Size: 291.9 KB (291948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ce119bc29da400dd00bd331789e14fab9587661da4bb3e57835053afeb50b7`  
		Last Modified: Mon, 18 Jul 2022 21:03:37 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8470e2e663127d3838fb96d9115f33c868c378cea548725085b75d9f39599548`  
		Last Modified: Mon, 18 Jul 2022 21:03:40 GMT  
		Size: 13.5 MB (13460687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e115a0286c47b77821e5d98da581e1d3e1f85b3dd134111f6c27790d0c45fbae`  
		Last Modified: Mon, 18 Jul 2022 21:03:37 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
