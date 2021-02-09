## `nginx:stable`

```console
$ docker pull nginx@sha256:3cc9e2858798a99ea1c7a770d6f1e8a57a279a6ad61cae8a7e0541868c7a9cbc
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

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:efd06bdca03abe05d44291d09cb7be752fc8d30fb4390e990c88ccdc4ff5bd09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53574148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ffa24881a40b8598267ace567826fb6ec922979ef52d6dc42d3cc1e1269bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:51:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 06:54:00 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 06:54:00 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 06:54:01 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 06:54:24 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 06:54:24 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 06:54:24 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:54:25 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:54:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:54:25 GMT
EXPOSE 80
# Tue, 09 Feb 2021 06:54:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 06:54:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f243cde729c2a0e990a39dbde698b2cabebe4af534578bd1a9d9b639f88ff18`  
		Last Modified: Tue, 09 Feb 2021 06:56:16 GMT  
		Size: 26.5 MB (26476841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdf3948de696bf8af623318645773dee5cf7992c430f1d0e30254767b208a9d`  
		Last Modified: Tue, 09 Feb 2021 06:56:12 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e2ed4fd336b5b4d1281a2bd94902c9b67c01034c1bfdedf35619fa832012fb`  
		Last Modified: Tue, 09 Feb 2021 06:56:12 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb5403cda99b0d97c435f9cad87f2da7a0866630c78aaff005513baa24f624c`  
		Last Modified: Tue, 09 Feb 2021 06:56:13 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:fb589b89442c9debe8abe80d6c77e96c1f3e26268e07752628b81137803e5efa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50276568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f219b371c0a137f543428ce83bc4e7f0d7dc94a1bc4f34b7b679fefa51e0aaec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 11:45:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 12:00:09 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 12:00:12 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 12:00:15 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 12:06:54 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 12:06:55 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 12:06:56 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 12:06:57 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 12:06:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 12:06:58 GMT
EXPOSE 80
# Tue, 09 Feb 2021 12:06:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 12:06:59 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7042a3bfa3e7777bb5e7ef4fe36a0139a7abc68b08a77b11fe49f4229999d49d`  
		Last Modified: Tue, 09 Feb 2021 12:16:07 GMT  
		Size: 25.4 MB (25435102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e592963edfddb4f178d0b00b0c90ab35716aa9b352aacdec36151d844ef68b21`  
		Last Modified: Tue, 09 Feb 2021 12:16:00 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a2c1814603c4920ee85c3ec932ffc3d509165088a3166ab07e0a6e1e1d5dd`  
		Last Modified: Tue, 09 Feb 2021 12:16:01 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9f2aa798e865659bf3ea3d945213086ad7db01e5f048ff1afe01dae8a2494d`  
		Last Modified: Tue, 09 Feb 2021 12:16:00 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b0e24622e0717d4453ae834cafc39aa8888fe9a55f9a362b13cc7035fa3f3344
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47233074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b217099a74a4ec318e4a4320028b5f796e8c3834a56e6e41f966c007793355e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:59:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 07:12:15 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 07:12:16 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 07:12:16 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 07:18:17 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 07:18:18 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 07:18:19 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:18:20 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:18:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 07:18:21 GMT
EXPOSE 80
# Tue, 09 Feb 2021 07:18:22 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 07:18:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c421fccc7be476ed6d76c9a5096996912d3290f20f832439ad677987344f360`  
		Last Modified: Tue, 09 Feb 2021 07:26:40 GMT  
		Size: 24.5 MB (24527519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0419830fcac3943b12aa2598a7ae406cb55084e340a7c73cd2359230736126be`  
		Last Modified: Tue, 09 Feb 2021 07:26:34 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3a5fb16eae7b5cf601191fbafa8bca8671dd375d83af6587681886e41f794a`  
		Last Modified: Tue, 09 Feb 2021 07:26:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f7ce58fb608f4b75e1260544328f32c4ff5ca6af05c181fdad1ee9c88641ac`  
		Last Modified: Tue, 09 Feb 2021 07:26:34 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:2c599aef1bb56189e95d8be7759dfda3f5b2303c4b2709bea3b5fc2f24c519e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52139323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad97031190a14d8bd7afb97cc32eb04b22c7274cdf2d67788436b900ae63e42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:35:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 06:38:03 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 06:38:04 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 06:38:05 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 06:38:45 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 06:38:46 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 06:38:47 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:38:48 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 06:38:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 06:38:49 GMT
EXPOSE 80
# Tue, 09 Feb 2021 06:38:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 06:38:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200286247a6c7762fa467c0ac94b2d4b2255afc75f9aa71c5a326b5a292ee4cd`  
		Last Modified: Tue, 09 Feb 2021 06:41:43 GMT  
		Size: 26.3 MB (26285707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5ef0737ba2d4a23b160de1453186d2b21e01e0938f897b9b6bdb1d6064b46`  
		Last Modified: Tue, 09 Feb 2021 06:41:37 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4562cbb6aa8b37fdcb844c9c6164fa962c7c8b27dccb42161ac6583dc750574`  
		Last Modified: Tue, 09 Feb 2021 06:41:37 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042cb90dfea18e3bcee96b095458ae647b74d93240869230a70e7d49e57030e8`  
		Last Modified: Tue, 09 Feb 2021 06:41:36 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:aef3a80efacdfeccc50a17d5921d8b779b27691eea0ff3dd89d5ec8b04f9f231
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55075647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ce4224964332a7a209b7398e19b1e1d332eb055e1e791c235775180337a7de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:31:06 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 07:32:42 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 07:32:42 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 07:32:42 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 07:33:08 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 07:33:08 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 07:33:08 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:33:09 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:33:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 07:33:09 GMT
EXPOSE 80
# Tue, 09 Feb 2021 07:33:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 07:33:10 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08da1063f0aa7dbf17516d88ae95575704ecb5f5e7965a29ff20cff6c3de0aaa`  
		Last Modified: Tue, 09 Feb 2021 07:35:49 GMT  
		Size: 27.3 MB (27320749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d982a4d300c723483518c7e9e0bad8f19d9c96f1ca817fba6fb6d37e8ae3fe87`  
		Last Modified: Tue, 09 Feb 2021 07:35:42 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b0a081954f5311a37d2da8dffd19a881a5f70a3601d91b984151f13de2e3cc`  
		Last Modified: Tue, 09 Feb 2021 07:35:42 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f9ca792eea55718f9901a97db3c4516f2463a9c88ee85c5bc51f9b37aadd6`  
		Last Modified: Tue, 09 Feb 2021 07:35:43 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:28e844396aa4aefbf8cf81d77107c0fc6092ecd27b2ce0a544f605facd5b4687
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51806545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb8ae4de0d743f377418110713b20b553bee4bfc5b64c3e0859ba104bfbba43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:11:40 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 07:36:10 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 07:36:10 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 07:36:11 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 07:47:02 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 07:47:03 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 07:47:03 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:47:04 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 07:47:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 07:47:04 GMT
EXPOSE 80
# Tue, 09 Feb 2021 07:47:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 07:47:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf044918357f262a4a66c8c3d0ac7d49513a380ea585bb748596ad20eef541c`  
		Last Modified: Tue, 09 Feb 2021 08:01:39 GMT  
		Size: 26.0 MB (26039735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c632818f9fa82f081e1f0692a5c602e6dbac79269ab55424933d73354f646c4`  
		Last Modified: Tue, 09 Feb 2021 08:01:23 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4155e822eac101f6a2aabe8c7ecfee1a33bc706c95a7bc6685aa0b439486f4bb`  
		Last Modified: Tue, 09 Feb 2021 08:01:22 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1796a111113a0d4bf0b7740cd46f9c55fa917fb26dfba93c8549f9214c40df01`  
		Last Modified: Tue, 09 Feb 2021 08:01:22 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:94646ada8f9c670a7d05274381607fe0337e127ec8c46f33deb5d8932c9c0f62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59058218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d39512f53982cd52254eca535ecafca989113afe4f3fbb773e41658c9d13c80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:38:10 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 11:37:22 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 11:37:29 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 11:37:38 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 12:17:11 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 12:17:15 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 12:17:19 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 12:17:21 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 12:17:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 12:17:30 GMT
EXPOSE 80
# Tue, 09 Feb 2021 12:17:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 12:17:39 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f13fae67353e2e8d780dd122a85026e98d86e9819008ad2a5d01467a686383f`  
		Last Modified: Tue, 09 Feb 2021 12:49:48 GMT  
		Size: 28.5 MB (28536538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19af79969d1681d34101d86fe5ccc7e7566267a03ecc057b57072ba5ef2ec08`  
		Last Modified: Tue, 09 Feb 2021 12:49:42 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a21eeb5e6cdbc432b17436fb43aca5b24a369382663914c9978036918eb0065`  
		Last Modified: Tue, 09 Feb 2021 12:49:42 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d65dbbf86f134142dcd14abf9dda46d2b3effafffc0f5594ddc84845ec350b`  
		Last Modified: Tue, 09 Feb 2021 12:49:43 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:91a226c2f37b96bb2eb693f801187ee9a1a0ec52787af680c4ec04c73311d048
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51794999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5933b1497d8fe8d989cd8c1211f620c385a7677cf6eacdb89020ed3c3a6f44d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:33:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Feb 2021 05:39:21 GMT
ENV NGINX_VERSION=1.18.0
# Tue, 09 Feb 2021 05:39:21 GMT
ENV NJS_VERSION=0.4.4
# Tue, 09 Feb 2021 05:39:22 GMT
ENV PKG_RELEASE=2~buster
# Tue, 09 Feb 2021 05:42:03 GMT
RUN set -x     && addgroup --system --gid 101 nginx     && adduser --system --disabled-login --ingroup nginx --no-create-home --home /nonexistent --gecos "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEY=573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62;     found='';     for server in         ha.pool.sks-keyservers.net         hkp://keyserver.ubuntu.com:80         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         apt-key adv --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|i386|arm64)             echo "deb https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src https://nginx.org/packages/debian/ buster nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Feb 2021 05:42:05 GMT
COPY file:e7e183879c35719c18aa7f733651029fbcc55f5d8c22a877ae199b389425789e in / 
# Tue, 09 Feb 2021 05:42:05 GMT
COPY file:08ae525f517706a57131e1efe03acba0fdd4ecadddb55301484f05d2ec76c39a in /docker-entrypoint.d 
# Tue, 09 Feb 2021 05:42:05 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Feb 2021 05:42:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Feb 2021 05:42:06 GMT
EXPOSE 80
# Tue, 09 Feb 2021 05:42:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Feb 2021 05:42:06 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3eabd597ba132cf6b3fe196966088e5cddca605299d93871b67d11ac084205f`  
		Last Modified: Tue, 09 Feb 2021 05:48:22 GMT  
		Size: 26.1 MB (26082812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf2700556a01ce4ac80432a0a8daf536f0d942a6b5a8b8d8023a7a5505547b5`  
		Last Modified: Tue, 09 Feb 2021 05:48:18 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e467a76f6aca95782c47e9482e6cb3ade8f099d0cd661d3f9b38c08357550916`  
		Last Modified: Tue, 09 Feb 2021 05:48:19 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69e11b9a545e980266ec450e8fec1d1b08b7070beb9ecf94151bee2416a0e4f`  
		Last Modified: Tue, 09 Feb 2021 05:48:18 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
