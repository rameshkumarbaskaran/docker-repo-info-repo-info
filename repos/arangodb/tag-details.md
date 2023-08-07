<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `arangodb`

-	[`arangodb:3.10`](#arangodb310)
-	[`arangodb:3.10.9`](#arangodb3109)
-	[`arangodb:3.11`](#arangodb311)
-	[`arangodb:3.11.2`](#arangodb3112)
-	[`arangodb:3.9`](#arangodb39)
-	[`arangodb:3.9.11`](#arangodb3911)
-	[`arangodb:latest`](#arangodblatest)

## `arangodb:3.10`

```console
$ docker pull arangodb@sha256:d31acec323d70311e992042d4af5710777786f1f8f08ac4c7d6eee80e0fd8d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10` - linux; amd64

```console
$ docker pull arangodb@sha256:310b6d8268fadc6557c46b266437f2e7496cb44a79fc4cf0faf1d99da7819fbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222904344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e56c0b89097fe9595310ac7119844cb927e4f76fcd524db953d42b7876ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:01:27 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 07 Aug 2023 20:01:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:55 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:56 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfb353c2d433d13c258b1a4ad24b6ce16694443fbd594328da0131822ecdc35`  
		Last Modified: Mon, 07 Aug 2023 20:03:45 GMT  
		Size: 220.1 MB (220094174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe1b4b844b88b7e7731d5deac2a85779daee0d8b76944568f090ec1bb7ff277`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e98312f4b0d01c451524b8916a36988db15bfebec2e31f992b420e6ffc219b`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c712065c4acd1d8a2f34e4e44e40e49daacabaeb5fb47bd8fdbea4fd6f7c066`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:ee9b1cad489a7d05e51db9354070db37e5d8d0e230682df9b99b733da2d0bc3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217859342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c9532ee5bd8b58f040e564ece00d930b2de6906dccbf0d2e447f421a32e4fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 10 Jul 2023 19:39:17 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 10 Jul 2023 19:39:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 10 Jul 2023 19:39:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 10 Jul 2023 19:39:48 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 10 Jul 2023 19:39:48 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 10 Jul 2023 19:39:48 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 10 Jul 2023 19:39:48 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 10 Jul 2023 19:39:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 19:39:48 GMT
EXPOSE 8529
# Mon, 10 Jul 2023 19:39:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a69ab09321d2555da86ff5235ae5645bc92db687e5a09f1b9686d6902d7a3c4`  
		Last Modified: Mon, 10 Jul 2023 19:40:16 GMT  
		Size: 215.1 MB (215148949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b1bb5c343da526b7273d9d568c7b161b8659bab0ca31ac3478b8ce58be384`  
		Last Modified: Mon, 10 Jul 2023 19:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecb57c5abcda6337811fca7047d7ed21241c76cb69064fdddad38ee2dbb5d89`  
		Last Modified: Mon, 10 Jul 2023 19:39:59 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e94da9fcb108119d240d63e8586512168c38ec3714b9554ba807160ec20e4e`  
		Last Modified: Mon, 10 Jul 2023 19:39:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.10.9`

```console
$ docker pull arangodb@sha256:d31acec323d70311e992042d4af5710777786f1f8f08ac4c7d6eee80e0fd8d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.10.9` - linux; amd64

```console
$ docker pull arangodb@sha256:310b6d8268fadc6557c46b266437f2e7496cb44a79fc4cf0faf1d99da7819fbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222904344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e56c0b89097fe9595310ac7119844cb927e4f76fcd524db953d42b7876ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:01:27 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 07 Aug 2023 20:01:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:55 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:55 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:55 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:56 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfb353c2d433d13c258b1a4ad24b6ce16694443fbd594328da0131822ecdc35`  
		Last Modified: Mon, 07 Aug 2023 20:03:45 GMT  
		Size: 220.1 MB (220094174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe1b4b844b88b7e7731d5deac2a85779daee0d8b76944568f090ec1bb7ff277`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e98312f4b0d01c451524b8916a36988db15bfebec2e31f992b420e6ffc219b`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c712065c4acd1d8a2f34e4e44e40e49daacabaeb5fb47bd8fdbea4fd6f7c066`  
		Last Modified: Mon, 07 Aug 2023 20:03:21 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.10.9` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:ee9b1cad489a7d05e51db9354070db37e5d8d0e230682df9b99b733da2d0bc3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217859342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c9532ee5bd8b58f040e564ece00d930b2de6906dccbf0d2e447f421a32e4fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 10 Jul 2023 19:39:17 GMT
ENV ARANGO_VERSION=3.10.9
# Mon, 10 Jul 2023 19:39:44 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 10 Jul 2023 19:39:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 10 Jul 2023 19:39:48 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 10 Jul 2023 19:39:48 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 10 Jul 2023 19:39:48 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 10 Jul 2023 19:39:48 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 10 Jul 2023 19:39:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 19:39:48 GMT
EXPOSE 8529
# Mon, 10 Jul 2023 19:39:48 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a69ab09321d2555da86ff5235ae5645bc92db687e5a09f1b9686d6902d7a3c4`  
		Last Modified: Mon, 10 Jul 2023 19:40:16 GMT  
		Size: 215.1 MB (215148949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b1bb5c343da526b7273d9d568c7b161b8659bab0ca31ac3478b8ce58be384`  
		Last Modified: Mon, 10 Jul 2023 19:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecb57c5abcda6337811fca7047d7ed21241c76cb69064fdddad38ee2dbb5d89`  
		Last Modified: Mon, 10 Jul 2023 19:39:59 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e94da9fcb108119d240d63e8586512168c38ec3714b9554ba807160ec20e4e`  
		Last Modified: Mon, 10 Jul 2023 19:39:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11`

```console
$ docker pull arangodb@sha256:c15a80335815de203cb90a6c2855e0c53077a9ac4a1e6ef2dce4344cdedf11fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11` - linux; amd64

```console
$ docker pull arangodb@sha256:812a1206d67f66168693fc5e4fb1399435794313813b87591c678aee905ee06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246722206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5d5f1b8579c3574571e6b485e98799d84183f57a281a33d7f11c763e133a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:02:01 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:02:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:02:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:02:29 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:02:30 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:02:30 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:02:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc4946923e5d7adbb0fe4fff8085210bb5f6c986dacde641a23e1cc014fed`  
		Last Modified: Mon, 07 Aug 2023 20:04:20 GMT  
		Size: 243.9 MB (243912038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47975cfa4e68060e2784b6ce179913a193de0831e78bc1cc9a8303f9c8cc4f6a`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44872a0add811d36f568676fe17c641abb9cfba7f4661700002d9f84d958fa`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576a3b295402a9f35f5d633d7f0d720e9e97d7284a36eed08a7f29f4df6e93af`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:400a804495df0d3ab993f5c8b541c8878dd4dbb4230ca5194e9dfc039e80a39a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241149200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c253a0d581d3a829be46ddb0102beaf84ef473ea104b338dece7b6eb10545b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 26 Jul 2023 23:39:15 GMT
ENV ARANGO_VERSION=3.11.2
# Wed, 26 Jul 2023 23:39:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 26 Jul 2023 23:39:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 26 Jul 2023 23:39:47 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 26 Jul 2023 23:39:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 26 Jul 2023 23:39:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 26 Jul 2023 23:39:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 26 Jul 2023 23:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jul 2023 23:39:47 GMT
EXPOSE 8529
# Wed, 26 Jul 2023 23:39:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acd0c32bf8ae36e4386be6d901ffaf04e9ee2443dcfb98f9331b45a470254ee`  
		Last Modified: Wed, 26 Jul 2023 23:40:21 GMT  
		Size: 238.4 MB (238438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d289fc3f9dd066fde0894dbb9cfe9af54b0c13c8f69b18785fcfafbabb6d2aae`  
		Last Modified: Wed, 26 Jul 2023 23:40:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf406cf179d67842a4e5ff36c0cdbdeb7e7c44cc43d808158e1a15c24951a7e`  
		Last Modified: Wed, 26 Jul 2023 23:40:02 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bca0a2ed01ea538464d28fbfcaecaf40b547422fbbad643eda00de2f89bed1c`  
		Last Modified: Wed, 26 Jul 2023 23:40:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.11.2`

```console
$ docker pull arangodb@sha256:c15a80335815de203cb90a6c2855e0c53077a9ac4a1e6ef2dce4344cdedf11fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:3.11.2` - linux; amd64

```console
$ docker pull arangodb@sha256:812a1206d67f66168693fc5e4fb1399435794313813b87591c678aee905ee06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246722206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5d5f1b8579c3574571e6b485e98799d84183f57a281a33d7f11c763e133a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:02:01 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:02:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:02:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:02:29 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:02:30 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:02:30 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:02:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc4946923e5d7adbb0fe4fff8085210bb5f6c986dacde641a23e1cc014fed`  
		Last Modified: Mon, 07 Aug 2023 20:04:20 GMT  
		Size: 243.9 MB (243912038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47975cfa4e68060e2784b6ce179913a193de0831e78bc1cc9a8303f9c8cc4f6a`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44872a0add811d36f568676fe17c641abb9cfba7f4661700002d9f84d958fa`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576a3b295402a9f35f5d633d7f0d720e9e97d7284a36eed08a7f29f4df6e93af`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:3.11.2` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:400a804495df0d3ab993f5c8b541c8878dd4dbb4230ca5194e9dfc039e80a39a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241149200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c253a0d581d3a829be46ddb0102beaf84ef473ea104b338dece7b6eb10545b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 26 Jul 2023 23:39:15 GMT
ENV ARANGO_VERSION=3.11.2
# Wed, 26 Jul 2023 23:39:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 26 Jul 2023 23:39:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 26 Jul 2023 23:39:47 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 26 Jul 2023 23:39:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 26 Jul 2023 23:39:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 26 Jul 2023 23:39:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 26 Jul 2023 23:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jul 2023 23:39:47 GMT
EXPOSE 8529
# Wed, 26 Jul 2023 23:39:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acd0c32bf8ae36e4386be6d901ffaf04e9ee2443dcfb98f9331b45a470254ee`  
		Last Modified: Wed, 26 Jul 2023 23:40:21 GMT  
		Size: 238.4 MB (238438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d289fc3f9dd066fde0894dbb9cfe9af54b0c13c8f69b18785fcfafbabb6d2aae`  
		Last Modified: Wed, 26 Jul 2023 23:40:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf406cf179d67842a4e5ff36c0cdbdeb7e7c44cc43d808158e1a15c24951a7e`  
		Last Modified: Wed, 26 Jul 2023 23:40:02 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bca0a2ed01ea538464d28fbfcaecaf40b547422fbbad643eda00de2f89bed1c`  
		Last Modified: Wed, 26 Jul 2023 23:40:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9`

```console
$ docker pull arangodb@sha256:48444fecfbd47c46b39273e285eabfd0d4bc38c0e663cf290f9859fb1258dd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9` - linux; amd64

```console
$ docker pull arangodb@sha256:b684ee4696aaa277213b729dbfc97523c069b30adb27d6f3c083f3362715ff13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a828c1780a3534212e7e84822bda377579c8c05f4aaaebf925a95074089f5809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:00:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_VERSION=3.9.11
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Mon, 07 Aug 2023 20:01:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:23 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:23 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c566ea949470dfa5a39d8cbab7a2eeaac8bcea317ac08e61baab3ab187f0d7`  
		Last Modified: Mon, 07 Aug 2023 20:03:11 GMT  
		Size: 202.4 MB (202430564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76fe7b5c0012d15f8beb4f1bb4e1f8e8e6b84c6b380586a6692649ce4f84b`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e2ece5d15da38fd51256f56856f25ff1fd57932f14ee1ab28d79fbab87fdd`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04056651227117636854c720f1abe7d7b7a1e360324af9e192bed188a33cbc40`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:3.9.11`

```console
$ docker pull arangodb@sha256:48444fecfbd47c46b39273e285eabfd0d4bc38c0e663cf290f9859fb1258dd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:3.9.11` - linux; amd64

```console
$ docker pull arangodb@sha256:b684ee4696aaa277213b729dbfc97523c069b30adb27d6f3c083f3362715ff13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205259056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a828c1780a3534212e7e84822bda377579c8c05f4aaaebf925a95074089f5809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:00:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_VERSION=3.9.11
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE=arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb
# Mon, 07 Aug 2023 20:00:53 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb39/DEBIAN/amd64/arangodb3_3.9.11-1_amd64.deb.asc
# Mon, 07 Aug 2023 20:01:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:01:22 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:01:23 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:01:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:01:23 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:01:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:01:23 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:01:23 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c566ea949470dfa5a39d8cbab7a2eeaac8bcea317ac08e61baab3ab187f0d7`  
		Last Modified: Mon, 07 Aug 2023 20:03:11 GMT  
		Size: 202.4 MB (202430564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76fe7b5c0012d15f8beb4f1bb4e1f8e8e6b84c6b380586a6692649ce4f84b`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e2ece5d15da38fd51256f56856f25ff1fd57932f14ee1ab28d79fbab87fdd`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04056651227117636854c720f1abe7d7b7a1e360324af9e192bed188a33cbc40`  
		Last Modified: Mon, 07 Aug 2023 20:02:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `arangodb:latest`

```console
$ docker pull arangodb@sha256:c15a80335815de203cb90a6c2855e0c53077a9ac4a1e6ef2dce4344cdedf11fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:812a1206d67f66168693fc5e4fb1399435794313813b87591c678aee905ee06d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246722206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5d5f1b8579c3574571e6b485e98799d84183f57a281a33d7f11c763e133a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:01:27 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 07 Aug 2023 20:02:01 GMT
ENV ARANGO_VERSION=3.11.2
# Mon, 07 Aug 2023 20:02:27 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Mon, 07 Aug 2023 20:02:29 GMT
ENV GLIBCXX_FORCE_NEW=1
# Mon, 07 Aug 2023 20:02:29 GMT
RUN echo "UTC" > /etc/timezone
# Mon, 07 Aug 2023 20:02:30 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Mon, 07 Aug 2023 20:02:30 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Mon, 07 Aug 2023 20:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 20:02:30 GMT
EXPOSE 8529
# Mon, 07 Aug 2023 20:02:30 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc4946923e5d7adbb0fe4fff8085210bb5f6c986dacde641a23e1cc014fed`  
		Last Modified: Mon, 07 Aug 2023 20:04:20 GMT  
		Size: 243.9 MB (243912038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47975cfa4e68060e2784b6ce179913a193de0831e78bc1cc9a8303f9c8cc4f6a`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb44872a0add811d36f568676fe17c641abb9cfba7f4661700002d9f84d958fa`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576a3b295402a9f35f5d633d7f0d720e9e97d7284a36eed08a7f29f4df6e93af`  
		Last Modified: Mon, 07 Aug 2023 20:03:54 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `arangodb:latest` - linux; arm64 variant v8

```console
$ docker pull arangodb@sha256:400a804495df0d3ab993f5c8b541c8878dd4dbb4230ca5194e9dfc039e80a39a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241149200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c253a0d581d3a829be46ddb0102beaf84ef473ea104b338dece7b6eb10545b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:45:26 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 26 Jul 2023 23:39:15 GMT
ENV ARANGO_VERSION=3.11.2
# Wed, 26 Jul 2023 23:39:42 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.1.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb311/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 26 Jul 2023 23:39:47 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 26 Jul 2023 23:39:47 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 26 Jul 2023 23:39:47 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 26 Jul 2023 23:39:47 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 26 Jul 2023 23:39:47 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 26 Jul 2023 23:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jul 2023 23:39:47 GMT
EXPOSE 8529
# Wed, 26 Jul 2023 23:39:47 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acd0c32bf8ae36e4386be6d901ffaf04e9ee2443dcfb98f9331b45a470254ee`  
		Last Modified: Wed, 26 Jul 2023 23:40:21 GMT  
		Size: 238.4 MB (238438807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d289fc3f9dd066fde0894dbb9cfe9af54b0c13c8f69b18785fcfafbabb6d2aae`  
		Last Modified: Wed, 26 Jul 2023 23:40:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf406cf179d67842a4e5ff36c0cdbdeb7e7c44cc43d808158e1a15c24951a7e`  
		Last Modified: Wed, 26 Jul 2023 23:40:02 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bca0a2ed01ea538464d28fbfcaecaf40b547422fbbad643eda00de2f89bed1c`  
		Last Modified: Wed, 26 Jul 2023 23:40:03 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
