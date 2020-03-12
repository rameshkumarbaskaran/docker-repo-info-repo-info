## `arangodb:latest`

```console
$ docker pull arangodb@sha256:60e34a105dc96a3feed9e4587defa8b2ef5cd708c031c57818888f3f2c171ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:6d767db42f4e172e232be9b5f7558098a72a25fdf93347d7972ba8d478eba168
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110403610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9444c3cbb5ba2bef95351b0d6e5965fa6c542eab24a7f907109e1d1c7add5d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:20 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_VERSION=3.6.2
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE=arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb
# Wed, 11 Mar 2020 22:19:43 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb36/DEBIAN/amd64/arangodb3_3.6.2-1_amd64.deb.asc
# Wed, 11 Mar 2020 22:20:06 GMT
RUN apk add --no-cache gnupg pwgen nodejs npm binutils numactl numactl-tools &&     npm install -g foxx-cli &&     rm -rf /root/.npm &&     gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B &&     mkdir /docker-entrypoint-initdb.d &&     cd /tmp                                &&     wget ${ARANGO_SIGNATURE_URL}           &&     wget ${ARANGO_PACKAGE_URL}             &&     gpg --verify ${ARANGO_PACKAGE}.asc     &&     ar x ${ARANGO_PACKAGE} data.tar.gz     &&     tar -C / -x -z -f data.tar.gz          &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=\s*).*!\1 -!'         -e 's!^\s*uid\s*=.*!!'         /etc/arangodb3/arangod.conf        &&     echo chgrp -R 0 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     echo chmod -R 775 /var/lib/arangodb3 /var/lib/arangodb3-apps &&     rm -f /usr/bin/foxx &&     rm -f ${ARANGO_PACKAGE}* data.tar.gz &&     apk del gnupg
# Wed, 11 Mar 2020 22:20:06 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Wed, 11 Mar 2020 22:20:06 GMT
COPY file:912d8c5e20cd837dbed0bf2608b1376ffffdd2d6de3e5b0af4cc869508443235 in /entrypoint.sh 
# Wed, 11 Mar 2020 22:20:07 GMT
COPY file:62d691f3a389929940df44ad84590c9019bdc0c8ce47667d5eb5dab0b2e66954 in /usr/bin/foxx 
# Wed, 11 Mar 2020 22:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2020 22:20:07 GMT
EXPOSE 8529
# Wed, 11 Mar 2020 22:20:07 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07085b9d9386b54af56ada05173b099ef139c3c914726899b2227989e71b587b`  
		Last Modified: Wed, 11 Mar 2020 22:20:35 GMT  
		Size: 107.6 MB (107614200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d915dc20c3286fedbc6b41419a943c6e153bc27324725b9064972b921a12a3d8`  
		Last Modified: Wed, 11 Mar 2020 22:20:17 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a8b8b82fc6d9f4264ea4116370f359195a8fa697d5a313e46284009990742e`  
		Last Modified: Wed, 11 Mar 2020 22:20:16 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
