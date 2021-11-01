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
