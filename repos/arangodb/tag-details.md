<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.7`](#arangodb387)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.3`](#arangodb393)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:7f3e61c9fdd06b02823ec9d96374e8e3fd0c84218deb259722b962200a521ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:622ad0ed058b3bda6cbbbbda4495cc72e4718379debc3466cb7521fe5f6b7a57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194446214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594c0bba3104220b7240160da55d09ecc51b5f6c3df952744f5ffabc42e636d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:48:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 09 Aug 2022 17:48:37 GMT
ENV ARANGO_VERSION=3.8.7
# Tue, 09 Aug 2022 17:48:37 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Tue, 09 Aug 2022 17:48:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.7-1_amd64.deb
# Tue, 09 Aug 2022 17:48:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb
# Tue, 09 Aug 2022 17:48:38 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb.asc
# Tue, 09 Aug 2022 17:49:03 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 09 Aug 2022 17:49:05 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 09 Aug 2022 17:49:05 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 09 Aug 2022 17:49:05 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 09 Aug 2022 17:49:05 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 09 Aug 2022 17:49:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 17:49:05 GMT
EXPOSE 8529
# Tue, 09 Aug 2022 17:49:05 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510c13ebe38630ae7d0da96c3bec11c313169fb15e64bebb14c7825db3bec2c0`  
		Last Modified: Tue, 09 Aug 2022 17:50:50 GMT  
		Size: 191.6 MB (191616375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd208bd903b0736645e7a3005e42fdd8c6de3e95deabe26019133107878a34`  
		Last Modified: Tue, 09 Aug 2022 17:50:27 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac74b32a1ceb396ec09a3590353d613ed7c51656b58da2f3fc3177a366bb6303`  
		Last Modified: Tue, 09 Aug 2022 17:50:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.7`

```console
$ docker pull arangodb@sha256:7f3e61c9fdd06b02823ec9d96374e8e3fd0c84218deb259722b962200a521ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.7` - linux; amd64

```console
$ docker pull arangodb@sha256:622ad0ed058b3bda6cbbbbda4495cc72e4718379debc3466cb7521fe5f6b7a57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194446214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594c0bba3104220b7240160da55d09ecc51b5f6c3df952744f5ffabc42e636d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:48:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 09 Aug 2022 17:48:37 GMT
ENV ARANGO_VERSION=3.8.7
# Tue, 09 Aug 2022 17:48:37 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Tue, 09 Aug 2022 17:48:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.7-1_amd64.deb
# Tue, 09 Aug 2022 17:48:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb
# Tue, 09 Aug 2022 17:48:38 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb.asc
# Tue, 09 Aug 2022 17:49:03 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 09 Aug 2022 17:49:05 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 09 Aug 2022 17:49:05 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 09 Aug 2022 17:49:05 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 09 Aug 2022 17:49:05 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 09 Aug 2022 17:49:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 17:49:05 GMT
EXPOSE 8529
# Tue, 09 Aug 2022 17:49:05 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510c13ebe38630ae7d0da96c3bec11c313169fb15e64bebb14c7825db3bec2c0`  
		Last Modified: Tue, 09 Aug 2022 17:50:50 GMT  
		Size: 191.6 MB (191616375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd208bd903b0736645e7a3005e42fdd8c6de3e95deabe26019133107878a34`  
		Last Modified: Tue, 09 Aug 2022 17:50:27 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac74b32a1ceb396ec09a3590353d613ed7c51656b58da2f3fc3177a366bb6303`  
		Last Modified: Tue, 09 Aug 2022 17:50:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:07181a0f5a93fda243933dc415798fc392ac5673da129ebcc13598210996456d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:5eb0c24d5e9befbd5f8fba31980a2789cd365b1319f80de4200ded4f796c066e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200177968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00373f397f2ced2e2ab0144a75d6a3b4c4663df64415456fe3f3f0a51941dc20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:48:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_VERSION=3.9.3
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.3-1_amd64.deb
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.3-1_amd64.deb
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.3-1_amd64.deb.asc
# Wed, 07 Sep 2022 20:23:19 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 07 Sep 2022 20:23:21 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 07 Sep 2022 20:23:21 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 07 Sep 2022 20:23:21 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 07 Sep 2022 20:23:21 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 07 Sep 2022 20:23:22 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 07 Sep 2022 20:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Sep 2022 20:23:22 GMT
EXPOSE 8529
# Wed, 07 Sep 2022 20:23:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6b21f85a5301ed9af7f1927d9d045aa87440141ee05e6198ee8e1c0b837850`  
		Last Modified: Wed, 07 Sep 2022 20:23:58 GMT  
		Size: 197.3 MB (197347994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b13a78e70aeb03e9aeb90587ad815681ef823a88a7c13413b1c13d53cbf21a`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed4f8b92486ed6e3ce673af51eb8eafbb210efd0de2c9836b9f5a9c2e83c1b`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f48578b9327bb79cf8e31ee2bb878e1bf434f2119203d4452e1d31a82779059`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.3`

```console
$ docker pull arangodb@sha256:07181a0f5a93fda243933dc415798fc392ac5673da129ebcc13598210996456d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.3` - linux; amd64

```console
$ docker pull arangodb@sha256:5eb0c24d5e9befbd5f8fba31980a2789cd365b1319f80de4200ded4f796c066e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200177968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00373f397f2ced2e2ab0144a75d6a3b4c4663df64415456fe3f3f0a51941dc20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:48:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_VERSION=3.9.3
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.3-1_amd64.deb
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.3-1_amd64.deb
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.3-1_amd64.deb.asc
# Wed, 07 Sep 2022 20:23:19 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 07 Sep 2022 20:23:21 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 07 Sep 2022 20:23:21 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 07 Sep 2022 20:23:21 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 07 Sep 2022 20:23:21 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 07 Sep 2022 20:23:22 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 07 Sep 2022 20:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Sep 2022 20:23:22 GMT
EXPOSE 8529
# Wed, 07 Sep 2022 20:23:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6b21f85a5301ed9af7f1927d9d045aa87440141ee05e6198ee8e1c0b837850`  
		Last Modified: Wed, 07 Sep 2022 20:23:58 GMT  
		Size: 197.3 MB (197347994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b13a78e70aeb03e9aeb90587ad815681ef823a88a7c13413b1c13d53cbf21a`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed4f8b92486ed6e3ce673af51eb8eafbb210efd0de2c9836b9f5a9c2e83c1b`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f48578b9327bb79cf8e31ee2bb878e1bf434f2119203d4452e1d31a82779059`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:07181a0f5a93fda243933dc415798fc392ac5673da129ebcc13598210996456d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:5eb0c24d5e9befbd5f8fba31980a2789cd365b1319f80de4200ded4f796c066e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200177968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00373f397f2ced2e2ab0144a75d6a3b4c4663df64415456fe3f3f0a51941dc20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 17:48:04 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_VERSION=3.9.3
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.3-1_amd64.deb
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.3-1_amd64.deb
# Wed, 07 Sep 2022 20:22:51 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.3-1_amd64.deb.asc
# Wed, 07 Sep 2022 20:23:19 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 07 Sep 2022 20:23:21 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 07 Sep 2022 20:23:21 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 07 Sep 2022 20:23:21 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 07 Sep 2022 20:23:21 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 07 Sep 2022 20:23:22 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 07 Sep 2022 20:23:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Sep 2022 20:23:22 GMT
EXPOSE 8529
# Wed, 07 Sep 2022 20:23:22 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6b21f85a5301ed9af7f1927d9d045aa87440141ee05e6198ee8e1c0b837850`  
		Last Modified: Wed, 07 Sep 2022 20:23:58 GMT  
		Size: 197.3 MB (197347994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b13a78e70aeb03e9aeb90587ad815681ef823a88a7c13413b1c13d53cbf21a`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed4f8b92486ed6e3ce673af51eb8eafbb210efd0de2c9836b9f5a9c2e83c1b`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f48578b9327bb79cf8e31ee2bb878e1bf434f2119203d4452e1d31a82779059`  
		Last Modified: Wed, 07 Sep 2022 20:23:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
