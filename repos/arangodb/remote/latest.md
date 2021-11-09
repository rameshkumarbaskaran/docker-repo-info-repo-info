## `arangodb:latest`

```console
$ docker pull arangodb@sha256:76c320350a8e3734ab680745f40b29b25533f19b0f44cb4bcecf4cbbcd55ea93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:3c748f97520ca35a486f508589cfee70f70b0c490cdec15bdc04ff60eb816964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187579536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769f7293da46cf89aa344250b19c440f7b667b844e70249493fbcf02548bfb16`
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
# Tue, 09 Nov 2021 00:20:21 GMT
RUN apk add --no-cache gnupg pwgen binutils numactl numactl-tools nodejs yarn &&     yarn global add foxx-cli &&     apk del yarn &&     gpg --batch --keyserver keys.openpgp.org --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Tue, 09 Nov 2021 00:20:23 GMT
ENV GLIBCXX_FORCE_NEW=1
# Tue, 09 Nov 2021 00:20:23 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 09 Nov 2021 00:20:23 GMT
COPY file:5186b735a7f691f0963e16d7add12851632ad73eceed0dc74092096025935cb4 in /entrypoint.sh 
# Tue, 09 Nov 2021 00:20:23 GMT
COPY file:e891c9dc63d937e22dc27abb45afa31518cd659993e0c54dab0f6cde8d994063 in /usr/bin/foxx 
# Tue, 09 Nov 2021 00:20:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Nov 2021 00:20:24 GMT
EXPOSE 8529
# Tue, 09 Nov 2021 00:20:24 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18189da276de9d9d58359a613143dacf7cb53fc4d27f04a78c3a77151658eab2`  
		Last Modified: Tue, 09 Nov 2021 00:21:42 GMT  
		Size: 184.8 MB (184775481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127d4d251d2e6911ce659acb405f23e5f0d46f65442302bd82c378a5c3eaa212`  
		Last Modified: Tue, 09 Nov 2021 00:21:13 GMT  
		Size: 2.1 KB (2086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556484d115ddc2840f5bafddd4498187d39b41d53a78fc66bcd6e023a4bbd108`  
		Last Modified: Tue, 09 Nov 2021 00:21:13 GMT  
		Size: 262.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
