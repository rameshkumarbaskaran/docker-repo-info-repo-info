<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2`](#kong2)
-	[`kong:2.0`](#kong20)
-	[`kong:2.0.5`](#kong205)
-	[`kong:2.0.5-alpine`](#kong205-alpine)
-	[`kong:2.0.5-centos`](#kong205-centos)
-	[`kong:2.0.5-ubuntu`](#kong205-ubuntu)
-	[`kong:2.0-centos`](#kong20-centos)
-	[`kong:2.0-ubuntu`](#kong20-ubuntu)
-	[`kong:2.1`](#kong21)
-	[`kong:2.1.4`](#kong214)
-	[`kong:2.1.4-alpine`](#kong214-alpine)
-	[`kong:2.1.4-centos`](#kong214-centos)
-	[`kong:2.1.4-ubuntu`](#kong214-ubuntu)
-	[`kong:2.1-alpine`](#kong21-alpine)
-	[`kong:2.1-centos`](#kong21-centos)
-	[`kong:2.1-ubuntu`](#kong21-ubuntu)
-	[`kong:2.2`](#kong22)
-	[`kong:2.2.0`](#kong220)
-	[`kong:2.2.1-alpine`](#kong221-alpine)
-	[`kong:2.2.1-centos`](#kong221-centos)
-	[`kong:2.2.1-ubuntu`](#kong221-ubuntu)
-	[`kong:2.2-alpine`](#kong22-alpine)
-	[`kong:2.2-centos`](#kong22-centos)
-	[`kong:2.2-ubuntu`](#kong22-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0`

```console
$ docker pull kong@sha256:694e8a2b046a28a846029e0e6b00f9087d644fab94435c872514c0673053087c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0` - linux; amd64

```console
$ docker pull kong@sha256:dcbcf61b6577441fd7d9b0b3729f4ae08a5d1bf7f277bcc79fd60fe3e110a15b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52761708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd6bc3dc6120ac04c63d99c82a2d117798dc4663ada08099c314d45bb49c9d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Fri, 10 Jul 2020 20:22:10 GMT
ARG KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:22:10 GMT
ENV KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:22:10 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Fri, 10 Jul 2020 20:22:11 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Fri, 10 Jul 2020 20:22:17 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Tue, 14 Jul 2020 20:21:10 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 14 Jul 2020 20:21:10 GMT
USER kong
# Tue, 14 Jul 2020 20:21:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jul 2020 20:21:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jul 2020 20:21:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jul 2020 20:21:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9927a578c07417ddbd09bec114df84f8a70d2dc31ed211de27e60350865702`  
		Last Modified: Fri, 10 Jul 2020 20:24:59 GMT  
		Size: 49.9 MB (49947527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d1ef16fef2b440996e796673a1b4cf393245998265d908753d82e07c122512`  
		Last Modified: Tue, 14 Jul 2020 20:22:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5`

```console
$ docker pull kong@sha256:694e8a2b046a28a846029e0e6b00f9087d644fab94435c872514c0673053087c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5` - linux; amd64

```console
$ docker pull kong@sha256:dcbcf61b6577441fd7d9b0b3729f4ae08a5d1bf7f277bcc79fd60fe3e110a15b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52761708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd6bc3dc6120ac04c63d99c82a2d117798dc4663ada08099c314d45bb49c9d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Fri, 10 Jul 2020 20:22:10 GMT
ARG KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:22:10 GMT
ENV KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:22:10 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Fri, 10 Jul 2020 20:22:11 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Fri, 10 Jul 2020 20:22:17 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Tue, 14 Jul 2020 20:21:10 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 14 Jul 2020 20:21:10 GMT
USER kong
# Tue, 14 Jul 2020 20:21:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jul 2020 20:21:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jul 2020 20:21:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jul 2020 20:21:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9927a578c07417ddbd09bec114df84f8a70d2dc31ed211de27e60350865702`  
		Last Modified: Fri, 10 Jul 2020 20:24:59 GMT  
		Size: 49.9 MB (49947527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d1ef16fef2b440996e796673a1b4cf393245998265d908753d82e07c122512`  
		Last Modified: Tue, 14 Jul 2020 20:22:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-alpine`

```console
$ docker pull kong@sha256:694e8a2b046a28a846029e0e6b00f9087d644fab94435c872514c0673053087c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:dcbcf61b6577441fd7d9b0b3729f4ae08a5d1bf7f277bcc79fd60fe3e110a15b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52761708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd6bc3dc6120ac04c63d99c82a2d117798dc4663ada08099c314d45bb49c9d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Tue, 05 May 2020 00:19:57 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Fri, 10 Jul 2020 20:22:10 GMT
ARG KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:22:10 GMT
ENV KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:22:10 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Fri, 10 Jul 2020 20:22:11 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Fri, 10 Jul 2020 20:22:17 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Tue, 14 Jul 2020 20:21:10 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 14 Jul 2020 20:21:10 GMT
USER kong
# Tue, 14 Jul 2020 20:21:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jul 2020 20:21:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jul 2020 20:21:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jul 2020 20:21:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79162f4c09617b6148c79941fef29989fd4efaf75afb688429147db76f1c1937`  
		Last Modified: Tue, 05 May 2020 00:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9927a578c07417ddbd09bec114df84f8a70d2dc31ed211de27e60350865702`  
		Last Modified: Fri, 10 Jul 2020 20:24:59 GMT  
		Size: 49.9 MB (49947527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d1ef16fef2b440996e796673a1b4cf393245998265d908753d82e07c122512`  
		Last Modified: Tue, 14 Jul 2020 20:22:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-centos`

```console
$ docker pull kong@sha256:079abab579c65a5b8d16be6cee38003ba4a57fd7e94b7de9168bb5c5d4d15ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-centos` - linux; amd64

```console
$ docker pull kong@sha256:554d9579ae5ccc7da6cfd7a742010c445cca0294e446abd55c10903c395e902b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127491262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9f5083661211369645dcdeb6b3f5338fd57bf7316dcde5c1258cad2f951eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:02:56 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:03:20 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 14 Nov 2020 01:03:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:03:21 GMT
USER kong
# Sat, 14 Nov 2020 01:03:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:03:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:03:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:03:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692b26149754880bb26d043fb2a9bba7fe1fb5406a67028d073895681609b4df`  
		Last Modified: Sat, 14 Nov 2020 01:04:21 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3c5952d48cacf33b16df4f8fac200bbecacd4350fd0629a4815eec28ff1cb`  
		Last Modified: Sat, 14 Nov 2020 01:04:31 GMT  
		Size: 51.4 MB (51393250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86ddac787b13b6ae84c90e260caa89eeb915b690116162d279d9fa5197477dc`  
		Last Modified: Sat, 14 Nov 2020 01:04:20 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-ubuntu`

```console
$ docker pull kong@sha256:c2a68e2ad6f3f4adc2d5343bab9382c6746f77edb50d231e73c0121563b870e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:0fb35a4763a4bfd0d25abf824420673561185497db6a71c654452d2c4ffc61fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100927546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7404cf91be9c9d798e371328fc8455a91645e8c8e3be463eb47c1393aea1d919`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:24:04 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 26 Nov 2020 01:24:04 GMT
ARG KONG_VERSION=2.0.5
# Thu, 26 Nov 2020 01:24:04 GMT
ENV KONG_VERSION=2.0.5
# Thu, 26 Nov 2020 01:24:24 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 26 Nov 2020 01:24:25 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 26 Nov 2020 01:24:25 GMT
USER kong
# Thu, 26 Nov 2020 01:24:26 GMT
RUN kong version
# Thu, 26 Nov 2020 01:24:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Nov 2020 01:24:26 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 26 Nov 2020 01:24:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Nov 2020 01:24:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3852c59f3f6ea2ff51034330ef1620d63097195d0e40b01e202b5d9940559f0`  
		Last Modified: Thu, 26 Nov 2020 01:25:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c22bd6b93608dfc625608394a1286e1794062a5426583308900f406990e236`  
		Last Modified: Thu, 26 Nov 2020 01:25:46 GMT  
		Size: 55.1 MB (55086821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220bade830edd554156140a5d49f1b57c79a51d10f8726c6515b9a9517d5dcb4`  
		Last Modified: Thu, 26 Nov 2020 01:25:35 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eb8cea719930282cbe3e6e3aafe1081ab1629021a265ec834cd274370dd838`  
		Last Modified: Thu, 26 Nov 2020 01:25:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0f300366bad5d9eba035bf1451aaff87ce06dafdeeb472e94dc2aafa4344a494
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93018128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd78574188a2781186eee913711bd8c62c1cef29fbbfe97a58e04bea92552997`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:28:34 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Wed, 25 Nov 2020 23:28:35 GMT
ARG KONG_VERSION=2.0.5
# Wed, 25 Nov 2020 23:28:36 GMT
ENV KONG_VERSION=2.0.5
# Wed, 25 Nov 2020 23:29:18 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Wed, 25 Nov 2020 23:29:20 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 25 Nov 2020 23:29:21 GMT
USER kong
# Wed, 25 Nov 2020 23:29:24 GMT
RUN kong version
# Wed, 25 Nov 2020 23:29:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Nov 2020 23:29:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 25 Nov 2020 23:29:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Nov 2020 23:29:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa89518f435ec6f9a0a429a54fc0c1efe5506570de4a2b477b3831010738e0`  
		Last Modified: Wed, 25 Nov 2020 23:30:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0854eeddb2934af892b9ff7ac40e9ac77296c7b4b02ad9896ee723326092cb32`  
		Last Modified: Wed, 25 Nov 2020 23:31:00 GMT  
		Size: 52.2 MB (52189622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93860ffaeb22fb36c81b7a964a388a78d3762b6fd001005d8250b27269d74683`  
		Last Modified: Wed, 25 Nov 2020 23:30:46 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bca7345029988cc3db286d56438da2694c4f13b8374f6e8473820cee87abf4e`  
		Last Modified: Wed, 25 Nov 2020 23:30:46 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-centos`

```console
$ docker pull kong@sha256:079abab579c65a5b8d16be6cee38003ba4a57fd7e94b7de9168bb5c5d4d15ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:554d9579ae5ccc7da6cfd7a742010c445cca0294e446abd55c10903c395e902b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127491262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9f5083661211369645dcdeb6b3f5338fd57bf7316dcde5c1258cad2f951eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:02:56 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:03:20 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 14 Nov 2020 01:03:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:03:21 GMT
USER kong
# Sat, 14 Nov 2020 01:03:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:03:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:03:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:03:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692b26149754880bb26d043fb2a9bba7fe1fb5406a67028d073895681609b4df`  
		Last Modified: Sat, 14 Nov 2020 01:04:21 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3c5952d48cacf33b16df4f8fac200bbecacd4350fd0629a4815eec28ff1cb`  
		Last Modified: Sat, 14 Nov 2020 01:04:31 GMT  
		Size: 51.4 MB (51393250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86ddac787b13b6ae84c90e260caa89eeb915b690116162d279d9fa5197477dc`  
		Last Modified: Sat, 14 Nov 2020 01:04:20 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-ubuntu`

```console
$ docker pull kong@sha256:c2a68e2ad6f3f4adc2d5343bab9382c6746f77edb50d231e73c0121563b870e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:0fb35a4763a4bfd0d25abf824420673561185497db6a71c654452d2c4ffc61fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100927546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7404cf91be9c9d798e371328fc8455a91645e8c8e3be463eb47c1393aea1d919`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:24:04 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 26 Nov 2020 01:24:04 GMT
ARG KONG_VERSION=2.0.5
# Thu, 26 Nov 2020 01:24:04 GMT
ENV KONG_VERSION=2.0.5
# Thu, 26 Nov 2020 01:24:24 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 26 Nov 2020 01:24:25 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 26 Nov 2020 01:24:25 GMT
USER kong
# Thu, 26 Nov 2020 01:24:26 GMT
RUN kong version
# Thu, 26 Nov 2020 01:24:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Nov 2020 01:24:26 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 26 Nov 2020 01:24:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Nov 2020 01:24:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3852c59f3f6ea2ff51034330ef1620d63097195d0e40b01e202b5d9940559f0`  
		Last Modified: Thu, 26 Nov 2020 01:25:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c22bd6b93608dfc625608394a1286e1794062a5426583308900f406990e236`  
		Last Modified: Thu, 26 Nov 2020 01:25:46 GMT  
		Size: 55.1 MB (55086821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220bade830edd554156140a5d49f1b57c79a51d10f8726c6515b9a9517d5dcb4`  
		Last Modified: Thu, 26 Nov 2020 01:25:35 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eb8cea719930282cbe3e6e3aafe1081ab1629021a265ec834cd274370dd838`  
		Last Modified: Thu, 26 Nov 2020 01:25:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0f300366bad5d9eba035bf1451aaff87ce06dafdeeb472e94dc2aafa4344a494
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93018128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd78574188a2781186eee913711bd8c62c1cef29fbbfe97a58e04bea92552997`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:28:34 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Wed, 25 Nov 2020 23:28:35 GMT
ARG KONG_VERSION=2.0.5
# Wed, 25 Nov 2020 23:28:36 GMT
ENV KONG_VERSION=2.0.5
# Wed, 25 Nov 2020 23:29:18 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Wed, 25 Nov 2020 23:29:20 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 25 Nov 2020 23:29:21 GMT
USER kong
# Wed, 25 Nov 2020 23:29:24 GMT
RUN kong version
# Wed, 25 Nov 2020 23:29:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Nov 2020 23:29:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 25 Nov 2020 23:29:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Nov 2020 23:29:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa89518f435ec6f9a0a429a54fc0c1efe5506570de4a2b477b3831010738e0`  
		Last Modified: Wed, 25 Nov 2020 23:30:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0854eeddb2934af892b9ff7ac40e9ac77296c7b4b02ad9896ee723326092cb32`  
		Last Modified: Wed, 25 Nov 2020 23:31:00 GMT  
		Size: 52.2 MB (52189622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93860ffaeb22fb36c81b7a964a388a78d3762b6fd001005d8250b27269d74683`  
		Last Modified: Wed, 25 Nov 2020 23:30:46 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bca7345029988cc3db286d56438da2694c4f13b8374f6e8473820cee87abf4e`  
		Last Modified: Wed, 25 Nov 2020 23:30:46 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1`

```console
$ docker pull kong@sha256:ea980a20d7d2a9166e9dac16bb6a1964d006e808eb00e8894ba267a90f9e0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1` - linux; amd64

```console
$ docker pull kong@sha256:32aec5d7a1152fad8604b74dfbfe544f8c346c42651791a768fd5f0025bc59b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53150431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55bcda861cae15b7310f14adc6b1f942f3d867ef30b6ff8da9268ac0ebd58a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 22 Sep 2020 18:32:31 GMT
ARG KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:31 GMT
ENV KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:37 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 22 Sep 2020 18:32:37 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 22 Sep 2020 18:32:37 GMT
USER kong
# Tue, 22 Sep 2020 18:32:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 22 Sep 2020 18:32:38 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 22 Sep 2020 18:32:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 22 Sep 2020 18:32:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306b16482a5463a3999b475a70c541b3eafcd2c4d3b6da8b5ae4d53bc49be14`  
		Last Modified: Tue, 22 Sep 2020 18:34:57 GMT  
		Size: 50.3 MB (50336253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff24278e47024f951b5e7834bbcb0a5ce4e0ea9086924d0a929eb960a35b3542`  
		Last Modified: Tue, 22 Sep 2020 18:34:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2ada4f5522df9afdcc8230d55d29842c321585b16258c46616a6d1e7ef8dc7a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d349242092b941662b5f7463ac4a33d865746d92ca9dfbf5ace92391d5cb0b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:51 GMT
ARG KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:57:53 GMT
ENV KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:58:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 17 Dec 2020 04:58:06 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:58:08 GMT
USER kong
# Thu, 17 Dec 2020 04:58:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:58:09 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:58:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:58:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8c4352649944a52a45f73f8267085e3e8f5f8c42cd7916f17e194af442ccdd`  
		Last Modified: Thu, 17 Dec 2020 04:59:39 GMT  
		Size: 49.9 MB (49938950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c2b84fa76be82f6d536a0c0a486863650800cfad97b972c7753461f8f4e3bc`  
		Last Modified: Thu, 17 Dec 2020 04:59:23 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4`

```console
$ docker pull kong@sha256:ea980a20d7d2a9166e9dac16bb6a1964d006e808eb00e8894ba267a90f9e0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4` - linux; amd64

```console
$ docker pull kong@sha256:32aec5d7a1152fad8604b74dfbfe544f8c346c42651791a768fd5f0025bc59b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53150431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55bcda861cae15b7310f14adc6b1f942f3d867ef30b6ff8da9268ac0ebd58a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 22 Sep 2020 18:32:31 GMT
ARG KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:31 GMT
ENV KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:37 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 22 Sep 2020 18:32:37 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 22 Sep 2020 18:32:37 GMT
USER kong
# Tue, 22 Sep 2020 18:32:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 22 Sep 2020 18:32:38 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 22 Sep 2020 18:32:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 22 Sep 2020 18:32:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306b16482a5463a3999b475a70c541b3eafcd2c4d3b6da8b5ae4d53bc49be14`  
		Last Modified: Tue, 22 Sep 2020 18:34:57 GMT  
		Size: 50.3 MB (50336253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff24278e47024f951b5e7834bbcb0a5ce4e0ea9086924d0a929eb960a35b3542`  
		Last Modified: Tue, 22 Sep 2020 18:34:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2ada4f5522df9afdcc8230d55d29842c321585b16258c46616a6d1e7ef8dc7a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d349242092b941662b5f7463ac4a33d865746d92ca9dfbf5ace92391d5cb0b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:51 GMT
ARG KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:57:53 GMT
ENV KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:58:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 17 Dec 2020 04:58:06 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:58:08 GMT
USER kong
# Thu, 17 Dec 2020 04:58:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:58:09 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:58:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:58:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8c4352649944a52a45f73f8267085e3e8f5f8c42cd7916f17e194af442ccdd`  
		Last Modified: Thu, 17 Dec 2020 04:59:39 GMT  
		Size: 49.9 MB (49938950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c2b84fa76be82f6d536a0c0a486863650800cfad97b972c7753461f8f4e3bc`  
		Last Modified: Thu, 17 Dec 2020 04:59:23 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-alpine`

```console
$ docker pull kong@sha256:ea980a20d7d2a9166e9dac16bb6a1964d006e808eb00e8894ba267a90f9e0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:32aec5d7a1152fad8604b74dfbfe544f8c346c42651791a768fd5f0025bc59b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53150431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55bcda861cae15b7310f14adc6b1f942f3d867ef30b6ff8da9268ac0ebd58a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 22 Sep 2020 18:32:31 GMT
ARG KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:31 GMT
ENV KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:37 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 22 Sep 2020 18:32:37 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 22 Sep 2020 18:32:37 GMT
USER kong
# Tue, 22 Sep 2020 18:32:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 22 Sep 2020 18:32:38 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 22 Sep 2020 18:32:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 22 Sep 2020 18:32:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306b16482a5463a3999b475a70c541b3eafcd2c4d3b6da8b5ae4d53bc49be14`  
		Last Modified: Tue, 22 Sep 2020 18:34:57 GMT  
		Size: 50.3 MB (50336253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff24278e47024f951b5e7834bbcb0a5ce4e0ea9086924d0a929eb960a35b3542`  
		Last Modified: Tue, 22 Sep 2020 18:34:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2ada4f5522df9afdcc8230d55d29842c321585b16258c46616a6d1e7ef8dc7a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d349242092b941662b5f7463ac4a33d865746d92ca9dfbf5ace92391d5cb0b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:51 GMT
ARG KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:57:53 GMT
ENV KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:58:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 17 Dec 2020 04:58:06 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:58:08 GMT
USER kong
# Thu, 17 Dec 2020 04:58:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:58:09 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:58:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:58:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8c4352649944a52a45f73f8267085e3e8f5f8c42cd7916f17e194af442ccdd`  
		Last Modified: Thu, 17 Dec 2020 04:59:39 GMT  
		Size: 49.9 MB (49938950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c2b84fa76be82f6d536a0c0a486863650800cfad97b972c7753461f8f4e3bc`  
		Last Modified: Thu, 17 Dec 2020 04:59:23 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-centos`

```console
$ docker pull kong@sha256:2074a8dbc332a2d158a41f480915d2cca721cd24449a36a956d673b992551da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:9abae830a109a6c87cf973fab99656a87fe37c1a53c195d79fa8b2448d85a75d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a08e453725f88199609cc19d52cc849a8b829755d8ea61b90d497a84e9c4b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ENV KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 14 Nov 2020 01:02:42 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 14 Nov 2020 01:02:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:02:43 GMT
USER kong
# Sat, 14 Nov 2020 01:02:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:02:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:02:43 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:02:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a690a7e5955b5f53b5859ac1391b51d1584818a0bbc504061e654b26d4d71f`  
		Last Modified: Sat, 14 Nov 2020 01:04:13 GMT  
		Size: 51.2 MB (51162000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4dd8889546b4ae415188145fb1dde0b9c303884420d3874d1673772dd91321`  
		Last Modified: Sat, 14 Nov 2020 01:04:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-ubuntu`

```console
$ docker pull kong@sha256:3cbcd2d2871e29afdad2e7839a6ea138ae16cdd82b325ba2b7b726255172e7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:52c7ae6e58317a6e45c17d8dce8b2bfb345edbaab31c6df8766bddb549ce8336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133765959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc1f4896ae569e6e57b663fa0da647e9928b82466d6ee11e7bceb4cadb6319f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ARG EE_PORTS
# Thu, 26 Nov 2020 01:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 26 Nov 2020 01:23:23 GMT
ARG KONG_VERSION=2.1.4
# Thu, 26 Nov 2020 01:23:23 GMT
ENV KONG_VERSION=2.1.4
# Thu, 26 Nov 2020 01:23:47 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 26 Nov 2020 01:23:48 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 26 Nov 2020 01:23:48 GMT
USER kong
# Thu, 26 Nov 2020 01:23:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Nov 2020 01:23:48 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 26 Nov 2020 01:23:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Nov 2020 01:23:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cf4456ff0f9681f8f28609985fc656156850b00b8345efddddb01f67e7d11`  
		Last Modified: Thu, 26 Nov 2020 01:24:55 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d701cb14b467c3deeb4bf40d80c385db3db4b6405048555a5e51b71d08dc1`  
		Last Modified: Thu, 26 Nov 2020 01:25:28 GMT  
		Size: 62.8 MB (62843489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233dfb6bcc3c62605c2778ff26bad8b7a5c67b9cbe61c695f7b550b9c4918782`  
		Last Modified: Thu, 26 Nov 2020 01:25:16 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cea3d52343c5817ef48fe86d8506860079d2fe09f080c79c8c76b0c5b35e8099
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125140620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97c5646bb862a7acb33f6358832cd42f80960ccfd2b39ff2004ae7175488b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ARG EE_PORTS
# Wed, 25 Nov 2020 23:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 25 Nov 2020 23:27:25 GMT
ARG KONG_VERSION=2.1.4
# Wed, 25 Nov 2020 23:27:25 GMT
ENV KONG_VERSION=2.1.4
# Wed, 25 Nov 2020 23:28:14 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 25 Nov 2020 23:28:17 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 25 Nov 2020 23:28:18 GMT
USER kong
# Wed, 25 Nov 2020 23:28:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Nov 2020 23:28:20 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 25 Nov 2020 23:28:20 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Nov 2020 23:28:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6cba0c8b4d5e1def090992b7d3bc001ae633fa3ad938efa00a15d89e40a72c`  
		Last Modified: Wed, 25 Nov 2020 23:29:55 GMT  
		Size: 25.1 MB (25081968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3a4efe36ab888c3f372905cb6757dd8b84ffd0ce5a6bcf62019fc83672032e`  
		Last Modified: Wed, 25 Nov 2020 23:30:38 GMT  
		Size: 59.2 MB (59230369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8be18280aa22e5454cd135b7e8c766283000ea67203fc0dc2c5bbcda44be23`  
		Last Modified: Wed, 25 Nov 2020 23:30:20 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:ea980a20d7d2a9166e9dac16bb6a1964d006e808eb00e8894ba267a90f9e0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:32aec5d7a1152fad8604b74dfbfe544f8c346c42651791a768fd5f0025bc59b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53150431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55bcda861cae15b7310f14adc6b1f942f3d867ef30b6ff8da9268ac0ebd58a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 22 Sep 2020 18:32:31 GMT
ARG KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:31 GMT
ENV KONG_VERSION=2.1.4
# Tue, 22 Sep 2020 18:32:37 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 22 Sep 2020 18:32:37 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 22 Sep 2020 18:32:37 GMT
USER kong
# Tue, 22 Sep 2020 18:32:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 22 Sep 2020 18:32:38 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 22 Sep 2020 18:32:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 22 Sep 2020 18:32:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306b16482a5463a3999b475a70c541b3eafcd2c4d3b6da8b5ae4d53bc49be14`  
		Last Modified: Tue, 22 Sep 2020 18:34:57 GMT  
		Size: 50.3 MB (50336253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff24278e47024f951b5e7834bbcb0a5ce4e0ea9086924d0a929eb960a35b3542`  
		Last Modified: Tue, 22 Sep 2020 18:34:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2ada4f5522df9afdcc8230d55d29842c321585b16258c46616a6d1e7ef8dc7a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d349242092b941662b5f7463ac4a33d865746d92ca9dfbf5ace92391d5cb0b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:51 GMT
ARG KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:57:53 GMT
ENV KONG_VERSION=2.1.4
# Thu, 17 Dec 2020 04:58:04 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 17 Dec 2020 04:58:06 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:58:08 GMT
USER kong
# Thu, 17 Dec 2020 04:58:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:58:09 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:58:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:58:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8c4352649944a52a45f73f8267085e3e8f5f8c42cd7916f17e194af442ccdd`  
		Last Modified: Thu, 17 Dec 2020 04:59:39 GMT  
		Size: 49.9 MB (49938950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c2b84fa76be82f6d536a0c0a486863650800cfad97b972c7753461f8f4e3bc`  
		Last Modified: Thu, 17 Dec 2020 04:59:23 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-centos`

```console
$ docker pull kong@sha256:2074a8dbc332a2d158a41f480915d2cca721cd24449a36a956d673b992551da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:9abae830a109a6c87cf973fab99656a87fe37c1a53c195d79fa8b2448d85a75d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a08e453725f88199609cc19d52cc849a8b829755d8ea61b90d497a84e9c4b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ENV KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 14 Nov 2020 01:02:42 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 14 Nov 2020 01:02:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:02:43 GMT
USER kong
# Sat, 14 Nov 2020 01:02:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:02:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:02:43 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:02:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a690a7e5955b5f53b5859ac1391b51d1584818a0bbc504061e654b26d4d71f`  
		Last Modified: Sat, 14 Nov 2020 01:04:13 GMT  
		Size: 51.2 MB (51162000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4dd8889546b4ae415188145fb1dde0b9c303884420d3874d1673772dd91321`  
		Last Modified: Sat, 14 Nov 2020 01:04:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-ubuntu`

```console
$ docker pull kong@sha256:3cbcd2d2871e29afdad2e7839a6ea138ae16cdd82b325ba2b7b726255172e7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:52c7ae6e58317a6e45c17d8dce8b2bfb345edbaab31c6df8766bddb549ce8336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133765959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc1f4896ae569e6e57b663fa0da647e9928b82466d6ee11e7bceb4cadb6319f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ARG EE_PORTS
# Thu, 26 Nov 2020 01:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 26 Nov 2020 01:23:23 GMT
ARG KONG_VERSION=2.1.4
# Thu, 26 Nov 2020 01:23:23 GMT
ENV KONG_VERSION=2.1.4
# Thu, 26 Nov 2020 01:23:47 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 26 Nov 2020 01:23:48 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 26 Nov 2020 01:23:48 GMT
USER kong
# Thu, 26 Nov 2020 01:23:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 26 Nov 2020 01:23:48 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 26 Nov 2020 01:23:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Nov 2020 01:23:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cf4456ff0f9681f8f28609985fc656156850b00b8345efddddb01f67e7d11`  
		Last Modified: Thu, 26 Nov 2020 01:24:55 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d701cb14b467c3deeb4bf40d80c385db3db4b6405048555a5e51b71d08dc1`  
		Last Modified: Thu, 26 Nov 2020 01:25:28 GMT  
		Size: 62.8 MB (62843489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233dfb6bcc3c62605c2778ff26bad8b7a5c67b9cbe61c695f7b550b9c4918782`  
		Last Modified: Thu, 26 Nov 2020 01:25:16 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cea3d52343c5817ef48fe86d8506860079d2fe09f080c79c8c76b0c5b35e8099
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125140620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97c5646bb862a7acb33f6358832cd42f80960ccfd2b39ff2004ae7175488b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ARG EE_PORTS
# Wed, 25 Nov 2020 23:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 25 Nov 2020 23:27:25 GMT
ARG KONG_VERSION=2.1.4
# Wed, 25 Nov 2020 23:27:25 GMT
ENV KONG_VERSION=2.1.4
# Wed, 25 Nov 2020 23:28:14 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 25 Nov 2020 23:28:17 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 25 Nov 2020 23:28:18 GMT
USER kong
# Wed, 25 Nov 2020 23:28:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Nov 2020 23:28:20 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 25 Nov 2020 23:28:20 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Nov 2020 23:28:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6cba0c8b4d5e1def090992b7d3bc001ae633fa3ad938efa00a15d89e40a72c`  
		Last Modified: Wed, 25 Nov 2020 23:29:55 GMT  
		Size: 25.1 MB (25081968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3a4efe36ab888c3f372905cb6757dd8b84ffd0ce5a6bcf62019fc83672032e`  
		Last Modified: Wed, 25 Nov 2020 23:30:38 GMT  
		Size: 59.2 MB (59230369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8be18280aa22e5454cd135b7e8c766283000ea67203fc0dc2c5bbcda44be23`  
		Last Modified: Wed, 25 Nov 2020 23:30:20 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.0`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.0` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.1-alpine`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.1-centos`

```console
$ docker pull kong@sha256:ad8632341f4a81d75058c45dff279fa8938f20b2a18d7eae41b843fb2d94f4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a710cd063951cfe5e89bca7b1f64e68ad1b5ea33f7268fb9ba13c530dcb9307
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127352007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a665d19b27df8e7b9b66445eeae0c72957bde11c041ee73094b778406c6d86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
# Wed, 02 Dec 2020 01:06:25 GMT
# ARGS: KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 02 Dec 2020 01:06:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:06:25 GMT
USER kong
# Wed, 02 Dec 2020 01:06:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:06:26 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:06:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:06:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef344440583f6238cd4ca52ab5606f1580aa083301cde2fc96a8a774b86132`  
		Last Modified: Wed, 02 Dec 2020 01:07:59 GMT  
		Size: 51.3 MB (51253987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4f52bbd47f126044058af2b82176e13c002b85536baa59a34e64c9b3f78e70`  
		Last Modified: Wed, 02 Dec 2020 01:07:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.1-ubuntu`

```console
$ docker pull kong@sha256:06a9597afd556d8c3528f1896f4c7089594773cff9bd162be1f957ed71d6eeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9b75bab8c4f35cbfc11ac61700c6cce230dd4cc10fcc70d6f4589671abfe30a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133836339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70caff3fdf6dd6a544ed6d0713696b69ac0d0913450ac32e69d2f5c4c2f44a93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ARG EE_PORTS
# Thu, 26 Nov 2020 01:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 02 Dec 2020 01:04:48 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:49 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:38 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 02 Dec 2020 01:05:38 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:05:39 GMT
USER kong
# Wed, 02 Dec 2020 01:05:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:05:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:05:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:05:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cf4456ff0f9681f8f28609985fc656156850b00b8345efddddb01f67e7d11`  
		Last Modified: Thu, 26 Nov 2020 01:24:55 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39015f67929c8d300a91c5f148063b9640af69f04e3a074c72a1a9c7066260`  
		Last Modified: Wed, 02 Dec 2020 01:07:42 GMT  
		Size: 62.9 MB (62913868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a4ac5176a48f525ea28a2263bb4b0bec8c42168184883a16174dbef91a777d`  
		Last Modified: Wed, 02 Dec 2020 01:07:29 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b6dd2d561ce47b1ca4c372f08153135d71448fd2d711081fecc591d977e49781
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125250778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985df27d1e31d9a94f3a9ab12699af299b05fb641e37396e3b682a054af870cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ARG EE_PORTS
# Wed, 25 Nov 2020 23:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 02 Dec 2020 00:04:36 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:04:37 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:05:29 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 02 Dec 2020 00:05:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 00:05:32 GMT
USER kong
# Wed, 02 Dec 2020 00:05:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 00:05:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 00:05:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 00:05:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6cba0c8b4d5e1def090992b7d3bc001ae633fa3ad938efa00a15d89e40a72c`  
		Last Modified: Wed, 25 Nov 2020 23:29:55 GMT  
		Size: 25.1 MB (25081968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda52cea25b914c9303de1002280efc9e81bf9d815b2e868a4c9d7f5d51a79a7`  
		Last Modified: Wed, 02 Dec 2020 00:06:55 GMT  
		Size: 59.3 MB (59340527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c60d97d9af49fa932cf2bd9e190261584edcc92ad062981a5d87adda5a44313`  
		Last Modified: Wed, 02 Dec 2020 00:06:38 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-alpine`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-centos`

```console
$ docker pull kong@sha256:ad8632341f4a81d75058c45dff279fa8938f20b2a18d7eae41b843fb2d94f4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a710cd063951cfe5e89bca7b1f64e68ad1b5ea33f7268fb9ba13c530dcb9307
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127352007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a665d19b27df8e7b9b66445eeae0c72957bde11c041ee73094b778406c6d86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
# Wed, 02 Dec 2020 01:06:25 GMT
# ARGS: KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 02 Dec 2020 01:06:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:06:25 GMT
USER kong
# Wed, 02 Dec 2020 01:06:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:06:26 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:06:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:06:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef344440583f6238cd4ca52ab5606f1580aa083301cde2fc96a8a774b86132`  
		Last Modified: Wed, 02 Dec 2020 01:07:59 GMT  
		Size: 51.3 MB (51253987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4f52bbd47f126044058af2b82176e13c002b85536baa59a34e64c9b3f78e70`  
		Last Modified: Wed, 02 Dec 2020 01:07:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-ubuntu`

```console
$ docker pull kong@sha256:06a9597afd556d8c3528f1896f4c7089594773cff9bd162be1f957ed71d6eeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9b75bab8c4f35cbfc11ac61700c6cce230dd4cc10fcc70d6f4589671abfe30a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133836339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70caff3fdf6dd6a544ed6d0713696b69ac0d0913450ac32e69d2f5c4c2f44a93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ARG EE_PORTS
# Thu, 26 Nov 2020 01:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 02 Dec 2020 01:04:48 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:49 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:38 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 02 Dec 2020 01:05:38 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:05:39 GMT
USER kong
# Wed, 02 Dec 2020 01:05:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:05:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:05:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:05:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cf4456ff0f9681f8f28609985fc656156850b00b8345efddddb01f67e7d11`  
		Last Modified: Thu, 26 Nov 2020 01:24:55 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39015f67929c8d300a91c5f148063b9640af69f04e3a074c72a1a9c7066260`  
		Last Modified: Wed, 02 Dec 2020 01:07:42 GMT  
		Size: 62.9 MB (62913868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a4ac5176a48f525ea28a2263bb4b0bec8c42168184883a16174dbef91a777d`  
		Last Modified: Wed, 02 Dec 2020 01:07:29 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b6dd2d561ce47b1ca4c372f08153135d71448fd2d711081fecc591d977e49781
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125250778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985df27d1e31d9a94f3a9ab12699af299b05fb641e37396e3b682a054af870cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ARG EE_PORTS
# Wed, 25 Nov 2020 23:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 02 Dec 2020 00:04:36 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:04:37 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:05:29 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 02 Dec 2020 00:05:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 00:05:32 GMT
USER kong
# Wed, 02 Dec 2020 00:05:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 00:05:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 00:05:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 00:05:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6cba0c8b4d5e1def090992b7d3bc001ae633fa3ad938efa00a15d89e40a72c`  
		Last Modified: Wed, 25 Nov 2020 23:29:55 GMT  
		Size: 25.1 MB (25081968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda52cea25b914c9303de1002280efc9e81bf9d815b2e868a4c9d7f5d51a79a7`  
		Last Modified: Wed, 02 Dec 2020 00:06:55 GMT  
		Size: 59.3 MB (59340527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c60d97d9af49fa932cf2bd9e190261584edcc92ad062981a5d87adda5a44313`  
		Last Modified: Wed, 02 Dec 2020 00:06:38 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:ad8632341f4a81d75058c45dff279fa8938f20b2a18d7eae41b843fb2d94f4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:6a710cd063951cfe5e89bca7b1f64e68ad1b5ea33f7268fb9ba13c530dcb9307
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127352007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a665d19b27df8e7b9b66445eeae0c72957bde11c041ee73094b778406c6d86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
# Wed, 02 Dec 2020 01:06:25 GMT
# ARGS: KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 02 Dec 2020 01:06:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:06:25 GMT
USER kong
# Wed, 02 Dec 2020 01:06:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:06:26 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:06:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:06:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef344440583f6238cd4ca52ab5606f1580aa083301cde2fc96a8a774b86132`  
		Last Modified: Wed, 02 Dec 2020 01:07:59 GMT  
		Size: 51.3 MB (51253987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4f52bbd47f126044058af2b82176e13c002b85536baa59a34e64c9b3f78e70`  
		Last Modified: Wed, 02 Dec 2020 01:07:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:fccb7c0a911f01a00b30c52ca1d1ad2d5acf0d26ac1a6379fc93a5448ae593c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:48f313b67cb04ba8ebcac96f07486ebeba4f3de4dfc9350db8e644cebeca014c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53270746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533327370bc6df80191fc98db62e5ac62d7db39c3805f77d572a78345abd0515`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2020 00:19:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 00:19:56 GMT
ARG ASSET=ce
# Tue, 05 May 2020 00:19:56 GMT
ENV ASSET=ce
# Mon, 13 Jul 2020 17:19:53 GMT
ARG EE_PORTS
# Mon, 13 Jul 2020 17:19:53 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 01:04:34 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:34 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:04:42 GMT
USER kong
# Wed, 02 Dec 2020 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:04:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e0de2dc0e7e86d092bbee85a6c1ef2769273bd1a78d87bc9a745745fe2d3b9`  
		Last Modified: Mon, 13 Jul 2020 17:21:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9236dce56335571945a751b4a619530e0610ee319ae425b59d87c9482ffe403b`  
		Last Modified: Wed, 02 Dec 2020 01:07:20 GMT  
		Size: 50.5 MB (50456567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f4a526b3977bb685b5eeab222fd3e08bacd27bd23c5fccb2db196444f65344`  
		Last Modified: Wed, 02 Dec 2020 01:07:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d1c2daab221d9e5054c5cd6a7df3e855c056bd8a79cf679833fe069f74ebceaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52801740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0813154a7843d44b47a393a769eedcf892d4c234e21226c7e3b03e9d496d652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:57:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Thu, 17 Dec 2020 04:57:06 GMT
ARG ASSET=ce
# Thu, 17 Dec 2020 04:57:07 GMT
ENV ASSET=ce
# Thu, 17 Dec 2020 04:57:08 GMT
ARG EE_PORTS
# Thu, 17 Dec 2020 04:57:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Thu, 17 Dec 2020 04:57:11 GMT
ARG KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:12 GMT
ENV KONG_VERSION=2.2.1
# Thu, 17 Dec 2020 04:57:30 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Thu, 17 Dec 2020 04:57:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 17 Dec 2020 04:57:35 GMT
USER kong
# Thu, 17 Dec 2020 04:57:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Dec 2020 04:57:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 17 Dec 2020 04:57:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Dec 2020 04:57:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3181cc464c4af55ff9dd73d4603f67578cdc16237deb0e5e467594b40164ab6`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73439c4e6c349f3f7edf0a15636c8b402f48bc351c48dfd010aa03c8a980a0ff`  
		Last Modified: Thu, 17 Dec 2020 04:59:05 GMT  
		Size: 50.1 MB (50075659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ae76d2ad481a47953973f988b2abfb80a24ff497eb267680d4a0b68f2da543`  
		Last Modified: Thu, 17 Dec 2020 04:58:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:06a9597afd556d8c3528f1896f4c7089594773cff9bd162be1f957ed71d6eeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9b75bab8c4f35cbfc11ac61700c6cce230dd4cc10fcc70d6f4589671abfe30a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133836339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70caff3fdf6dd6a544ed6d0713696b69ac0d0913450ac32e69d2f5c4c2f44a93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:22:41 GMT
ARG ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ENV ASSET=ce
# Thu, 26 Nov 2020 01:22:42 GMT
ARG EE_PORTS
# Thu, 26 Nov 2020 01:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 02 Dec 2020 01:04:48 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:04:49 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:38 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 02 Dec 2020 01:05:38 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:05:39 GMT
USER kong
# Wed, 02 Dec 2020 01:05:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:05:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:05:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:05:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cf4456ff0f9681f8f28609985fc656156850b00b8345efddddb01f67e7d11`  
		Last Modified: Thu, 26 Nov 2020 01:24:55 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39015f67929c8d300a91c5f148063b9640af69f04e3a074c72a1a9c7066260`  
		Last Modified: Wed, 02 Dec 2020 01:07:42 GMT  
		Size: 62.9 MB (62913868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a4ac5176a48f525ea28a2263bb4b0bec8c42168184883a16174dbef91a777d`  
		Last Modified: Wed, 02 Dec 2020 01:07:29 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b6dd2d561ce47b1ca4c372f08153135d71448fd2d711081fecc591d977e49781
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125250778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985df27d1e31d9a94f3a9ab12699af299b05fb641e37396e3b682a054af870cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:26:02 GMT
ARG ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ENV ASSET=ce
# Wed, 25 Nov 2020 23:26:04 GMT
ARG EE_PORTS
# Wed, 25 Nov 2020 23:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 02 Dec 2020 00:04:36 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:04:37 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:05:29 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 02 Dec 2020 00:05:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 00:05:32 GMT
USER kong
# Wed, 02 Dec 2020 00:05:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 00:05:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 00:05:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 00:05:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6cba0c8b4d5e1def090992b7d3bc001ae633fa3ad938efa00a15d89e40a72c`  
		Last Modified: Wed, 25 Nov 2020 23:29:55 GMT  
		Size: 25.1 MB (25081968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda52cea25b914c9303de1002280efc9e81bf9d815b2e868a4c9d7f5d51a79a7`  
		Last Modified: Wed, 02 Dec 2020 00:06:55 GMT  
		Size: 59.3 MB (59340527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c60d97d9af49fa932cf2bd9e190261584edcc92ad062981a5d87adda5a44313`  
		Last Modified: Wed, 02 Dec 2020 00:06:38 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
