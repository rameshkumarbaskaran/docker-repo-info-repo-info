## `amazoncorretto:11-alpine3.12-jdk`

```console
$ docker pull amazoncorretto@sha256:e366b49891d8c7b7a880e1aa0fc90ff1c3fe2222ae7c01fbe7cdc7a8d35ba926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.12-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1d7c16e4d84eea55ac6e462c7f7ec569ca449e2520b43ff5e9eb39e51323f473
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196269310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5c54e77560832614029797449f613a1d5106e9a508c61e1f644ffaf7de7169`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:50 GMT
ADD file:cbe481f8a83651395a1e84bf344472e2fa9cc3551601514e50c000f76255e938 in / 
# Tue, 29 Mar 2022 00:19:51 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:24:13 GMT
ARG version=11.0.14.9.1
# Tue, 29 Mar 2022 05:24:23 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 29 Mar 2022 05:24:24 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:24:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:24:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9c4930dab7624ba1487a3aa1f29c65f2241e7a8fae81d26e8bc66eaa4086c440`  
		Last Modified: Tue, 29 Mar 2022 00:20:53 GMT  
		Size: 2.8 MB (2807997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c960bc26b5352c172da909c25a9f2d26c61ac9a6899c55eae5f4d5a3bec100d`  
		Last Modified: Tue, 29 Mar 2022 05:29:50 GMT  
		Size: 193.5 MB (193461313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
