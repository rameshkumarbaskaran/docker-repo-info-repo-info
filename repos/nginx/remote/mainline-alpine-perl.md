## `nginx:mainline-alpine-perl`

```console
$ docker pull nginx@sha256:03cf072cabe2c49f9825ab2fcc44c37b5101258bea4e5a45e66a7f4a8586c08d
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

### `nginx:mainline-alpine-perl` - linux; amd64

```console
$ docker pull nginx@sha256:d0bd71add7ded78d1fb6cd6508d67b49f9c40084afaf5030904a86cb531fd2b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18061957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c068c0f15a748a4c63072e634f4fe81cfa4f43db364e860cb84e6e56a01154`
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
# Tue, 02 Jun 2020 00:36:36 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:36:37 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:23:54 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:23:54 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:23:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:23:54 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:23:54 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:23:55 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bdc183716b658af645c2e96d9400fa90f43d48fe57d67c41b6c23d72417470`  
		Last Modified: Tue, 02 Jun 2020 00:37:42 GMT  
		Size: 15.2 MB (15246533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23c33e8ca3f4e3aaef37cdbd1fc9d5e72e1e45c52c4367951cd48aa190cd24`  
		Last Modified: Tue, 02 Jun 2020 00:37:38 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef689db1431fd997f2e69ce7b2141b6eebd8c5157141d5cc2071e9a9619fc04`  
		Last Modified: Tue, 02 Jun 2020 16:24:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8018058877f79b1eaeb2736b759a3edf1c0a78eb571a6da2c8d3232e05d6270`  
		Last Modified: Tue, 02 Jun 2020 16:24:43 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-alpine-perl` - linux; arm variant v6

```console
$ docker pull nginx@sha256:1446e2f56f08d4705343512dc8ddbc951795196685c1bdc9be66a2fc518b61ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16718719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a160df94f20558718344cea841f464ba3dec495e8fba613c26798506d91a31`
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
# Tue, 02 Jun 2020 00:58:55 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:58:57 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:52:16 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:52:16 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:52:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:52:19 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:52:20 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:52:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d312f6366c7820976b4543c4818176dd4198cef321c949d5cafa20979cc959`  
		Last Modified: Tue, 02 Jun 2020 01:00:06 GMT  
		Size: 14.1 MB (14096677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f54c7f57f3b6df7c02fb0bcdb975bb384de955f384127729b230b188d5e696`  
		Last Modified: Tue, 02 Jun 2020 01:00:00 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9635258b0ded4acb77c407ce1766f5de769c67842d8dc89338e592ce771ed083`  
		Last Modified: Tue, 02 Jun 2020 16:52:53 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022da3d464f039362206c70068821bc35ac620e995df66c7a61087e144e97730`  
		Last Modified: Tue, 02 Jun 2020 16:52:52 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-alpine-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:27ff3ba27c155e4162b1a3a232b734908b76c2e6e85744927f7ffed3544c2edc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15889572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed0911cdd640a9de305733e6d4ed5a8923c4928705d06d4ae4811ca70952607`
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
# Tue, 02 Jun 2020 04:28:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 04:28:23 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:02:53 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:02:54 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:02:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:02:55 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:02:56 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:02:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d96199df2d95eb0a35eebc0eecaa19e977d37d786ce66e688686093787a9a11`  
		Last Modified: Tue, 02 Jun 2020 04:31:40 GMT  
		Size: 13.5 MB (13465405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0174d38389fb115b0fe7f860caf419044e520f1b054688e2bad7f0b2d34ea41`  
		Last Modified: Tue, 02 Jun 2020 04:31:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975e76c4299cda5ad3d048702613a3b00e720e850fb75ee6fc10c01580effdd0`  
		Last Modified: Tue, 02 Jun 2020 16:03:55 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e946101cefcd6cf8f10432a002f5d1c9a509431ca6da78eeca0855fc18dfa`  
		Last Modified: Tue, 02 Jun 2020 16:03:55 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-alpine-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:51dff17beef1782f9280c4ecdaf5e427dd6f7d803b22db44eb0558ac4497ffa9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17919551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e550996913072eb02b25329805af4cc8d796b5a85f1d711ebf7fe09b0b949059`
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
# Tue, 02 Jun 2020 01:05:36 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 01:05:37 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:44:44 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:45 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:44:46 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:44:46 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:44:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c864edca6f73065e812bd722e7765c99baabd5df21f07d35b97c311962d9db0`  
		Last Modified: Tue, 02 Jun 2020 01:07:29 GMT  
		Size: 15.2 MB (15193020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d27389439d204a51d5e2aa288ef6caf3fe4731e72fdbd1ec77b8d44767617e`  
		Last Modified: Tue, 02 Jun 2020 01:07:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7f6267e972c3a76da10db022dd0db8f6e971a9addea8f33a6d5274378561ce`  
		Last Modified: Tue, 02 Jun 2020 16:46:13 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b55819f0a414e222b05266a84271e9a666b5e69525b52d6add0ffa639e56d35`  
		Last Modified: Tue, 02 Jun 2020 16:46:12 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-alpine-perl` - linux; 386

```console
$ docker pull nginx@sha256:99a055e7ed52b05c7e9accdcbcad7e9c2130b16d25ff7423de23825a5ea6f62a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17807180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2433bc0ab7d8257ad236f25a804812e565c4dda8eaa84d821f4cdf6517fd5c`
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
# Tue, 02 Jun 2020 00:45:59 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:45:59 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:42:17 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:42:17 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:42:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:42:18 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:42:18 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:42:18 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4262c1641d5460d391dc922c7f473f92303998abb5618bba2a1d4cff89c8ec`  
		Last Modified: Tue, 02 Jun 2020 00:47:15 GMT  
		Size: 15.0 MB (14996658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4b784d42df9e0a1f51b61dd058e953abf95841c4657f56eed1d5888843d674`  
		Last Modified: Tue, 02 Jun 2020 00:47:10 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e94bfef85067c0baec31ab77e49c3aed0c474b4ea561dbbb9d77e96ef05fd8`  
		Last Modified: Tue, 02 Jun 2020 16:43:22 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f5c66780f7e8654f9869ff2cb190785e64143313df08e5a067acc06c92cbef`  
		Last Modified: Tue, 02 Jun 2020 16:43:22 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-alpine-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:5a4d46f6b197005b165d486055455d951e5dec0961bc41e587c0285e4c3be8ff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18455571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d906a91725cbd1effa0bd1c6fae4b88d9f387099d1f9b83d9d22f4eebce3d8c`
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
# Tue, 02 Jun 2020 00:59:03 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:59:10 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:26:57 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:26:59 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:27:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:27:07 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:27:10 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:27:15 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d2633744b029635955c26ad54e69bda87e14032ca3250e72999a63af8e67ea`  
		Last Modified: Tue, 02 Jun 2020 01:01:48 GMT  
		Size: 15.6 MB (15631617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec457ee217172150b92b3fbf606246077e30e811e9af635967cb7bebe437c2d`  
		Last Modified: Tue, 02 Jun 2020 01:01:43 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dd7d6d709ca464e36b6203e8c2cfe366d550c5899580ee5f9782977ac8c42b`  
		Last Modified: Tue, 02 Jun 2020 16:29:17 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce9963b7b00735b7dd31185da39ab177bf0881377b097ae30183e1fc220c82`  
		Last Modified: Tue, 02 Jun 2020 16:29:17 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-alpine-perl` - linux; s390x

```console
$ docker pull nginx@sha256:0f24ac753065246bce9348cfd69ae3e30a6085e93354b53867315e0f80d7eaba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18350038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d022a24e355c60436332bc6fbd389d9655a82ca34522ee3f3cd8a018fd440d7`
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
# Tue, 02 Jun 2020 00:51:02 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && case "$apkArch" in         x86_64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && apk add --no-cache --virtual .cert-deps                 openssl             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk del .cert-deps             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 mercurial                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && hg clone https://hg.nginx.org/pkg-oss                 && cd pkg-oss                 && hg up ${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:51:03 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:44:35 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:35 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:44:36 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:44:36 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:44:36 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539e2ea9d932eefa7e558a22258277ad282312f9fc5c167221bc3f50128e45bf`  
		Last Modified: Tue, 02 Jun 2020 00:52:18 GMT  
		Size: 15.8 MB (15765074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e2e96aeb3713e02377a8de842da6384ca8d861e1fddf78d6e3aee27722570`  
		Last Modified: Tue, 02 Jun 2020 00:52:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b13402682435fbf85580fbb829a20bb3afd4de23cb6fb0d87580c6284e466`  
		Last Modified: Tue, 02 Jun 2020 16:45:33 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3aba223057013cf8d3fa6b91bc2ec8f8e9a050599b8426a8d26c485ac2fba0`  
		Last Modified: Tue, 02 Jun 2020 16:45:32 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
