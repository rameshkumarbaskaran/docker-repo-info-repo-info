## `amazoncorretto:8u322-alpine3.12`

```console
$ docker pull amazoncorretto@sha256:2beb3709abfebba6c8216928ec6deaf9a2dc06c90cadb09426cea44e40dd2e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.12` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bbd6edab3f62b5f8c24d97934b4581c53b0798545b6b8a82fe912982df1e0547
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101918262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324db49a8281baad10e7b3ef2a10fe8b3b499e8e55e70359eba155b99d317ff8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:50 GMT
ADD file:cbe481f8a83651395a1e84bf344472e2fa9cc3551601514e50c000f76255e938 in / 
# Tue, 29 Mar 2022 00:19:51 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:18 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:23:23 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 29 Mar 2022 05:23:23 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:23:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:23:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9c4930dab7624ba1487a3aa1f29c65f2241e7a8fae81d26e8bc66eaa4086c440`  
		Last Modified: Tue, 29 Mar 2022 00:20:53 GMT  
		Size: 2.8 MB (2807997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff9be22b04e82f6b4421933c88866ed4de4855972af08769078c29c0032a63a`  
		Last Modified: Tue, 29 Mar 2022 05:27:06 GMT  
		Size: 99.1 MB (99110265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
