## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:e75d73038b77b373f26e0af88975e7647335feabd7e6ce05558a86b5880a3d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a36b9aca0338eca668a30666aab3767dd54de7ff03ecface4789487d8fae3958
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196277904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791d6ce3a22ab66d473044ffe2099b3d38ba3b9ff7dbacaab88202567978ed16`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:24:46 GMT
ARG version=11.0.14.9.1
# Tue, 29 Mar 2022 05:24:52 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 29 Mar 2022 05:24:53 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:24:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:24:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c07312abad8919eaffec0075c3b2a76b5ca9d4f911ae9193bbf3b76944a3c50`  
		Last Modified: Tue, 29 Mar 2022 05:31:14 GMT  
		Size: 193.5 MB (193463392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
