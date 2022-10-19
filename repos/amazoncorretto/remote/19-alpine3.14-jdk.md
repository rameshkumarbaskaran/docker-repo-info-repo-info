## `amazoncorretto:19-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:b370e3d925a38b64641d11009a3573ea9bf8d6c91c2534fbc73effb544cc208f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d0e22ead546cf76825e9f63a9c84eb884ca3b20fdfd1514ac3b56e5f1eef9787
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203305542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d001c7f5f7e6a05f361f5a1699027a63362be7e99092eb91b80816a424dfbe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:41:15 GMT
ARG version=19.0.1.10.1
# Tue, 18 Oct 2022 23:41:21 GMT
# ARGS: version=19.0.1.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Tue, 18 Oct 2022 23:41:22 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:41:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:41:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bb707b875867c945a6765c1a64bd306fd94a4f229c89d76d56b326588da0bb`  
		Last Modified: Tue, 18 Oct 2022 23:53:15 GMT  
		Size: 200.5 MB (200478053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
