## `amazoncorretto:11-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:0f664120adb356cbfcdb12312c7c72029ced0b0546104c57826e920e5d9226a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e8bcdf170e932b80b914d962b54988ecf043a06a6dfe09ecd0742e507a9f0031
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196368258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b908c8624af45e9cf1c1fc9c137695066f0f47ff57031360f8d672aea8beea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:38:37 GMT
ARG version=11.0.17.8.1
# Tue, 18 Oct 2022 23:38:43 GMT
# ARGS: version=11.0.17.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 18 Oct 2022 23:38:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:38:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:38:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c3a21fb45d4e8f192c16a67794505f08792f917b316fb4ed45299353a97b19`  
		Last Modified: Tue, 18 Oct 2022 23:47:26 GMT  
		Size: 193.5 MB (193540687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
