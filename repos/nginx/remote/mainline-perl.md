## `nginx:mainline-perl`

```console
$ docker pull nginx@sha256:b16c82ace905f547b13823ef9e7694810ed54a86f850e9a933db15a28a77861e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `nginx:mainline-perl` - linux; amd64

```console
$ docker pull nginx@sha256:e44d18103b02f7d64ae72136446932cbcdadb66455bb222df7ef6093b24aa3b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64578478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3215b5fa7c06e43f28b8c3c3fc07ef87fdd2e3609a1953798ab301c625b2742`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:51:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 06:51:31 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 06:51:32 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 06:51:32 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 06:53:43 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 06:53:43 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 06:53:44 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:53:44 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:53:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:53:44 GMT
EXPOSE 80
# Tue, 09 Feb 2021 06:53:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 06:53:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c0c95458fe953580693442981226f59268b99c38fc731a64462ecb324f2d1`  
		Last Modified: Tue, 09 Feb 2021 06:56:00 GMT  
		Size: 37.5 MB (37481179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01356b1e6257bb3de91f074d35a80d4c7e0dfa45d5af5872a43e4444981d76`  
		Last Modified: Tue, 09 Feb 2021 06:55:52 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618499b3e6690a2a3504c15f35b0cc74a5ce01560a276f21e4e8721ee6e5600f`  
		Last Modified: Tue, 09 Feb 2021 06:55:52 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8796de292aabaa9588be8aa0ba1c48ba475b1d8ebff8e5d0fbfd045d9b8eb7ff`  
		Last Modified: Tue, 09 Feb 2021 06:55:52 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:4b9395356342f8ec60df8e2e2603f6faa7251b29a96dbb6b389be01aeaf42dd4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60517294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31f43b7a534e22822d287828be707916f459832b6e4cf14805be5e394faa866`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:45:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 11:45:31 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 11:45:32 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 11:45:32 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 11:59:40 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 11:59:42 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 11:59:43 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 11:59:44 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 11:59:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 11:59:46 GMT
EXPOSE 80
# Tue, 09 Feb 2021 11:59:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 11:59:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039daf7041c0d0b439356b9f39dd7d7b70cea37cc01b4df0b31a17c824c7dc17`  
		Last Modified: Tue, 09 Feb 2021 12:15:49 GMT  
		Size: 35.7 MB (35675835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bad76d2bffe6b460ed88fe291cdc1108015f210801b63070f663da9f5d6fed`  
		Last Modified: Tue, 09 Feb 2021 12:15:35 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92209fb0112fd7a79bc0ca1450d2033ec9926e021dbad90566327700c600ad3`  
		Last Modified: Tue, 09 Feb 2021 12:15:35 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed4fe549f2f0791c7b0a4ac5a36d2203ba3846e06212a55a8b8a50408f09196`  
		Last Modified: Tue, 09 Feb 2021 12:15:35 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:7021fa1c08e46e0686ec95b29965d8c0d794ce1a96e9fd7152babe4b7c8ef4a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57274421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5707ab48fe10d2208d1b45b7d8187f1f58f62e835dca241f691b394756b7ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:59:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 06:59:02 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 06:59:03 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 06:59:03 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 07:11:38 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 07:11:40 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 07:11:41 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:11:42 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:11:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 07:11:45 GMT
EXPOSE 80
# Tue, 09 Feb 2021 07:11:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 07:11:46 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8dc3a44f6aa6306f784cefa3a081889b0cad29d9725a1fb42f418dca327d11`  
		Last Modified: Tue, 09 Feb 2021 07:26:14 GMT  
		Size: 34.6 MB (34568878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e8c61e206624370ba581083490a81cd4be336cb63e9712cfde77cab12fa6ae`  
		Last Modified: Tue, 09 Feb 2021 07:26:03 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3325171b12028d2c045f14e71cf6313ff2767c6df619ae0b1bdf7776c74bf96d`  
		Last Modified: Tue, 09 Feb 2021 07:26:06 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de4bc7cd0ddcb42563936af2f0c8c3b93eee3c281e752e10dc7b3604f6e6299`  
		Last Modified: Tue, 09 Feb 2021 07:26:04 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:869af316fec24f6b347537a69e07850481b4fbfece958967c909b7b20831a57e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63040158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8915728513cd5dfcf18f559a2e197b68a4f6175481e61f256852f05460feda5c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:35:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 06:35:53 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 06:35:54 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 06:35:55 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 06:37:32 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 06:37:33 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 06:37:34 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:37:35 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:37:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:37:36 GMT
EXPOSE 80
# Tue, 09 Feb 2021 06:37:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 06:37:37 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6b2f1c38bc3a3268f22fd3a13a17aeb7836d4c5b7d499aed5300531f23373f`  
		Last Modified: Tue, 09 Feb 2021 06:41:19 GMT  
		Size: 37.2 MB (37186553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6d1fd67305ec3b2b07341c5c129a5d42396f8641fac0895d61a4bb0e47813a`  
		Last Modified: Tue, 09 Feb 2021 06:41:10 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9971a6b418d9a27dcfeec4cddf150c506267329cc1190be2fbfed9d389de717`  
		Last Modified: Tue, 09 Feb 2021 06:41:10 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bca96fa698abe88cb995e19bce1e41e03e8ef7e95ab1f3c6d5fd03b1489be0b`  
		Last Modified: Tue, 09 Feb 2021 06:41:10 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; 386

```console
$ docker pull nginx@sha256:88188086648e90976ff991b59148402416c47bd83460458851b8a6f47bf05eeb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65558081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909767196978ccb9a6759b15f0f2888dfa1fe441bfb64f880738e4d38dcc5189`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:31:06 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 07:31:06 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 07:31:06 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 07:31:06 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 07:32:25 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 07:32:25 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 07:32:26 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:32:26 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:32:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 07:32:26 GMT
EXPOSE 80
# Tue, 09 Feb 2021 07:32:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 07:32:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dec52ca1dc2da1773dd95575cc6a147aa9e7847b9176b9413240205af46c55`  
		Last Modified: Tue, 09 Feb 2021 07:35:30 GMT  
		Size: 37.8 MB (37803190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5bb8c7b7f5601bbdfd4c8a286f9b695602498f6f47d69bdeff7a218bce0b63`  
		Last Modified: Tue, 09 Feb 2021 07:35:20 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a896b0d2b586c423e631c925a1d815e545a5c1892d2e8b859a90e15890b543e`  
		Last Modified: Tue, 09 Feb 2021 07:35:19 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5033d478e9fe5a7084e573b70e69081d036f20e3e8ceb9018e501da5f26c2917`  
		Last Modified: Tue, 09 Feb 2021 07:35:19 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; mips64le

```console
$ docker pull nginx@sha256:96cd05df6e1b30e4bacaea562b40fcd7f971dcaf717974f4145132d10fa6b6af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62073250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072bf3a74407efe97094c58324b5bd1ee87bd17d161c7f5ff7a3526fd0ba02ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:11:40 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 07:11:40 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 07:11:40 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 07:11:41 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 07:35:53 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 07:35:54 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 07:35:54 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:35:54 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:35:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 07:35:55 GMT
EXPOSE 80
# Tue, 09 Feb 2021 07:35:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 07:35:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ae95484e3ac8e0f15af8ff490da4017bb078dcb80893ff5088803a37d9739`  
		Last Modified: Tue, 09 Feb 2021 08:00:52 GMT  
		Size: 36.3 MB (36306445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce7f20383977d9f12361c7a62228e6bc3a5a22877c1f5da11b77d9b47a716ef`  
		Last Modified: Tue, 09 Feb 2021 08:00:26 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68716fcc4d78b16e32aab3116729eb376073f8f0370538a2c10980ed02f413f`  
		Last Modified: Tue, 09 Feb 2021 08:00:26 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c218318dd825bf3d2c1d91bb6541e36b29378aa11aa839384fb5af573cd7db`  
		Last Modified: Tue, 09 Feb 2021 08:00:26 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:f998053942a5e45c6f5aa4e0516174727e3a2da7c76b8e3656a9173a692b4e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70280618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6500d727359575e438d435d04b6c8c6f2fa9240fce2dc5fb8a80287b4a97e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:38:10 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 10:38:13 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 10:38:18 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 10:38:33 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 11:35:47 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 11:35:58 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 11:36:00 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 11:36:02 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 11:36:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 11:36:17 GMT
EXPOSE 80
# Tue, 09 Feb 2021 11:36:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 11:36:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e02b1fc629a841d543ba0afa1b9af382ed5edae0ee5c6a3265536091d76fe9`  
		Last Modified: Tue, 09 Feb 2021 12:49:22 GMT  
		Size: 39.8 MB (39758944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f085968d60b048dbb85460844a7bcae964c63d25e5b536bdb49b3a6f0ba91fa`  
		Last Modified: Tue, 09 Feb 2021 12:49:14 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d315b2c5d9ff1404a9e9f10e51b2c3b6e545915dfd25801b589e69be2aaa512f`  
		Last Modified: Tue, 09 Feb 2021 12:49:14 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d49adb396ef01d9279960dd685e46ee2bfe3b8563ee5dddae9775c5f2911096`  
		Last Modified: Tue, 09 Feb 2021 12:49:14 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:mainline-perl` - linux; s390x

```console
$ docker pull nginx@sha256:e311064b5b2d9af752ad4147a132ab16ac19874ecc2243ab98523d9f59b38f45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63078028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1ac895658fc7d6e9af91d47ca8ceade6fd94b34bbb47e20c132d3df123d4ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:33:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 05:33:05 GMT
ENV NGINX_VERSION=1.19.6
# Tue, 09 Feb 2021 05:33:06 GMT
ENV NJS_VERSION=0.5.0
# Tue, 09 Feb 2021 05:33:06 GMT
ENV PKG_RELEASE=1~buster
# Tue, 09 Feb 2021 05:38:58 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/mainline/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 05:39:00 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 05:39:00 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Feb 2021 05:39:00 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 05:39:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 05:39:01 GMT
EXPOSE 80
# Tue, 09 Feb 2021 05:39:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 05:39:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e651a13c8cf594fa21059ca4e54328057069a3f8ebf261be4f7778d4790457c`  
		Last Modified: Tue, 09 Feb 2021 05:48:03 GMT  
		Size: 37.4 MB (37365847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039676796d036a91c8f9388a1eef34d77830ade6b620fcd26f013f4e9a4003e4`  
		Last Modified: Tue, 09 Feb 2021 05:47:57 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff8cd35465df2508d18a2789f6858ea66aa9d93d572bdebeba75d349a44ebaf`  
		Last Modified: Tue, 09 Feb 2021 05:47:57 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ba1d09578160cfe2941d86b3f095647dfd6ca9d2da46b8cd4d88ac50ce500e`  
		Last Modified: Tue, 09 Feb 2021 05:47:57 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
