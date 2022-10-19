## `amazoncorretto:8-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:32e0bbeb170269f1b1cc4d3af384f79565b293948c7d0a2fb8eea1128585105e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:312fc242b73022f11660ded4059277c41049faf5652cf8f14d2f2b7e3d8737f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101626091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b316d826c5541c88d0bf2a932ded5e74eda4106112d4323c7474339bf4e6e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:37:30 GMT
ARG version=8.352.08.1
# Tue, 18 Oct 2022 23:37:34 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 18 Oct 2022 23:37:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:37:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:37:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6536cf88ba4829a1322d5c286539d47e4d0901b0df0c297a4e637da90d3a4454`  
		Last Modified: Tue, 18 Oct 2022 23:44:50 GMT  
		Size: 98.8 MB (98798602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
