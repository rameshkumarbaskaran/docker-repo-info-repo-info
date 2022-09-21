## `amazoncorretto:19-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:c075999f677410ef0748ebb97cae66045553bc79b023644746356aec741e3a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:649b83840385a386dd5b9bff82a553dea1eee1bb26cc142228ca192499eabc75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203042367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83017100b5dabaa563f097c84c3dc0ab12368ea0805b5779ac235106d41c84ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 20 Sep 2022 23:21:00 GMT
ARG version=19.0.0.36.1
# Tue, 20 Sep 2022 23:21:06 GMT
# ARGS: version=19.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Tue, 20 Sep 2022 23:21:06 GMT
ENV LANG=C.UTF-8
# Tue, 20 Sep 2022 23:21:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Sep 2022 23:21:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb77665ccf5e768481f267edb10bac6fd14fdd978e96f8d71e509020f608731c`  
		Last Modified: Tue, 20 Sep 2022 23:24:53 GMT  
		Size: 200.2 MB (200214878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
