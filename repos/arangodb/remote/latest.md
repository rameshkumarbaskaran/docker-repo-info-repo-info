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
