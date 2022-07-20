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
$ docker pull arangodb@sha256:a2ce423c904b02c6f7df4dca32fcfd40518d3b57b7596dfc8e9ab91417c3270a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7` - linux; amd64

```console
$ docker pull arangodb@sha256:9bcfd24175c7fd49033cfe3a92f52ee5b4eb52ea308efc1acc150465a5191ab2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3702c6ccd27cd4ab01f683d6dd7e0b2a218f18fb5c8095e026e0d05bc212ecdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:51:00 GMT
ENV ARANGO_VERSION=3.7.18
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.18-1_amd64.deb
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:51:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:51:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:51:29 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:51:29 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:51:29 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:51:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:51:29 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:51:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8b949f9add3af891001ba5e5cab7f7c369fa0fd924c238ae89293ba37b2346`  
		Last Modified: Tue, 19 Jul 2022 22:53:12 GMT  
		Size: 132.8 MB (132809691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c53b345c161fa330489d3d8d80c96521127eff1d1ab548bee7fa65e59d9600`  
		Last Modified: Tue, 19 Jul 2022 22:52:52 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bbb48d29461b1b63a232838ab7f618d0b08336c7662d56ecf3a3e3d69cc000`  
		Last Modified: Tue, 19 Jul 2022 22:52:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.7.18`

```console
$ docker pull arangodb@sha256:a2ce423c904b02c6f7df4dca32fcfd40518d3b57b7596dfc8e9ab91417c3270a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.7.18` - linux; amd64

```console
$ docker pull arangodb@sha256:9bcfd24175c7fd49033cfe3a92f52ee5b4eb52ea308efc1acc150465a5191ab2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135630551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3702c6ccd27cd4ab01f683d6dd7e0b2a218f18fb5c8095e026e0d05bc212ecdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:51:00 GMT
ENV ARANGO_VERSION=3.7.18
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_PACKAGE=arangodb3_3.7.18-1_amd64.deb
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb
# Tue, 19 Jul 2022 22:51:01 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb37/DEBIAN/amd64/arangodb3_3.7.18-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:51:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:51:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:51:29 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:51:29 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:51:29 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:51:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:51:29 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:51:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8b949f9add3af891001ba5e5cab7f7c369fa0fd924c238ae89293ba37b2346`  
		Last Modified: Tue, 19 Jul 2022 22:53:12 GMT  
		Size: 132.8 MB (132809691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c53b345c161fa330489d3d8d80c96521127eff1d1ab548bee7fa65e59d9600`  
		Last Modified: Tue, 19 Jul 2022 22:52:52 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bbb48d29461b1b63a232838ab7f618d0b08336c7662d56ecf3a3e3d69cc000`  
		Last Modified: Tue, 19 Jul 2022 22:52:52 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8`

```console
$ docker pull arangodb@sha256:3dbee0629d174de4b202615824307cb96dfca9f75356463f8823f4cf5f3d911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8` - linux; amd64

```console
$ docker pull arangodb@sha256:c2ced007711a5fe2297b18eb305fc66198ef3219a95109c9e21a71193aed85a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193651287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ab4bc631a5f9d338b9d6edcb9c09f2a8c585191665ce2bbb4cf0a3c762796d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_VERSION=3.8.7
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.7-1_amd64.deb
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:52:01 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:52:02 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:52:02 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:52:02 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:52:02 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:52:03 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:52:03 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f90e8530fe3b2ce8f95b303007eb2197347dc94de3ae61d2dfd5ba9dd1cec74`  
		Last Modified: Tue, 19 Jul 2022 22:53:45 GMT  
		Size: 190.8 MB (190830426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c398f9c2b348ef47dc6e14fcd76a99530fb9297fd32a49c0ad2ec7665f59ed3`  
		Last Modified: Tue, 19 Jul 2022 22:53:21 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe08c8940f3c539c5f01fa6fa2bb102375f37eff69df00f525c76cab451f65`  
		Last Modified: Tue, 19 Jul 2022 22:53:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.8.7`

```console
$ docker pull arangodb@sha256:3dbee0629d174de4b202615824307cb96dfca9f75356463f8823f4cf5f3d911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.8.7` - linux; amd64

```console
$ docker pull arangodb@sha256:c2ced007711a5fe2297b18eb305fc66198ef3219a95109c9e21a71193aed85a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193651287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ab4bc631a5f9d338b9d6edcb9c09f2a8c585191665ce2bbb4cf0a3c762796d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_VERSION=3.8.7
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_PACKAGE=arangodb3_3.8.7-1_amd64.deb
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb
# Tue, 19 Jul 2022 22:51:34 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb38/DEBIAN/amd64/arangodb3_3.8.7-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:52:01 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:52:02 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:52:02 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:52:02 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:52:02 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:52:03 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:52:03 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f90e8530fe3b2ce8f95b303007eb2197347dc94de3ae61d2dfd5ba9dd1cec74`  
		Last Modified: Tue, 19 Jul 2022 22:53:45 GMT  
		Size: 190.8 MB (190830426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c398f9c2b348ef47dc6e14fcd76a99530fb9297fd32a49c0ad2ec7665f59ed3`  
		Last Modified: Tue, 19 Jul 2022 22:53:21 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe08c8940f3c539c5f01fa6fa2bb102375f37eff69df00f525c76cab451f65`  
		Last Modified: Tue, 19 Jul 2022 22:53:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:ff91fb0eb65e54f94113fc809abaf40a2314afd37d7f3390c69ca3158629ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:7ff7eba5c52bc6c1d45e4c1fd1d2a52dce3929bcd70ce76177afb3feb3f08475
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199284961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13efe616d4f290f5c7f610d18e09168e7dd8afa233baabb8412689813bb37abc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_VERSION=3.9.2
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.2-1_amd64.deb
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:52:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:52:35 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:52:35 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:52:35 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:52:35 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:52:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:52:35 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:52:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb2d982ee8b9fc9aaac9c63a5c5dd5ff96f13a9dbacc643fa5a93f5b4172d5`  
		Last Modified: Tue, 19 Jul 2022 22:54:18 GMT  
		Size: 196.5 MB (196464101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf15badb46721b42eda13179cd39f033c9fcc6323e050d605f6c9b0175170c5`  
		Last Modified: Tue, 19 Jul 2022 22:53:55 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0989fbd140348b6d075e05098fadb3a7834b30611c60276973d57aad5cfbe114`  
		Last Modified: Tue, 19 Jul 2022 22:53:55 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.2`

```console
$ docker pull arangodb@sha256:ff91fb0eb65e54f94113fc809abaf40a2314afd37d7f3390c69ca3158629ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.2` - linux; amd64

```console
$ docker pull arangodb@sha256:7ff7eba5c52bc6c1d45e4c1fd1d2a52dce3929bcd70ce76177afb3feb3f08475
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199284961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13efe616d4f290f5c7f610d18e09168e7dd8afa233baabb8412689813bb37abc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_VERSION=3.9.2
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.2-1_amd64.deb
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:52:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:52:35 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:52:35 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:52:35 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:52:35 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:52:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:52:35 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:52:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb2d982ee8b9fc9aaac9c63a5c5dd5ff96f13a9dbacc643fa5a93f5b4172d5`  
		Last Modified: Tue, 19 Jul 2022 22:54:18 GMT  
		Size: 196.5 MB (196464101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf15badb46721b42eda13179cd39f033c9fcc6323e050d605f6c9b0175170c5`  
		Last Modified: Tue, 19 Jul 2022 22:53:55 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0989fbd140348b6d075e05098fadb3a7834b30611c60276973d57aad5cfbe114`  
		Last Modified: Tue, 19 Jul 2022 22:53:55 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:ff91fb0eb65e54f94113fc809abaf40a2314afd37d7f3390c69ca3158629ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:7ff7eba5c52bc6c1d45e4c1fd1d2a52dce3929bcd70ce76177afb3feb3f08475
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.3 MB (199284961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13efe616d4f290f5c7f610d18e09168e7dd8afa233baabb8412689813bb37abc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:18 GMT
ADD file:80b46be2fe86b402518b00758ff5d8556d92113dc267a002b6c72a5f9c6742a3 in / 
# Tue, 19 Jul 2022 22:20:18 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 22:51:00 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_VERSION=3.9.2
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.2-1_amd64.deb
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb
# Tue, 19 Jul 2022 22:52:08 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.2-1_amd64.deb.asc
# Tue, 19 Jul 2022 22:52:33 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 19 Jul 2022 22:52:35 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 19 Jul 2022 22:52:35 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 19 Jul 2022 22:52:35 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 19 Jul 2022 22:52:35 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 19 Jul 2022 22:52:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Jul 2022 22:52:35 GMT
EXPOSE 8529
# Tue, 19 Jul 2022 22:52:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:decfdc335d9bae9ca06166e1a4fc2cdf8c2344a42d85c8a1d3f964aab59ecff5`  
		Last Modified: Tue, 19 Jul 2022 22:20:55 GMT  
		Size: 2.8 MB (2818512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb2d982ee8b9fc9aaac9c63a5c5dd5ff96f13a9dbacc643fa5a93f5b4172d5`  
		Last Modified: Tue, 19 Jul 2022 22:54:18 GMT  
		Size: 196.5 MB (196464101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf15badb46721b42eda13179cd39f033c9fcc6323e050d605f6c9b0175170c5`  
		Last Modified: Tue, 19 Jul 2022 22:53:55 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0989fbd140348b6d075e05098fadb3a7834b30611c60276973d57aad5cfbe114`  
		Last Modified: Tue, 19 Jul 2022 22:53:55 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
