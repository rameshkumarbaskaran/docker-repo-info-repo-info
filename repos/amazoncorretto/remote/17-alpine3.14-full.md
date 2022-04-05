## `amazoncorretto:17-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:284a2aed9416710fdd652ffc82862fc7d7953156fc79ae7a854087d0b30b7dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7ea30746841911b584913d828c26a1d9e44eada486a1b170816506773664c65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194632778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d534cbe1910d7dbb84c7dcb8dd25d3d99dbbac37550cba358d12d8f035d783a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:52:13 GMT
ARG version=17.0.2.8.1
# Tue, 05 Apr 2022 03:52:19 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 05 Apr 2022 03:52:20 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:52:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 05 Apr 2022 03:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8313d9ff2a6eaee8ce99c1fc2d144df716281b4baee4255311ef78515c6a5363`  
		Last Modified: Tue, 05 Apr 2022 03:59:50 GMT  
		Size: 191.8 MB (191814408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
