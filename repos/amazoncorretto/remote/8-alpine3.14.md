## `amazoncorretto:8-alpine3.14`

```console
$ docker pull amazoncorretto@sha256:d6610edb8603870a573da1484f953683258721d785184365a434216a54cd0195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3a69b76d0a1f09c48ad73b95b66ab2d61e4c494c1603418a267dd8ba6d9b841b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101921804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6306565a1e2e38e419e3bbfd67c603a0322263e87ea3aa04fa5f669ce0d64d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:50:30 GMT
ARG version=8.322.06.2
# Tue, 05 Apr 2022 03:50:34 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 05 Apr 2022 03:50:35 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:50:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 05 Apr 2022 03:50:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cb197ee691637e646e8c9a26af893e2144c10b81022842501e563f886cbd72`  
		Last Modified: Tue, 05 Apr 2022 03:55:17 GMT  
		Size: 99.1 MB (99103434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
