## `amazoncorretto:11-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:0ad6abc312d69086906b6785645676022268f1c593ec9506569c20888acaa9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8cc8efc89a42efe80dcc350bb9dd3fd58a67919355e58ec20b11fcacdaad0952
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196281852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f99eb96c59a27759604d690bccebb39472fbb6c9e1ec948b424313b8044a69`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:24:36 GMT
ARG version=11.0.14.9.1
# Tue, 29 Mar 2022 05:24:42 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 29 Mar 2022 05:24:43 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:24:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:24:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb67efdf923d0cc25b223ebc439fe9e991be768f8260348909c6fe1beea0e1e2`  
		Last Modified: Tue, 29 Mar 2022 05:30:46 GMT  
		Size: 193.5 MB (193463498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
