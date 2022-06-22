<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.7`](#arangodb37)
-	[`arangodb:3.7.18`](#arangodb3718)
-	[`arangodb:3.8`](#arangodb38)
-	[`arangodb:3.8.7`](#arangodb387)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.2`](#arangodb392)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.7`

```console
$ docker pull arangodb@sha256:955a386d1f54adbcbc58346e18d6dcab321e73828bcb2d655c11d6c8198c8cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:f04f4d1f4cc1e2ba49ab6db86ef7b1c0cf32e00bea13e2c140783c5b275925ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135264762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58aae6df018dbb92653f2641d1ac4bedaaea29ba8d3325ab7fab1e7e5228ffc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_VERSION=3.7.18
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.18-1_amd64.deb
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb.asc
# Mon, 23 May 2022 18:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 23 May 2022 18:19:45 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 23 May 2022 18:19:45 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 23 May 2022 18:19:45 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 23 May 2022 18:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 23 May 2022 18:19:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 May 2022 18:19:46 GMT
EXPOSE 8529
# Mon, 23 May 2022 18:19:46 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af8a2fc04ddf101b97c7c70f6cbf170774eea5b26aa1d19e82d88dd1cc2160b`  
		Last Modified: Mon, 23 May 2022 18:20:22 GMT  
		Size: 132.4 MB (132444046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d637a6657ff78c581a0e34712a16646e72a7573f43d99bfec72eb019771ea57`  
		Last Modified: Mon, 23 May 2022 18:20:03 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab60af5b671ef90a24d27c0f80b85a5a7e1784143236f93147ce9bcef8c1ee`  
		Last Modified: Mon, 23 May 2022 18:20:03 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.18`

```console
$ docker pull arangodb@sha256:955a386d1f54adbcbc58346e18d6dcab321e73828bcb2d655c11d6c8198c8cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7.18` - linux; amd64

```console
$ docker pull arangodb@sha256:f04f4d1f4cc1e2ba49ab6db86ef7b1c0cf32e00bea13e2c140783c5b275925ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135264762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58aae6df018dbb92653f2641d1ac4bedaaea29ba8d3325ab7fab1e7e5228ffc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_VERSION=3.7.18
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.18-1_amd64.deb
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb
# Mon, 23 May 2022 18:19:20 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb.asc
# Mon, 23 May 2022 18:19:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 23 May 2022 18:19:45 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 23 May 2022 18:19:45 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 23 May 2022 18:19:45 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 23 May 2022 18:19:46 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 23 May 2022 18:19:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 May 2022 18:19:46 GMT
EXPOSE 8529
# Mon, 23 May 2022 18:19:46 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af8a2fc04ddf101b97c7c70f6cbf170774eea5b26aa1d19e82d88dd1cc2160b`  
		Last Modified: Mon, 23 May 2022 18:20:22 GMT  
		Size: 132.4 MB (132444046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d637a6657ff78c581a0e34712a16646e72a7573f43d99bfec72eb019771ea57`  
		Last Modified: Mon, 23 May 2022 18:20:03 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab60af5b671ef90a24d27c0f80b85a5a7e1784143236f93147ce9bcef8c1ee`  
		Last Modified: Mon, 23 May 2022 18:20:03 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:c2270201e8bbd731c218712ce0bb9cf2bf01a9d8dbfe6dae6cfe77bf98a66d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:f0402df079253b3d8bafbd6784fd206d35ba9d380f1b4828b6e706fd9751d31f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193294790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70527c50c92e4c5bf65aa5be621e76d55e9995a5b4846d24914e2792c4847de9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_VERSION=3.8.7
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.7-1_amd64.deb
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb.asc
# Tue, 07 Jun 2022 18:19:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 07 Jun 2022 18:19:43 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 07 Jun 2022 18:19:43 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 07 Jun 2022 18:19:43 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 07 Jun 2022 18:19:43 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 07 Jun 2022 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jun 2022 18:19:44 GMT
EXPOSE 8529
# Tue, 07 Jun 2022 18:19:44 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc25f35e30c47cdd4a9a21d1211c9b16a95caf85dd5b595f5637a389edd352b`  
		Last Modified: Tue, 07 Jun 2022 18:20:26 GMT  
		Size: 190.5 MB (190474073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55655019c777aad5c159cd11b3450693429aee728e22165b4e560f19c62b30`  
		Last Modified: Tue, 07 Jun 2022 18:20:04 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fbf674d595d40fb4117e242c9d4af66c18626b3c3e3f30dd0a1a1526692573`  
		Last Modified: Tue, 07 Jun 2022 18:20:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.7`

```console
$ docker pull arangodb@sha256:c2270201e8bbd731c218712ce0bb9cf2bf01a9d8dbfe6dae6cfe77bf98a66d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.7` - linux; amd64

```console
$ docker pull arangodb@sha256:f0402df079253b3d8bafbd6784fd206d35ba9d380f1b4828b6e706fd9751d31f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193294790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70527c50c92e4c5bf65aa5be621e76d55e9995a5b4846d24914e2792c4847de9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_VERSION=3.8.7
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.7-1_amd64.deb
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb
# Tue, 07 Jun 2022 18:19:17 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb.asc
# Tue, 07 Jun 2022 18:19:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 07 Jun 2022 18:19:43 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 07 Jun 2022 18:19:43 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 07 Jun 2022 18:19:43 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 07 Jun 2022 18:19:43 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 07 Jun 2022 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jun 2022 18:19:44 GMT
EXPOSE 8529
# Tue, 07 Jun 2022 18:19:44 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc25f35e30c47cdd4a9a21d1211c9b16a95caf85dd5b595f5637a389edd352b`  
		Last Modified: Tue, 07 Jun 2022 18:20:26 GMT  
		Size: 190.5 MB (190474073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e55655019c777aad5c159cd11b3450693429aee728e22165b4e560f19c62b30`  
		Last Modified: Tue, 07 Jun 2022 18:20:04 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fbf674d595d40fb4117e242c9d4af66c18626b3c3e3f30dd0a1a1526692573`  
		Last Modified: Tue, 07 Jun 2022 18:20:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:10b04b71838ed9d07ecf838c5ff5aba97041201dedcc59f2e815bac1b9b68ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:d083fbdfc789f872296e9f4126a728bb247df8337d97d4d203ba248ccebb63a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199256598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5f20cff0e4dbfe52b0d056a09caa48bdd50d79412ede97ba993038d5e179d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_VERSION=3.9.2
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.2-1_amd64.deb
# Tue, 21 Jun 2022 20:19:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb
# Tue, 21 Jun 2022 20:19:29 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb.asc
# Tue, 21 Jun 2022 20:19:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jun 2022 20:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 21 Jun 2022 20:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jun 2022 20:19:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 21 Jun 2022 20:19:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 21 Jun 2022 20:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 20:19:56 GMT
EXPOSE 8529
# Tue, 21 Jun 2022 20:19:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dd6611da6eef5f3e0ce896c3848071e38e9d4411d37e881ca15b4b51c23a2`  
		Last Modified: Tue, 21 Jun 2022 20:20:36 GMT  
		Size: 196.4 MB (196435882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2dee184353a3f6637e4993d57a6e301e960e848e247a63ccae305a4d324150`  
		Last Modified: Tue, 21 Jun 2022 20:20:14 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9225893ee77eff9a2797d98250f9d846bfca10a7e9c2bfef2caeb60dd91bbc`  
		Last Modified: Tue, 21 Jun 2022 20:20:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.2`

```console
$ docker pull arangodb@sha256:10b04b71838ed9d07ecf838c5ff5aba97041201dedcc59f2e815bac1b9b68ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.2` - linux; amd64

```console
$ docker pull arangodb@sha256:d083fbdfc789f872296e9f4126a728bb247df8337d97d4d203ba248ccebb63a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199256598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5f20cff0e4dbfe52b0d056a09caa48bdd50d79412ede97ba993038d5e179d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_VERSION=3.9.2
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.2-1_amd64.deb
# Tue, 21 Jun 2022 20:19:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb
# Tue, 21 Jun 2022 20:19:29 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb.asc
# Tue, 21 Jun 2022 20:19:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jun 2022 20:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 21 Jun 2022 20:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jun 2022 20:19:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 21 Jun 2022 20:19:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 21 Jun 2022 20:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 20:19:56 GMT
EXPOSE 8529
# Tue, 21 Jun 2022 20:19:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dd6611da6eef5f3e0ce896c3848071e38e9d4411d37e881ca15b4b51c23a2`  
		Last Modified: Tue, 21 Jun 2022 20:20:36 GMT  
		Size: 196.4 MB (196435882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2dee184353a3f6637e4993d57a6e301e960e848e247a63ccae305a4d324150`  
		Last Modified: Tue, 21 Jun 2022 20:20:14 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9225893ee77eff9a2797d98250f9d846bfca10a7e9c2bfef2caeb60dd91bbc`  
		Last Modified: Tue, 21 Jun 2022 20:20:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:10b04b71838ed9d07ecf838c5ff5aba97041201dedcc59f2e815bac1b9b68ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:d083fbdfc789f872296e9f4126a728bb247df8337d97d4d203ba248ccebb63a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199256598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5f20cff0e4dbfe52b0d056a09caa48bdd50d79412ede97ba993038d5e179d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:09:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_VERSION=3.9.2
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Tue, 21 Jun 2022 20:19:28 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.2-1_amd64.deb
# Tue, 21 Jun 2022 20:19:29 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb
# Tue, 21 Jun 2022 20:19:29 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb.asc
# Tue, 21 Jun 2022 20:19:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 21 Jun 2022 20:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 21 Jun 2022 20:19:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 21 Jun 2022 20:19:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 21 Jun 2022 20:19:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 21 Jun 2022 20:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Jun 2022 20:19:56 GMT
EXPOSE 8529
# Tue, 21 Jun 2022 20:19:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140dd6611da6eef5f3e0ce896c3848071e38e9d4411d37e881ca15b4b51c23a2`  
		Last Modified: Tue, 21 Jun 2022 20:20:36 GMT  
		Size: 196.4 MB (196435882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2dee184353a3f6637e4993d57a6e301e960e848e247a63ccae305a4d324150`  
		Last Modified: Tue, 21 Jun 2022 20:20:14 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9225893ee77eff9a2797d98250f9d846bfca10a7e9c2bfef2caeb60dd91bbc`  
		Last Modified: Tue, 21 Jun 2022 20:20:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
