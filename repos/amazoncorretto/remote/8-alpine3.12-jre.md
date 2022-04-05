## `amazoncorretto:8-alpine3.12-jre`

```console
$ docker pull amazoncorretto@sha256:df85166186ce09753947a803bebe22d5afc4d3a9cd945b7aa7456c2c0c2b0ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.12-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:227949d4e5930d063a36dcd0635a1f72f4e3701ca8becb262c94845553c97bd5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43179762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101ccc54fb079c6202d6359629c4c5f09109f62f3b5a6e4a61d7fc8549ed1667`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:49:59 GMT
ARG version=8.322.06.2
# Tue, 05 Apr 2022 03:50:15 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 05 Apr 2022 03:50:15 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:50:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a957593fd99195047d6699e6319e02a7aaa05ea387ae5eb39edf2be25f4086`  
		Last Modified: Tue, 05 Apr 2022 03:54:22 GMT  
		Size: 40.4 MB (40371702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
