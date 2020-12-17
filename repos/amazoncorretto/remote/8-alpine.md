## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:c0cee418710672eb0bf832f77505491958db377d08f946d8b9a5dac594474c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93920a42ddb25dbf5a91fbd128891eb383f22a09813bbe30cfd0b912ca139806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101779760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408df7b07ec1b2ac7817ba9a4ea4e9076db21bd598337d83c6578595a18b871f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:10 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 17 Dec 2020 00:50:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b381c2ee7bec3c1c893e503740a32e185ae03be120aefea696cccb7c05eef9e`  
		Last Modified: Thu, 17 Dec 2020 00:51:37 GMT  
		Size: 99.0 MB (98980694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
