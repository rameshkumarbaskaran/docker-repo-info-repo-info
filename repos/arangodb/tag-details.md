<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.12`](#arangodb31012)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.6`](#arangodb3116)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:a2c600169d4dce0a12dd909662c1740d340f3f891f4255c6c6b1ec36a497abca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:1a4e028a50743c2e823c5703436015821c61cc0fceffe5b57638bd83eda6e837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225329875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee05011f33459e7ade4b4e83e0565a9cef8a1b7ce6c9601388795d1f672b37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:33:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 22 Dec 2023 17:38:17 GMT
ENV ARANGO_VERSION=3.10.12
# Fri, 22 Dec 2023 17:38:43 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 22 Dec 2023 17:38:44 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 22 Dec 2023 17:38:45 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 22 Dec 2023 17:38:45 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 22 Dec 2023 17:38:45 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 22 Dec 2023 17:38:45 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 22 Dec 2023 17:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 22 Dec 2023 17:38:45 GMT
EXPOSE 8529
# Fri, 22 Dec 2023 17:38:45 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baf5c83f90dfd907f58f4631ee828864bc54d9610bc302c44354dbe1bf1443a`  
		Last Modified: Fri, 22 Dec 2023 17:39:23 GMT  
		Size: 222.5 MB (222519608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb9e376cc8c99cf6303ec8061158f94c52ace2c42f3992c667f7154c82cb5`  
		Last Modified: Fri, 22 Dec 2023 17:39:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e4329109b522a9659d5b1dce2b24bdabc6291e38ec637632d67d3289c48844`  
		Last Modified: Fri, 22 Dec 2023 17:39:00 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82761ad8dd091548b812325d7e342c045356480f08ef6094bc04d9c2d2234983`  
		Last Modified: Fri, 22 Dec 2023 17:39:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:e3e3275f71ecf9dc5039e7900c556feb5d92e77a433d353175dce2e8d20ad45e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220417564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89125a94a8c746557e682113f2ff84c23db4118101b781e61171ed8a506938a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:53:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 22 Dec 2023 16:39:17 GMT
ENV ARANGO_VERSION=3.10.12
# Fri, 22 Dec 2023 16:39:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 22 Dec 2023 16:39:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 22 Dec 2023 16:39:47 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 22 Dec 2023 16:39:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 22 Dec 2023 16:39:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 22 Dec 2023 16:39:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 22 Dec 2023 16:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 22 Dec 2023 16:39:47 GMT
EXPOSE 8529
# Fri, 22 Dec 2023 16:39:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ae5b8832b9a4a54184dcbd587577e444cf122eeea688b7706a8c1807d7eae`  
		Last Modified: Fri, 22 Dec 2023 16:40:15 GMT  
		Size: 217.7 MB (217706783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5428c4930f6fc838a498d677cf4453764240ed57b96520c86b1580adee28d1be`  
		Last Modified: Fri, 22 Dec 2023 16:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e73e23e7b219b43fddf07bb7f5d5e46f692abebe576566e876ef0ef2df3b72a`  
		Last Modified: Fri, 22 Dec 2023 16:39:59 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b7cca2c2db5ee33c3621e2e0c9e3ccf1715a47d013d5e62ed1c19c4e0eb047`  
		Last Modified: Fri, 22 Dec 2023 16:39:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.12`

```console
$ docker pull arangodb@sha256:a2c600169d4dce0a12dd909662c1740d340f3f891f4255c6c6b1ec36a497abca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.12` - linux; amd64

```console
$ docker pull arangodb@sha256:1a4e028a50743c2e823c5703436015821c61cc0fceffe5b57638bd83eda6e837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225329875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee05011f33459e7ade4b4e83e0565a9cef8a1b7ce6c9601388795d1f672b37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:33:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 22 Dec 2023 17:38:17 GMT
ENV ARANGO_VERSION=3.10.12
# Fri, 22 Dec 2023 17:38:43 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 22 Dec 2023 17:38:44 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 22 Dec 2023 17:38:45 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 22 Dec 2023 17:38:45 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 22 Dec 2023 17:38:45 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 22 Dec 2023 17:38:45 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 22 Dec 2023 17:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 22 Dec 2023 17:38:45 GMT
EXPOSE 8529
# Fri, 22 Dec 2023 17:38:45 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baf5c83f90dfd907f58f4631ee828864bc54d9610bc302c44354dbe1bf1443a`  
		Last Modified: Fri, 22 Dec 2023 17:39:23 GMT  
		Size: 222.5 MB (222519608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb9e376cc8c99cf6303ec8061158f94c52ace2c42f3992c667f7154c82cb5`  
		Last Modified: Fri, 22 Dec 2023 17:39:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e4329109b522a9659d5b1dce2b24bdabc6291e38ec637632d67d3289c48844`  
		Last Modified: Fri, 22 Dec 2023 17:39:00 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82761ad8dd091548b812325d7e342c045356480f08ef6094bc04d9c2d2234983`  
		Last Modified: Fri, 22 Dec 2023 17:39:00 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.12` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:e3e3275f71ecf9dc5039e7900c556feb5d92e77a433d353175dce2e8d20ad45e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220417564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89125a94a8c746557e682113f2ff84c23db4118101b781e61171ed8a506938a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:53:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Fri, 22 Dec 2023 16:39:17 GMT
ENV ARANGO_VERSION=3.10.12
# Fri, 22 Dec 2023 16:39:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Fri, 22 Dec 2023 16:39:46 GMT
ENV GLIBCXX_FORCE_NEW=1
# Fri, 22 Dec 2023 16:39:47 GMT
RUN echo "UTC" > /etc/timezone
# Fri, 22 Dec 2023 16:39:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Fri, 22 Dec 2023 16:39:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Fri, 22 Dec 2023 16:39:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Fri, 22 Dec 2023 16:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 22 Dec 2023 16:39:47 GMT
EXPOSE 8529
# Fri, 22 Dec 2023 16:39:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2ae5b8832b9a4a54184dcbd587577e444cf122eeea688b7706a8c1807d7eae`  
		Last Modified: Fri, 22 Dec 2023 16:40:15 GMT  
		Size: 217.7 MB (217706783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5428c4930f6fc838a498d677cf4453764240ed57b96520c86b1580adee28d1be`  
		Last Modified: Fri, 22 Dec 2023 16:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e73e23e7b219b43fddf07bb7f5d5e46f692abebe576566e876ef0ef2df3b72a`  
		Last Modified: Fri, 22 Dec 2023 16:39:59 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b7cca2c2db5ee33c3621e2e0c9e3ccf1715a47d013d5e62ed1c19c4e0eb047`  
		Last Modified: Fri, 22 Dec 2023 16:39:59 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:fab8974562f4cf806d1b687a3a72b365c4647e3199c459f1e7fd6703c2397927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:475dcd25dd73abc6bdd0e935d77946561a8d5af60178d90b8e22916a692071d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249706114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d7122782e261f1b222bd101380de94f79c91ead13bcacf40c9c3864f9238e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:33:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 05 Dec 2023 18:19:24 GMT
ENV ARANGO_VERSION=3.11.6
# Tue, 05 Dec 2023 18:19:54 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 05 Dec 2023 18:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 05 Dec 2023 18:19:56 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 05 Dec 2023 18:19:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 05 Dec 2023 18:19:56 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 05 Dec 2023 18:19:56 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 05 Dec 2023 18:19:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Dec 2023 18:19:56 GMT
EXPOSE 8529
# Tue, 05 Dec 2023 18:19:57 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d69e031de529a7522030c32772ff9adb96f903f094b8ef9ab8945d17476209a`  
		Last Modified: Tue, 05 Dec 2023 18:20:35 GMT  
		Size: 246.9 MB (246895848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d16fe42b8dd4d8c3bd1821d523c818331e70bd1b7c7d91fc1c10ba85c53f82`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd02e1fb16f044d666e4530ef57ff818d752a3f34967dbbfa5dd60ec168eb6`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f77c37f7ab899407ec90a7c00c89cc1363fd7d866b96552738563c5f12235`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:b0627b11790bca396bab25097c2d0940c09f19749bed6f12081951e0f411d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243831370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8daadef97aa3b1fd2967d9e4654758ed0a6e5bdf655bbdad78e7b6a3ce9797`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:53:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 05 Dec 2023 17:39:16 GMT
ENV ARANGO_VERSION=3.11.6
# Tue, 05 Dec 2023 17:39:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 05 Dec 2023 17:39:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 05 Dec 2023 17:39:50 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 05 Dec 2023 17:39:50 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 05 Dec 2023 17:39:50 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 05 Dec 2023 17:39:50 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 05 Dec 2023 17:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Dec 2023 17:39:50 GMT
EXPOSE 8529
# Tue, 05 Dec 2023 17:39:50 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae8476c0054a82176b0a29098e04ecdbb1ea7324e40849f5014235afd50d629`  
		Last Modified: Tue, 05 Dec 2023 17:40:20 GMT  
		Size: 241.1 MB (241120590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad84b93e255d7c8a928830635cb49067f5e65c484ca0f7df1807e6d22812f0e`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ceb9fb0ef3ff1db3775d9c17fa6c334b8ebf39a308d8fa5824343bde7ab8bc3`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737b8448bc16570f1e609e627abfb0f8a45a0b2dfb559a242688528707d9a42e`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.6`

```console
$ docker pull arangodb@sha256:fab8974562f4cf806d1b687a3a72b365c4647e3199c459f1e7fd6703c2397927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.6` - linux; amd64

```console
$ docker pull arangodb@sha256:475dcd25dd73abc6bdd0e935d77946561a8d5af60178d90b8e22916a692071d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249706114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d7122782e261f1b222bd101380de94f79c91ead13bcacf40c9c3864f9238e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:33:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 05 Dec 2023 18:19:24 GMT
ENV ARANGO_VERSION=3.11.6
# Tue, 05 Dec 2023 18:19:54 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 05 Dec 2023 18:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 05 Dec 2023 18:19:56 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 05 Dec 2023 18:19:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 05 Dec 2023 18:19:56 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 05 Dec 2023 18:19:56 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 05 Dec 2023 18:19:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Dec 2023 18:19:56 GMT
EXPOSE 8529
# Tue, 05 Dec 2023 18:19:57 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d69e031de529a7522030c32772ff9adb96f903f094b8ef9ab8945d17476209a`  
		Last Modified: Tue, 05 Dec 2023 18:20:35 GMT  
		Size: 246.9 MB (246895848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d16fe42b8dd4d8c3bd1821d523c818331e70bd1b7c7d91fc1c10ba85c53f82`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd02e1fb16f044d666e4530ef57ff818d752a3f34967dbbfa5dd60ec168eb6`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f77c37f7ab899407ec90a7c00c89cc1363fd7d866b96552738563c5f12235`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.6` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:b0627b11790bca396bab25097c2d0940c09f19749bed6f12081951e0f411d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243831370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8daadef97aa3b1fd2967d9e4654758ed0a6e5bdf655bbdad78e7b6a3ce9797`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:53:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 05 Dec 2023 17:39:16 GMT
ENV ARANGO_VERSION=3.11.6
# Tue, 05 Dec 2023 17:39:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 05 Dec 2023 17:39:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 05 Dec 2023 17:39:50 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 05 Dec 2023 17:39:50 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 05 Dec 2023 17:39:50 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 05 Dec 2023 17:39:50 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 05 Dec 2023 17:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Dec 2023 17:39:50 GMT
EXPOSE 8529
# Tue, 05 Dec 2023 17:39:50 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae8476c0054a82176b0a29098e04ecdbb1ea7324e40849f5014235afd50d629`  
		Last Modified: Tue, 05 Dec 2023 17:40:20 GMT  
		Size: 241.1 MB (241120590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad84b93e255d7c8a928830635cb49067f5e65c484ca0f7df1807e6d22812f0e`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ceb9fb0ef3ff1db3775d9c17fa6c334b8ebf39a308d8fa5824343bde7ab8bc3`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737b8448bc16570f1e609e627abfb0f8a45a0b2dfb559a242688528707d9a42e`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:fab8974562f4cf806d1b687a3a72b365c4647e3199c459f1e7fd6703c2397927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:475dcd25dd73abc6bdd0e935d77946561a8d5af60178d90b8e22916a692071d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249706114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d7122782e261f1b222bd101380de94f79c91ead13bcacf40c9c3864f9238e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:33:14 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 05 Dec 2023 18:19:24 GMT
ENV ARANGO_VERSION=3.11.6
# Tue, 05 Dec 2023 18:19:54 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 05 Dec 2023 18:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 05 Dec 2023 18:19:56 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 05 Dec 2023 18:19:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 05 Dec 2023 18:19:56 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 05 Dec 2023 18:19:56 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 05 Dec 2023 18:19:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Dec 2023 18:19:56 GMT
EXPOSE 8529
# Tue, 05 Dec 2023 18:19:57 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d69e031de529a7522030c32772ff9adb96f903f094b8ef9ab8945d17476209a`  
		Last Modified: Tue, 05 Dec 2023 18:20:35 GMT  
		Size: 246.9 MB (246895848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d16fe42b8dd4d8c3bd1821d523c818331e70bd1b7c7d91fc1c10ba85c53f82`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd02e1fb16f044d666e4530ef57ff818d752a3f34967dbbfa5dd60ec168eb6`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5f77c37f7ab899407ec90a7c00c89cc1363fd7d866b96552738563c5f12235`  
		Last Modified: Tue, 05 Dec 2023 18:20:13 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:b0627b11790bca396bab25097c2d0940c09f19749bed6f12081951e0f411d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243831370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8daadef97aa3b1fd2967d9e4654758ed0a6e5bdf655bbdad78e7b6a3ce9797`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:53:16 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 05 Dec 2023 17:39:16 GMT
ENV ARANGO_VERSION=3.11.6
# Tue, 05 Dec 2023 17:39:45 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 05 Dec 2023 17:39:49 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 05 Dec 2023 17:39:50 GMT
RUN echo "UTC" > /etc/timezone
# Tue, 05 Dec 2023 17:39:50 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 05 Dec 2023 17:39:50 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 05 Dec 2023 17:39:50 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 05 Dec 2023 17:39:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Dec 2023 17:39:50 GMT
EXPOSE 8529
# Tue, 05 Dec 2023 17:39:50 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae8476c0054a82176b0a29098e04ecdbb1ea7324e40849f5014235afd50d629`  
		Last Modified: Tue, 05 Dec 2023 17:40:20 GMT  
		Size: 241.1 MB (241120590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad84b93e255d7c8a928830635cb49067f5e65c484ca0f7df1807e6d22812f0e`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ceb9fb0ef3ff1db3775d9c17fa6c334b8ebf39a308d8fa5824343bde7ab8bc3`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737b8448bc16570f1e609e627abfb0f8a45a0b2dfb559a242688528707d9a42e`  
		Last Modified: Tue, 05 Dec 2023 17:40:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
