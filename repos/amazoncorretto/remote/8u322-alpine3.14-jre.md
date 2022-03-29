## `amazoncorretto:8u322-alpine3.14-jre`

```console
$ docker pull amazoncorretto@sha256:e06143a8a6c91bb85cbe99767846ff0abb99a005f88a497f6e472b2226648530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.14-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bac9c0a453789ec917cb5d407c9e048e774bf9a892e46b53afafc17b26b039ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43199377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeb8e38f47a1d923733b78b5281e2cfb1e181dce413fa67ae6f1a35a4a51de3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:44 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:23:54 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 29 Mar 2022 05:23:54 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:23:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3013be802ad6b12d16fc5c34b0d9d77fb611c4127d24c654d10819a289e24b`  
		Last Modified: Tue, 29 Mar 2022 05:28:36 GMT  
		Size: 40.4 MB (40381023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
