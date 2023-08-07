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
