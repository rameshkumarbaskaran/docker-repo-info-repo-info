## `nginx:latest`

```console
$ docker pull nginx@sha256:883874c218a6c71640579ae54e6952398757ec65702f4c8ba7675655156fcca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `nginx:latest` - linux; amd64

```console
$ docker pull nginx@sha256:d9002da0297bcd0909b394c26bd0fc9d8c466caf2b7396f58948cac5318d0d0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53311441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4392e5dad77dbaf6a573650b0fe1e282b57c5fba6e6cea00a27c7d4b68539b81`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:15:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:35:23 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:35:23 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:35:23 GMT
ENV PKG_RELEASE=1~buster
# Tue, 02 Jun 2020 00:35:44 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:35:44 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:23:39 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:23:39 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:23:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:23:40 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:23:40 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:23:40 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3ac8106a0bbe43a6e55d2b719fc00a2f8f694e90c7903403e8fdecd2ccc57f`  
		Last Modified: Tue, 02 Jun 2020 00:37:12 GMT  
		Size: 26.2 MB (26210578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de28bdda69b66a8e07b14f03a9762f508bc4caac35cef9543bad53503ce5f53`  
		Last Modified: Tue, 02 Jun 2020 00:37:05 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c431ac2669038db7a758a597c7d1d53cdfb2dd9bf6de2ad3418973569b3fc7`  
		Last Modified: Tue, 02 Jun 2020 16:24:23 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e070d03fd1b5a05aafc7c16830d80b4ed622d546061fabac8163d3082098a849`  
		Last Modified: Tue, 02 Jun 2020 16:24:23 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:latest` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ccdbf0106919b197f0b341ddd481d7e447ad951001b9415670e3ae725b145b70
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47017994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d99b820cf98e142d67c91937ca6b39e66662839ce229173a103156cff03365d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 11:03:38 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 03:59:43 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 03:59:52 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 04:00:01 GMT
ENV PKG_RELEASE=1~buster
# Tue, 02 Jun 2020 04:08:16 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 04:08:22 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:02:25 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:02:25 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:02:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:02:26 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:02:27 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:02:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde9f0dae75d28c6ea549566e2f265e14ce142c736c613c44ef41b3684be39ca`  
		Last Modified: Tue, 02 Jun 2020 04:30:20 GMT  
		Size: 24.3 MB (24309960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5b112ea599d775d7bf823dc7e952e9726211ae25c59c3b2d95b4dbeb5ae352`  
		Last Modified: Tue, 02 Jun 2020 04:30:11 GMT  
		Size: 539.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62923fe5ddbd6e3974716a04b4b16922952952fcefb77d61e84722e86ca73482`  
		Last Modified: Tue, 02 Jun 2020 16:03:27 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ba6ca404457057ab9b7e8bc05c44617aa2ef077779fa150931a0a2f8e82a7a`  
		Last Modified: Tue, 02 Jun 2020 16:03:26 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:latest` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:c6f330e394292c1cfa51c522915163cc421f304b4fd3c72344e88158404ad5a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52052142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264a6a602e1a60a43d324c8a62baa42fbab5be9915f9237d80849f388def21aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 22:21:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:39:56 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:39:57 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:39:57 GMT
ENV PKG_RELEASE=1~buster
# Tue, 02 Jun 2020 00:47:30 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:47:32 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:44:17 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:17 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:44:18 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:44:19 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:44:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ed510f8cec1def65fad09e10d3df8d0119dc50e81081caabd98e4e8d94707`  
		Last Modified: Tue, 02 Jun 2020 01:06:39 GMT  
		Size: 26.2 MB (26192840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ecdc50dd44d49d3ff8cdd957d4e1893829ea84a723d81f09b0a911e2d587c2`  
		Last Modified: Tue, 02 Jun 2020 01:06:32 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc5be41d45d3630667cb2545770a63595a49088d4b2a4ae3daae53a008363a8`  
		Last Modified: Tue, 02 Jun 2020 16:45:42 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de64e2d776275171935e9123baabb1a6e072d7ed4b7178988b038b3d88daa877`  
		Last Modified: Tue, 02 Jun 2020 16:45:42 GMT  
		Size: 669.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:latest` - linux; 386

```console
$ docker pull nginx@sha256:d09f8d172faa72bdb6022599732d1b0c7211bb40e4331759b96687c65cc45b68
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54783689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e605e720b28ba49b5fe668cbb7baa2ae48b7ed987ed65d93e9c5fc9cb2f4bbe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:22:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:38:32 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:38:32 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:38:32 GMT
ENV PKG_RELEASE=1~buster
# Tue, 02 Jun 2020 00:38:57 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:38:57 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:42:02 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:42:02 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:42:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:42:03 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:42:03 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:42:03 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5caba06751b9d9dfc9c8f4c47e677b6badd8fcb449d0652870e01306e7332bbd`  
		Last Modified: Tue, 02 Jun 2020 00:46:43 GMT  
		Size: 27.0 MB (27026663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc31e63c2ebde0ae51c591ba9c11db5772a6ff38067cdb37797d73680123036e`  
		Last Modified: Tue, 02 Jun 2020 00:46:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c097d8e7f2183ced23eedab9f0997c7383d7817720495e184810f0af5d0813`  
		Last Modified: Tue, 02 Jun 2020 16:42:58 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44574b6734e3a322310f85010f3a31d0553c8f7fe2cc2edb2b94987392072a7f`  
		Last Modified: Tue, 02 Jun 2020 16:42:58 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:latest` - linux; ppc64le

```console
$ docker pull nginx@sha256:ff830f286a93f3c5b644bba10ca76102782442d37451359abd7226e5a2d1a6bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58731955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ead72affddd05657dd9a5baa77b020938c8f25e91f358328829d0b615d7b689`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Fri, 29 May 2020 22:02:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:16:55 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:17:00 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:17:03 GMT
ENV PKG_RELEASE=1~buster
# Tue, 02 Jun 2020 00:33:01 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:33:10 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:24:53 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:24:59 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:25:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:25:17 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:25:23 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:25:28 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628316a1feaca142af0f8603f8ef328af4f80a33a4153f4165d9c9bdd118fdf8`  
		Last Modified: Tue, 02 Jun 2020 01:00:43 GMT  
		Size: 28.2 MB (28205386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7b0bd1a8205f022ecbd22ae25522fcd008ef5ea1514b564632eb8f20202dfd`  
		Last Modified: Tue, 02 Jun 2020 01:00:35 GMT  
		Size: 540.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43652592eb9547cc60a60df99c59337e30ba5eb223d80a74d6a3059a60cd1322`  
		Last Modified: Tue, 02 Jun 2020 16:28:24 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d822b6be9de43dd032998bb19acc615f5fc3ea0740663d3856904852c44ef6b3`  
		Last Modified: Tue, 02 Jun 2020 16:28:24 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:latest` - linux; s390x

```console
$ docker pull nginx@sha256:971a1b5f03103df52a6412c43cd841bdf431d2f000cf43e8aa9f85c90aac2202
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51561996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120f1bf01b9d08eaddac444b4f96fa0a6c5fbe4bf25f481cf1145580bee399e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:45:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 02 Jun 2020 00:42:41 GMT
ENV NGINX_VERSION=1.19.0
# Tue, 02 Jun 2020 00:42:41 GMT
ENV NJS_VERSION=0.4.1
# Tue, 02 Jun 2020 00:42:41 GMT
ENV PKG_RELEASE=1~buster
# Tue, 02 Jun 2020 00:45:01 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 02 Jun 2020 00:45:02 GMT
COPY file:d68fadb480cbc781c3424ce3e42e1b5be80133bdcce2569655e90411a4045da2 in / 
# Tue, 02 Jun 2020 16:44:19 GMT
COPY file:b96f664d94ca7bbe69241468d85ee421e9d310ffa36f3b04c762dcce9a42c7f1 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:19 GMT
COPY file:cc7d4f1d03426ebd11e960d6a487961e0540059dcfad14b33762f008eed03788 in /docker-entrypoint.d 
# Tue, 02 Jun 2020 16:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2020 16:44:19 GMT
EXPOSE 80
# Tue, 02 Jun 2020 16:44:20 GMT
STOPSIGNAL SIGTERM
# Tue, 02 Jun 2020 16:44:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb34024551c8d5b5d5cb3a0ae114d73e1ccc870a5b7476ae3f30a5dda6801e4`  
		Last Modified: Tue, 02 Jun 2020 00:51:38 GMT  
		Size: 25.8 MB (25846961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff57510e6e0e811c118d42fd8a320ec310705c4d6c9b3845749ba6d496a901f`  
		Last Modified: Tue, 02 Jun 2020 00:51:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cef171c6128d9c99cac81ddbdce683c5ec191e9d154786ce318df84d2d121b3`  
		Last Modified: Tue, 02 Jun 2020 16:45:06 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9a8a1f8e9046a1d316d4c043c0fbafde79e69c40a370d5a57592422cdd46`  
		Last Modified: Tue, 02 Jun 2020 16:45:11 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
