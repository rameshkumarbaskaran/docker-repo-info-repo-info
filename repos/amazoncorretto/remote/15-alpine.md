## `amazoncorretto:15-alpine`

```console
$ docker pull amazoncorretto@sha256:20c82ab4e62bf9f91630d7841ed3c9dc943c17f5f5c94857764a2ffd54b2f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c25de619e51e7c78a486bf70808b754a3abd610411f8e1f87c8fedabf59734c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207717112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e56b0bd70ace662b71fe9d3638c944ad640bfe394dc200355bc53aef77a452a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:39 GMT
ARG version=15.0.1.9.1
# Thu, 17 Dec 2020 00:50:47 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 17 Dec 2020 00:50:47 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d14c6e3b1c71aadf5ad20b205d0c58ed6721023a96da8bb8ccaf98a9edd08`  
		Last Modified: Thu, 17 Dec 2020 00:52:52 GMT  
		Size: 204.9 MB (204918046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
