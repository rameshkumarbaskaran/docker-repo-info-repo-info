<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.15`](#arangodb3715)
-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.2`](#arangodb382)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:dab1a123540bf619fc633448397608eb426ac74f1cedfa6a1d8131fde9818673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:3a6075adb369507232dc386a06449dbd0c1993bbbbfd98e6eef50965576d407a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129647710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb8742bf48e4747d75f9c2c6d43325e29987c5121e956979d366ed4ab0e49e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:41:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Sep 2021 19:19:24 GMT
ENV ARANGO_VERSION=3.7.15
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.15-1_amd64.deb
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.15-1_amd64.deb
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.15-1_amd64.deb.asc
# Wed, 29 Sep 2021 19:19:52 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 29 Sep 2021 19:19:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Sep 2021 19:19:54 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Sep 2021 19:19:54 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 29 Sep 2021 19:19:54 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 29 Sep 2021 19:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Sep 2021 19:19:54 GMT
EXPOSE 8529
# Wed, 29 Sep 2021 19:19:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da5e56e1337834c93d73256021b25db5992ef0b723499b6d268b274ad2e1e53`  
		Last Modified: Wed, 29 Sep 2021 19:20:31 GMT  
		Size: 126.8 MB (126828055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdd08b8185822d888b0dcfeb24885c3a94717436bd0b3865fabbab4f35b4892`  
		Last Modified: Wed, 29 Sep 2021 19:20:13 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee31965a3011f572d6c9187fa3ef7d6f64d8176fa94dfce026795a373ce9525`  
		Last Modified: Wed, 29 Sep 2021 19:20:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.15`

```console
$ docker pull arangodb@sha256:dab1a123540bf619fc633448397608eb426ac74f1cedfa6a1d8131fde9818673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7.15` - linux; amd64

```console
$ docker pull arangodb@sha256:3a6075adb369507232dc386a06449dbd0c1993bbbbfd98e6eef50965576d407a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129647710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb8742bf48e4747d75f9c2c6d43325e29987c5121e956979d366ed4ab0e49e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:41:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 29 Sep 2021 19:19:24 GMT
ENV ARANGO_VERSION=3.7.15
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.15-1_amd64.deb
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.15-1_amd64.deb
# Wed, 29 Sep 2021 19:19:25 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.15-1_amd64.deb.asc
# Wed, 29 Sep 2021 19:19:52 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 29 Sep 2021 19:19:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 29 Sep 2021 19:19:54 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 29 Sep 2021 19:19:54 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 29 Sep 2021 19:19:54 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 29 Sep 2021 19:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Sep 2021 19:19:54 GMT
EXPOSE 8529
# Wed, 29 Sep 2021 19:19:55 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da5e56e1337834c93d73256021b25db5992ef0b723499b6d268b274ad2e1e53`  
		Last Modified: Wed, 29 Sep 2021 19:20:31 GMT  
		Size: 126.8 MB (126828055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdd08b8185822d888b0dcfeb24885c3a94717436bd0b3865fabbab4f35b4892`  
		Last Modified: Wed, 29 Sep 2021 19:20:13 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee31965a3011f572d6c9187fa3ef7d6f64d8176fa94dfce026795a373ce9525`  
		Last Modified: Wed, 29 Sep 2021 19:20:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:a0e0d5b7247cbaa867eccfb4ba87c46ed8bfa6516149cae6618c70b2cacba7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:abb6263e55584560b84524f5f475245ead0dd2f1a463bbdeb4d3762b542b6fbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187579306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803819368973bc9c6ddc09a77f8054a2a00e030d56cd3857866dc88ab2663773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:42:38 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_VERSION=3.8.2
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.2-1_amd64.deb
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.2-1_amd64.deb
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.2-1_amd64.deb.asc
# Mon, 01 Nov 2021 18:19:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 01 Nov 2021 18:19:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 01 Nov 2021 18:19:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 01 Nov 2021 18:19:53 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 01 Nov 2021 18:19:53 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 01 Nov 2021 18:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:19:54 GMT
EXPOSE 8529
# Mon, 01 Nov 2021 18:19:54 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98251fdaaf1f2de708332d588315b554f2227535123c400ec2d894da3f6efa40`  
		Last Modified: Mon, 01 Nov 2021 18:20:34 GMT  
		Size: 184.8 MB (184775251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb0941d326d4f72e334e913fa6120dfa2ffdf6d80e8f0ca29971837da72eaa4`  
		Last Modified: Mon, 01 Nov 2021 18:20:12 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331bfcf4d958cb10efaf73e3d3a0deca85c9b1be6a6186d45b94590e72a90fe2`  
		Last Modified: Mon, 01 Nov 2021 18:20:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.2`

```console
$ docker pull arangodb@sha256:a0e0d5b7247cbaa867eccfb4ba87c46ed8bfa6516149cae6618c70b2cacba7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.2` - linux; amd64

```console
$ docker pull arangodb@sha256:abb6263e55584560b84524f5f475245ead0dd2f1a463bbdeb4d3762b542b6fbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187579306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803819368973bc9c6ddc09a77f8054a2a00e030d56cd3857866dc88ab2663773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:42:38 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_VERSION=3.8.2
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.2-1_amd64.deb
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.2-1_amd64.deb
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.2-1_amd64.deb.asc
# Mon, 01 Nov 2021 18:19:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 01 Nov 2021 18:19:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 01 Nov 2021 18:19:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 01 Nov 2021 18:19:53 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 01 Nov 2021 18:19:53 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 01 Nov 2021 18:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:19:54 GMT
EXPOSE 8529
# Mon, 01 Nov 2021 18:19:54 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98251fdaaf1f2de708332d588315b554f2227535123c400ec2d894da3f6efa40`  
		Last Modified: Mon, 01 Nov 2021 18:20:34 GMT  
		Size: 184.8 MB (184775251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb0941d326d4f72e334e913fa6120dfa2ffdf6d80e8f0ca29971837da72eaa4`  
		Last Modified: Mon, 01 Nov 2021 18:20:12 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331bfcf4d958cb10efaf73e3d3a0deca85c9b1be6a6186d45b94590e72a90fe2`  
		Last Modified: Mon, 01 Nov 2021 18:20:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:a0e0d5b7247cbaa867eccfb4ba87c46ed8bfa6516149cae6618c70b2cacba7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:abb6263e55584560b84524f5f475245ead0dd2f1a463bbdeb4d3762b542b6fbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187579306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803819368973bc9c6ddc09a77f8054a2a00e030d56cd3857866dc88ab2663773`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:42:38 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_VERSION=3.8.2
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.2-1_amd64.deb
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.2-1_amd64.deb
# Mon, 01 Nov 2021 18:19:22 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.2-1_amd64.deb.asc
# Mon, 01 Nov 2021 18:19:51 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 01 Nov 2021 18:19:53 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 01 Nov 2021 18:19:53 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 01 Nov 2021 18:19:53 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 01 Nov 2021 18:19:53 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 01 Nov 2021 18:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:19:54 GMT
EXPOSE 8529
# Mon, 01 Nov 2021 18:19:54 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98251fdaaf1f2de708332d588315b554f2227535123c400ec2d894da3f6efa40`  
		Last Modified: Mon, 01 Nov 2021 18:20:34 GMT  
		Size: 184.8 MB (184775251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb0941d326d4f72e334e913fa6120dfa2ffdf6d80e8f0ca29971837da72eaa4`  
		Last Modified: Mon, 01 Nov 2021 18:20:12 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331bfcf4d958cb10efaf73e3d3a0deca85c9b1be6a6186d45b94590e72a90fe2`  
		Last Modified: Mon, 01 Nov 2021 18:20:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
