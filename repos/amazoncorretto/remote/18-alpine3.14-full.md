## `amazoncorretto:18-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:e6a4cc26653c15d25b108240e53b2be3067860130433d6b6bf6cc1379ef6de87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:18-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6d6a877f176958cdceff66b02e5cf4722c9d1c9cffb08651a3148306c67b6a67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195713912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f12f5ca49b8c992c5345dbbcad1a86b58adec88f5ca9f3e29fd656a953de7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Wed, 06 Apr 2022 22:21:15 GMT
ARG version=18.0.0.37.1
# Wed, 06 Apr 2022 22:21:21 GMT
# ARGS: version=18.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-18=$version-r0
# Wed, 06 Apr 2022 22:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 06 Apr 2022 22:21:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 06 Apr 2022 22:21:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f95ca6c611687bcfd9898c7813e6afbb53ae66ea13e2afa9283f7f440de413`  
		Last Modified: Wed, 06 Apr 2022 22:25:26 GMT  
		Size: 192.9 MB (192895542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
