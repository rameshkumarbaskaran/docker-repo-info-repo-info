## `arangodb:latest`

```console
$ docker pull arangodb@sha256:ad8804006da97f7ed6f45e35fa573ccd3be78748970761fef91e8cd2c9f5852a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:c0d4e9df6dcd8645c3d84395fe84652b87cf8b07db363d2d5e70274f8cef3dd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218752791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d2f9a9d5c96eecd66cb16c817989e3fabe592fabcd60165237466af2d6e788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 12 Oct 2022 19:19:28 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 12 Oct 2022 19:19:28 GMT
ENV ARANGO_VERSION=3.10.0
# Wed, 12 Oct 2022 19:19:53 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli@2.0.1 &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     arch="$(apk --print-arch)"             &&     case "$arch" in                                   x86_64)  dpkgArch='amd64'          ;;         aarch64) dpkgArch='arm64'          ;;         *) echo >&2 "unsupported: $arch" && exit 1 ;;     esac                                   &&     ARANGO_URL="https://download.arangodb.com/arangodb310/DEBIAN/$dpkgArch" &&     ARANGO_PACKAGE="arangodb3_${ARANGO_VERSION}-1_${dpkgArch}.deb" &&     ARANGO_PACKAGE_URL="${ARANGO_URL}/${ARANGO_PACKAGE}" &&     ARANGO_SIGNATURE_URL="${ARANGO_PACKAGE_URL}.asc" &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 12 Oct 2022 19:19:55 GMT
ENV GLIBCXX_FORCE_NEW=1
# Wed, 12 Oct 2022 19:19:55 GMT
RUN echo "UTC" > /etc/timezone
# Wed, 12 Oct 2022 19:19:56 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 12 Oct 2022 19:19:56 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Wed, 12 Oct 2022 19:19:56 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Wed, 12 Oct 2022 19:19:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 Oct 2022 19:19:56 GMT
EXPOSE 8529
# Wed, 12 Oct 2022 19:19:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614c1b15d1f618586750750d537cb77ab74b182930266a4a1f432fd6d556e276`  
		Last Modified: Wed, 12 Oct 2022 19:20:55 GMT  
		Size: 215.9 MB (215944251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be0edb86b44826c4c52b741d7b62ad5a0a50bb46af0e6726d5ad25c6712b43e`  
		Last Modified: Wed, 12 Oct 2022 19:20:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c743a53b7ac0379787c5abb5643c79f7ce16f2c646c485c5ac347eb213a4c8`  
		Last Modified: Wed, 12 Oct 2022 19:20:14 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69f3d2d920cde77d2e955d7fae092c587aa8976f94c63e34bd79bc48188ee20`  
		Last Modified: Wed, 12 Oct 2022 19:20:14 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
