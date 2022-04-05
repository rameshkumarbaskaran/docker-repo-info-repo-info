## `amazoncorretto:8-alpine3.12-jdk`

```console
$ docker pull amazoncorretto@sha256:94e12b2ad3b5ec4ebaead050c05cb349fcc513ee8d66cde17ba9ad02be427d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.12-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d1f261ada5f1d668a21abafb970f758a177eb9ce2ee2a4fef82b076d8091019d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101918356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b0738b68d27eb5b9fc4cc18d352922d7136a18fe00f354af979c44ead992b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:49:59 GMT
ARG version=8.322.06.2
# Tue, 05 Apr 2022 03:50:08 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 05 Apr 2022 03:50:08 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:50:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 05 Apr 2022 03:50:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d82cf3d019f6b46666807ee35b464ce96bc01c5bba88f1da7e8748d60c675bd`  
		Last Modified: Tue, 05 Apr 2022 03:54:04 GMT  
		Size: 99.1 MB (99110296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
