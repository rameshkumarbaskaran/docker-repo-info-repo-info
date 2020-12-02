## `kong:alpine`

```console
$ docker pull kong@sha256:8784987692b927a06d5dffc9e1aa95aede554f47f890028cf7b167734efdf0e2
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
$ docker pull kong@sha256:9c55f11620a0a1ed6f2fdf0a0c8677bfd3161bbaf8485425060c69bc4fa71815
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52798827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d823792d1254d38dc0ff387d533389f21a913c5c7b32fbb4056a8888fa2817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Tue, 22 Sep 2020 19:05:32 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 22 Sep 2020 19:05:34 GMT
ARG ASSET=ce
# Tue, 22 Sep 2020 19:05:35 GMT
ENV ASSET=ce
# Tue, 22 Sep 2020 19:05:36 GMT
ARG EE_PORTS
# Tue, 22 Sep 2020 19:05:36 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 02 Dec 2020 00:04:04 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:04:05 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 00:04:18 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 02 Dec 2020 00:04:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 00:04:21 GMT
USER kong
# Wed, 02 Dec 2020 00:04:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 00:04:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 00:04:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 00:04:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f1f361b75deeea5140a58989e54db49d72c8f2794625392d9b60e5f6adea53`  
		Last Modified: Tue, 22 Sep 2020 19:08:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab335b576deedcb85860c51be3d400f942b169096520421ac7a56179faeeec5`  
		Last Modified: Wed, 02 Dec 2020 00:06:25 GMT  
		Size: 50.1 MB (50073536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b71048fe80aa69ed919469664151691ff0dc3b98bf1dd2ba38d602d4cf270a8`  
		Last Modified: Wed, 02 Dec 2020 00:06:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
