## `nginx:1-alpine`

```console
$ docker pull nginx@sha256:b89a6ccbda39576ad23fd079978c967cecc6b170db6e7ff8a769bf2259a71912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `nginx:1-alpine` - linux; amd64

```console
$ docker pull nginx@sha256:ee5a9b68e8d4a4b8b48318ff08ad5489bd1ce52b357bf48c511968a302bc347b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9276391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0cdcc60a96a5124763fddf5d534d058ad7d0d8d4c3b8be2aefedf4267d0270`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:58:32 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:36:21 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:36:21 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:36:21 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 00:36:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:36:26 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:23:49 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:23:49 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:23:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:23:49 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:23:50 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:23:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c113fb0c778963cb3069e94e8148a3770122f6763c94373e22f5342b503ab0`  
		Last Modified: Tue, 02 Jun 2020 00:37:32 GMT  
		Size: 6.5 MB (6460970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba64393807bf2549af97a1a074ca5fff1bce25ad115b0a7ced446cd1b4305d0`  
		Last Modified: Tue, 02 Jun 2020 00:37:31 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262f9908119d4529a370bcdf1f1306131ad556edf400413d5fa74008d7919931`  
		Last Modified: Tue, 02 Jun 2020 16:24:36 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a057508f96954546441044f0d2373303862a4d4accc163e68a4c30d0c88869`  
		Last Modified: Tue, 02 Jun 2020 16:24:36 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:88fd834bc089b5dff1f27ab0315c3b0bbdfddfca3b2c1aeb9798944d179e441b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8690722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a003e751c73e0d00cb07b7918866000a22de92ca4ff72a7b3448b48a3883e850`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 18:28:29 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:49:37 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:49:38 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:49:39 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 00:54:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:54:36 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:52:03 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:52:04 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:52:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:52:06 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:52:08 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:52:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cc2adfab5fa06add87f7cbd62b1b592408d14f5f37688ddfee4e30088b90dc`  
		Last Modified: Tue, 02 Jun 2020 00:59:47 GMT  
		Size: 6.1 MB (6068678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b53781734493fbae128b3cfca47a7eaa565cb3d7891d896b95309377b6b335`  
		Last Modified: Tue, 02 Jun 2020 00:59:45 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0243ea7d4bfb9f924f41ffa26ca69c4d71b7367cf1b565352b4edfa96354b539`  
		Last Modified: Tue, 02 Jun 2020 16:52:45 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae80919ab713e86d44691047681da860e9fc5b4b6f938ddb867103dc7b87216`  
		Last Modified: Tue, 02 Jun 2020 16:52:44 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:bf8ebb8068d7ff10711c1670398eeaa83283a7987cdc9b9b014560dbba71773c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7997272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d363c5f93f65d1273bdf2621bd550055830d5de0c38fb0f8971797ca05cb89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 04:18:50 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 04:19:02 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 04:19:15 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 04:19:26 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 04:23:19 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 04:23:27 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:02:44 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:02:45 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:02:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:02:46 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:02:47 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:02:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa95196f78f3b6f53c7266338c74bf457f384eebf1c66b0d1fc44a9e5d9d7926`  
		Last Modified: Tue, 02 Jun 2020 04:31:22 GMT  
		Size: 5.6 MB (5573100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fedb7caa51cd45805002475d8a46a1f2319a3372e11c9e3e2d796d6742e21c`  
		Last Modified: Tue, 02 Jun 2020 04:31:21 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e03dd18048d1d48d6d13271bbd21d3f34ff67234eb70f4e65c3ab361baee089`  
		Last Modified: Tue, 02 Jun 2020 16:03:45 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5c0dbb40b6f1dd83b9b9bf077acf93493fb0ea797cf994383b114720950c31`  
		Last Modified: Tue, 02 Jun 2020 16:03:46 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:fa24815c8e52981d8ef01249e17d46dc5367765814d6feed154f1043aa255b8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9137141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d918ec5de8628dc8c8dc8f3928b6ce6cc8de5ddc2634ce1d907ab823601f16a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 04:01:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:56:37 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:56:38 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:56:40 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 01:00:23 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 01:00:24 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:44:35 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:36 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:44:37 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:44:37 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:44:38 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bba6258c7cb74683a9643cdeeef25544393d0962f2366b4163d690f37012d8`  
		Last Modified: Tue, 02 Jun 2020 01:07:15 GMT  
		Size: 6.4 MB (6410608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87b7e08b42c4db8341ff87e80300d58fbf4564279c6967cc52be8a341c003ef`  
		Last Modified: Tue, 02 Jun 2020 01:07:15 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e962a39d104db9e06d9001a84f98148975b2ab11fc000eb30809a663a904d9`  
		Last Modified: Tue, 02 Jun 2020 16:46:00 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf598435b4658b77ce78c595c1be5fba08aecbe3c082f4ca24cc360b80b2424f`  
		Last Modified: Tue, 02 Jun 2020 16:46:00 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-alpine` - linux; 386

```console
$ docker pull nginx@sha256:2fa12030ffb0224e0b2e17bc4b1f1479e191e2fd65869fc60d09a8efa5b6d879
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9645743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c4d6fd12f7f958523fbfa10b20656d7819d4e8a96d370c1bd7e72000e861d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 03:42:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:39:40 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:39:40 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:39:41 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 00:42:42 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:42:42 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:42:12 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:42:13 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:42:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:42:13 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:42:13 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:42:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8c7ecca96e5e2222239bcc1443ea051ce048a0e4239f83ff2cceb6e63bdfd4`  
		Last Modified: Tue, 02 Jun 2020 00:47:05 GMT  
		Size: 6.8 MB (6835220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044883f89af1e259adb7493c22cc165e227b27eef15ac21e0b913b842fd00de6`  
		Last Modified: Tue, 02 Jun 2020 00:47:03 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6969c887fe4c88e64860878b8aa3941968539e0ed5f2bb6eebaaa6194226add1`  
		Last Modified: Tue, 02 Jun 2020 16:43:14 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec31cfe0bbef0a40a6f880bd5f54f7f63db69c129183eb1d8a2f808ecf68302`  
		Last Modified: Tue, 02 Jun 2020 16:43:14 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:9012a1962d3201492ea815d0b395af623cf78e4b2187f9069d5cee0c0d1345c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9560586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24927b9f51bf99929297f155363ec45161c20f88418881a4955b851f9ad89226`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 01:30:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:52:07 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:52:10 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:52:12 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 00:55:19 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:55:22 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:26:18 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:26:21 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:26:30 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:26:36 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:26:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db39f8e56558c4712d13c321776e003e2726307852488a81a01c6e5320d645f4`  
		Last Modified: Tue, 02 Jun 2020 01:01:28 GMT  
		Size: 6.7 MB (6736633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4078b962ada0fd7bb1183743844e253f79200e91dfa6a7d5e71b3c5196644ab5`  
		Last Modified: Tue, 02 Jun 2020 01:01:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daad665c458d907c9ab836d4c9fb9455354983ba2d2f1b29a88a4e90063b3abc`  
		Last Modified: Tue, 02 Jun 2020 16:28:58 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb240f76617bc718149b047cbef930cf8e709b8a0afdefe046d1f2aff3383ce`  
		Last Modified: Tue, 02 Jun 2020 16:28:58 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:1-alpine` - linux; s390x

```console
$ docker pull nginx@sha256:d7b9368659ff1be2bbb4267c9d45e7aa201cb282ac9bc86e09bf390087df68b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9136921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffd7a5ec3633d197e96f14eb590c1f6898c0c43bc2075d13a192920627dea61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:15:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:47:49 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:47:49 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:47:49 GMT
ENV PKG_RELEASE=1
# Tue, 02 Jun 2020 00:49:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:49:16 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:44:30 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:30 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:44:31 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:44:31 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:44:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c99153a51cb3d9517eb749feb0b06d5a79be231658ad9a82c6997063b9d4c36`  
		Last Modified: Tue, 02 Jun 2020 00:52:02 GMT  
		Size: 6.6 MB (6551957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c8f1b8d529334f50db4fb33945f81aab4c1cb22b972ab4e89721e31f930afe`  
		Last Modified: Tue, 02 Jun 2020 00:52:01 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee9eaef3803d0c9061007cdd5867ac44964e1b96282126ece4ed345ad80e521`  
		Last Modified: Tue, 02 Jun 2020 16:45:25 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72bcf9c5e38e669719957e65499c2e174a948c3fa22fae4236da6c384cca5a9`  
		Last Modified: Tue, 02 Jun 2020 16:45:25 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
