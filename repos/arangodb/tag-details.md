<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.6`](#arangodb36)
-	[`arangodb:3.6.12`](#arangodb3612)
-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.10`](#arangodb3710)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.6`

```console
$ docker pull arangodb@sha256:0a636974158ec45739be327d2420dbdfa47e3072f84da8260273e3f841d10d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6` - linux; amd64

```console
$ docker pull arangodb@sha256:d249710e4cadf71f53561518fc23564df7e985b9def131f1717118ee38a97a5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119543913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fb6b25fc2c66a7d4832e6556d8b6acb9c71ecde99a3c75fb692e0b46fc340e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:19:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 01 Apr 2021 13:19:41 GMT
ENV ARANGO_VERSION=3.6.12
# Thu, 01 Apr 2021 13:19:41 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Thu, 01 Apr 2021 13:19:41 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.12-1_amd64.deb
# Thu, 01 Apr 2021 13:19:42 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb
# Thu, 01 Apr 2021 13:19:42 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb.asc
# Thu, 01 Apr 2021 13:20:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 01 Apr 2021 13:20:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 01 Apr 2021 13:20:07 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 01 Apr 2021 13:20:07 GMT
COPY file:0906ed6b024317ae8adc7caf5905c27c8ed6d7c227bbbfd131411e3fb9a6beaa in /entrypoint.sh 
# Thu, 01 Apr 2021 13:20:07 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 01 Apr 2021 13:20:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:08 GMT
EXPOSE 8529
# Thu, 01 Apr 2021 13:20:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9dd448d8d3b9cadefcc31cb486477c1364a793c1551d1a187dbbb0a0f682d`  
		Last Modified: Thu, 01 Apr 2021 13:21:08 GMT  
		Size: 116.7 MB (116726128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558abd8049751b850de586dad855aab4d727069861208cc7b7086453fa7abf0a`  
		Last Modified: Thu, 01 Apr 2021 13:20:50 GMT  
		Size: 2.2 KB (2178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1970651eda7723f3b4d717c7476cc7779bc9ba19da80caa2f943603966c278c`  
		Last Modified: Thu, 01 Apr 2021 13:20:50 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.6.12`

```console
$ docker pull arangodb@sha256:0a636974158ec45739be327d2420dbdfa47e3072f84da8260273e3f841d10d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.6.12` - linux; amd64

```console
$ docker pull arangodb@sha256:d249710e4cadf71f53561518fc23564df7e985b9def131f1717118ee38a97a5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119543913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fb6b25fc2c66a7d4832e6556d8b6acb9c71ecde99a3c75fb692e0b46fc340e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:19:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 01 Apr 2021 13:19:41 GMT
ENV ARANGO_VERSION=3.6.12
# Thu, 01 Apr 2021 13:19:41 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Thu, 01 Apr 2021 13:19:41 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.12-1_amd64.deb
# Thu, 01 Apr 2021 13:19:42 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb
# Thu, 01 Apr 2021 13:19:42 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.12-1_amd64.deb.asc
# Thu, 01 Apr 2021 13:20:05 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 01 Apr 2021 13:20:07 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 01 Apr 2021 13:20:07 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 01 Apr 2021 13:20:07 GMT
COPY file:0906ed6b024317ae8adc7caf5905c27c8ed6d7c227bbbfd131411e3fb9a6beaa in /entrypoint.sh 
# Thu, 01 Apr 2021 13:20:07 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 01 Apr 2021 13:20:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:08 GMT
EXPOSE 8529
# Thu, 01 Apr 2021 13:20:08 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9dd448d8d3b9cadefcc31cb486477c1364a793c1551d1a187dbbb0a0f682d`  
		Last Modified: Thu, 01 Apr 2021 13:21:08 GMT  
		Size: 116.7 MB (116726128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558abd8049751b850de586dad855aab4d727069861208cc7b7086453fa7abf0a`  
		Last Modified: Thu, 01 Apr 2021 13:20:50 GMT  
		Size: 2.2 KB (2178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1970651eda7723f3b4d717c7476cc7779bc9ba19da80caa2f943603966c278c`  
		Last Modified: Thu, 01 Apr 2021 13:20:50 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:bdb6e4b46792189b8fad1e275b6958153333a4c4a6fc4ffedee04ca8782db776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:c257f68d1294a261345121f7b19ee9f5adbe9d498c9ee59a0217ec4b32bdcef4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae27c54e722b70ab19e8f09c575731f8d64e7d080773041e893479cb2e01b45a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:19:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_VERSION=3.7.10
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.10-1_amd64.deb
# Thu, 01 Apr 2021 13:20:12 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb
# Thu, 01 Apr 2021 13:20:12 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb.asc
# Thu, 01 Apr 2021 13:20:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 01 Apr 2021 13:20:34 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 01 Apr 2021 13:20:34 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 01 Apr 2021 13:20:34 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:20:34 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 01 Apr 2021 13:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:35 GMT
EXPOSE 8529
# Thu, 01 Apr 2021 13:20:35 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cc33dc011029d5ce0c62edfbc9615a3ad61d2cdd608f5870884148343818e6`  
		Last Modified: Thu, 01 Apr 2021 13:21:37 GMT  
		Size: 125.6 MB (125555749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2002013d5dbd37e4a82f2b4150a90cf859019c35fb14a185e420d36e205b89f0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ffaac061aeb56201c6d977ec1906a5fc4baa5702a5be2944cc50241427c60`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.10`

```console
$ docker pull arangodb@sha256:bdb6e4b46792189b8fad1e275b6958153333a4c4a6fc4ffedee04ca8782db776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:3.7.10` - linux; amd64

```console
$ docker pull arangodb@sha256:c257f68d1294a261345121f7b19ee9f5adbe9d498c9ee59a0217ec4b32bdcef4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae27c54e722b70ab19e8f09c575731f8d64e7d080773041e893479cb2e01b45a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:19:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_VERSION=3.7.10
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.10-1_amd64.deb
# Thu, 01 Apr 2021 13:20:12 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb
# Thu, 01 Apr 2021 13:20:12 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb.asc
# Thu, 01 Apr 2021 13:20:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 01 Apr 2021 13:20:34 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 01 Apr 2021 13:20:34 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 01 Apr 2021 13:20:34 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:20:34 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 01 Apr 2021 13:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:35 GMT
EXPOSE 8529
# Thu, 01 Apr 2021 13:20:35 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cc33dc011029d5ce0c62edfbc9615a3ad61d2cdd608f5870884148343818e6`  
		Last Modified: Thu, 01 Apr 2021 13:21:37 GMT  
		Size: 125.6 MB (125555749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2002013d5dbd37e4a82f2b4150a90cf859019c35fb14a185e420d36e205b89f0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ffaac061aeb56201c6d977ec1906a5fc4baa5702a5be2944cc50241427c60`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:bdb6e4b46792189b8fad1e275b6958153333a4c4a6fc4ffedee04ca8782db776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:c257f68d1294a261345121f7b19ee9f5adbe9d498c9ee59a0217ec4b32bdcef4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae27c54e722b70ab19e8f09c575731f8d64e7d080773041e893479cb2e01b45a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 13:19:41 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_VERSION=3.7.10
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Thu, 01 Apr 2021 13:20:11 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.10-1_amd64.deb
# Thu, 01 Apr 2021 13:20:12 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb
# Thu, 01 Apr 2021 13:20:12 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.10-1_amd64.deb.asc
# Thu, 01 Apr 2021 13:20:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Thu, 01 Apr 2021 13:20:34 GMT
ENV GLIBCXX_FORCE_NEW=1
# Thu, 01 Apr 2021 13:20:34 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Thu, 01 Apr 2021 13:20:34 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Thu, 01 Apr 2021 13:20:34 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Thu, 01 Apr 2021 13:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 13:20:35 GMT
EXPOSE 8529
# Thu, 01 Apr 2021 13:20:35 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cc33dc011029d5ce0c62edfbc9615a3ad61d2cdd608f5870884148343818e6`  
		Last Modified: Thu, 01 Apr 2021 13:21:37 GMT  
		Size: 125.6 MB (125555749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2002013d5dbd37e4a82f2b4150a90cf859019c35fb14a185e420d36e205b89f0`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ffaac061aeb56201c6d977ec1906a5fc4baa5702a5be2944cc50241427c60`  
		Last Modified: Thu, 01 Apr 2021 13:21:18 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
