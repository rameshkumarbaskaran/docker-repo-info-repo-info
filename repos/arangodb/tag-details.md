<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.15`](#arangodb3615)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.14`](#arangodb3714)
-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.0`](#arangodb380)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:e3cbd79fc78840d7e5f910fe7604417374d278789d3f4cf1b296e523f4904f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:427d3c4941c468aa48ff4c261ba00d507e591fb330c271103d583c198a8a840c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121513349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8328fa5e7216a428d79b14bb0cf34c8a27a0a73bd4aace4a4a2672d30e059ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:41:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:41:26 GMT
ENV ARANGO_VERSION=3.6.15
# Wed, 01 Sep 2021 00:41:26 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 01 Sep 2021 00:41:27 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.15-1_amd64.deb
# Wed, 01 Sep 2021 00:41:27 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.15-1_amd64.deb
# Wed, 01 Sep 2021 00:41:27 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.15-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:41:52 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:41:54 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:41:54 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:41:54 GMT
COPY file:0906ed6b024317ae8adc7caf5905c27c8ed6d7c227bbbfd131411e3fb9a6beaa in /entrypoint.sh 
# Wed, 01 Sep 2021 00:41:54 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:41:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:41:55 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:41:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d886b60dbbeb20e0599ebf34399f088da28ba8c79e8feca46c38f8e1637893a`  
		Last Modified: Wed, 01 Sep 2021 00:43:44 GMT  
		Size: 118.7 MB (118693602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeddb1572aea754182f029b938e0c9bd4e524b36a2fe9367f1293e3c54eda754`  
		Last Modified: Wed, 01 Sep 2021 00:43:25 GMT  
		Size: 2.2 KB (2178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef5c6a41989bdfa7a38d2aac3de2feb34700b33fd89adba988e66f324d0b202`  
		Last Modified: Wed, 01 Sep 2021 00:43:25 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.15`

```console
$ docker pull arangodb@sha256:e3cbd79fc78840d7e5f910fe7604417374d278789d3f4cf1b296e523f4904f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.6.15` - linux; amd64

```console
$ docker pull arangodb@sha256:427d3c4941c468aa48ff4c261ba00d507e591fb330c271103d583c198a8a840c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121513349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8328fa5e7216a428d79b14bb0cf34c8a27a0a73bd4aace4a4a2672d30e059ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:41:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:41:26 GMT
ENV ARANGO_VERSION=3.6.15
# Wed, 01 Sep 2021 00:41:26 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 01 Sep 2021 00:41:27 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.15-1_amd64.deb
# Wed, 01 Sep 2021 00:41:27 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.15-1_amd64.deb
# Wed, 01 Sep 2021 00:41:27 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.15-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:41:52 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:41:54 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:41:54 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:41:54 GMT
COPY file:0906ed6b024317ae8adc7caf5905c27c8ed6d7c227bbbfd131411e3fb9a6beaa in /entrypoint.sh 
# Wed, 01 Sep 2021 00:41:54 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:41:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:41:55 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:41:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d886b60dbbeb20e0599ebf34399f088da28ba8c79e8feca46c38f8e1637893a`  
		Last Modified: Wed, 01 Sep 2021 00:43:44 GMT  
		Size: 118.7 MB (118693602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeddb1572aea754182f029b938e0c9bd4e524b36a2fe9367f1293e3c54eda754`  
		Last Modified: Wed, 01 Sep 2021 00:43:25 GMT  
		Size: 2.2 KB (2178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef5c6a41989bdfa7a38d2aac3de2feb34700b33fd89adba988e66f324d0b202`  
		Last Modified: Wed, 01 Sep 2021 00:43:25 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:4c6fc608a72b2761e116a4b12046bcc8416cf33fc3cba4cab151fbf220a2e5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:c7d921d004179e549610141ed964de8e7715611a2b8c235712946259ac5ef6dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129551271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c306c0e600458ad3ac7cc6f29b8b657e61c00ba37ddc944d280e05f2184833a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:41:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:42:02 GMT
ENV ARANGO_VERSION=3.7.14
# Wed, 01 Sep 2021 00:42:02 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 01 Sep 2021 00:42:02 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.14-1_amd64.deb
# Wed, 01 Sep 2021 00:42:03 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.14-1_amd64.deb
# Wed, 01 Sep 2021 00:42:03 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.14-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:42:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:42:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:42:29 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:42:29 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:42:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:42:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:42:30 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:42:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9c0e2ae2c997d682bea390f8e0b3d641c3e1eb9026dd97b557f0c4633f9eb`  
		Last Modified: Wed, 01 Sep 2021 00:44:17 GMT  
		Size: 126.7 MB (126731617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b43fcd5476861d2d4551ebd2f536a21b56c0b2ef0947524bd48a73b98fea7e`  
		Last Modified: Wed, 01 Sep 2021 00:43:56 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cd9e507dbd9769623929f3d604788b61cf1c18d8bc45e618e1450101dedc13`  
		Last Modified: Wed, 01 Sep 2021 00:43:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.14`

```console
$ docker pull arangodb@sha256:4c6fc608a72b2761e116a4b12046bcc8416cf33fc3cba4cab151fbf220a2e5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7.14` - linux; amd64

```console
$ docker pull arangodb@sha256:c7d921d004179e549610141ed964de8e7715611a2b8c235712946259ac5ef6dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129551271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c306c0e600458ad3ac7cc6f29b8b657e61c00ba37ddc944d280e05f2184833a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:41:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:42:02 GMT
ENV ARANGO_VERSION=3.7.14
# Wed, 01 Sep 2021 00:42:02 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 01 Sep 2021 00:42:02 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.14-1_amd64.deb
# Wed, 01 Sep 2021 00:42:03 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.14-1_amd64.deb
# Wed, 01 Sep 2021 00:42:03 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.14-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:42:28 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:42:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:42:29 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:42:29 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:42:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:42:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:42:30 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:42:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9c0e2ae2c997d682bea390f8e0b3d641c3e1eb9026dd97b557f0c4633f9eb`  
		Last Modified: Wed, 01 Sep 2021 00:44:17 GMT  
		Size: 126.7 MB (126731617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b43fcd5476861d2d4551ebd2f536a21b56c0b2ef0947524bd48a73b98fea7e`  
		Last Modified: Wed, 01 Sep 2021 00:43:56 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cd9e507dbd9769623929f3d604788b61cf1c18d8bc45e618e1450101dedc13`  
		Last Modified: Wed, 01 Sep 2021 00:43:56 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:b85c1689522b21c465264ae72bc8b4df343186ca8c7660a1a4fd27bf7bdc4d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:39180922715a1150538b46532d5d0bf706364ae2d4ee37dfd5ade34591847a94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187552709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d505e91be9ab549fedccbeef081c87475b77a524a8dcaa810cf0cf10535db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:42:38 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_VERSION=3.8.0
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.0-1_amd64.deb
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.0-1_amd64.deb
# Wed, 01 Sep 2021 00:42:39 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.0-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:43:06 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:43:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:43:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:43:08 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:43:08 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:43:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:43:09 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:43:09 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65900f23759fc093cdabe7a9dde59ea044b69774f7f5730df46bd364d79bca`  
		Last Modified: Wed, 01 Sep 2021 00:44:58 GMT  
		Size: 184.7 MB (184748657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af671c214e916ef1878ddbc95b17f9ac7cfa1c72b5e700da65d0a59568c488`  
		Last Modified: Wed, 01 Sep 2021 00:44:27 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9eabdc8588b21630939ed10deba5b3c861d330fececc09a0457948b5c04e314`  
		Last Modified: Wed, 01 Sep 2021 00:44:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.0`

```console
$ docker pull arangodb@sha256:b85c1689522b21c465264ae72bc8b4df343186ca8c7660a1a4fd27bf7bdc4d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.0` - linux; amd64

```console
$ docker pull arangodb@sha256:39180922715a1150538b46532d5d0bf706364ae2d4ee37dfd5ade34591847a94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187552709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d505e91be9ab549fedccbeef081c87475b77a524a8dcaa810cf0cf10535db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:42:38 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_VERSION=3.8.0
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.0-1_amd64.deb
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.0-1_amd64.deb
# Wed, 01 Sep 2021 00:42:39 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.0-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:43:06 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:43:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:43:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:43:08 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:43:08 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:43:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:43:09 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:43:09 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65900f23759fc093cdabe7a9dde59ea044b69774f7f5730df46bd364d79bca`  
		Last Modified: Wed, 01 Sep 2021 00:44:58 GMT  
		Size: 184.7 MB (184748657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af671c214e916ef1878ddbc95b17f9ac7cfa1c72b5e700da65d0a59568c488`  
		Last Modified: Wed, 01 Sep 2021 00:44:27 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9eabdc8588b21630939ed10deba5b3c861d330fececc09a0457948b5c04e314`  
		Last Modified: Wed, 01 Sep 2021 00:44:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:b85c1689522b21c465264ae72bc8b4df343186ca8c7660a1a4fd27bf7bdc4d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:39180922715a1150538b46532d5d0bf706364ae2d4ee37dfd5ade34591847a94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187552709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d505e91be9ab549fedccbeef081c87475b77a524a8dcaa810cf0cf10535db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:42:38 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_VERSION=3.8.0
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.0-1_amd64.deb
# Wed, 01 Sep 2021 00:42:38 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.0-1_amd64.deb
# Wed, 01 Sep 2021 00:42:39 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.0-1_amd64.deb.asc
# Wed, 01 Sep 2021 00:43:06 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 01 Sep 2021 00:43:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 01 Sep 2021 00:43:08 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 01 Sep 2021 00:43:08 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:43:08 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 01 Sep 2021 00:43:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:43:09 GMT
EXPOSE 8529
# Wed, 01 Sep 2021 00:43:09 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65900f23759fc093cdabe7a9dde59ea044b69774f7f5730df46bd364d79bca`  
		Last Modified: Wed, 01 Sep 2021 00:44:58 GMT  
		Size: 184.7 MB (184748657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af671c214e916ef1878ddbc95b17f9ac7cfa1c72b5e700da65d0a59568c488`  
		Last Modified: Wed, 01 Sep 2021 00:44:27 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9eabdc8588b21630939ed10deba5b3c861d330fececc09a0457948b5c04e314`  
		Last Modified: Wed, 01 Sep 2021 00:44:27 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
