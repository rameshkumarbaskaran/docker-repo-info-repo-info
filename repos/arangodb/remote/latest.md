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
