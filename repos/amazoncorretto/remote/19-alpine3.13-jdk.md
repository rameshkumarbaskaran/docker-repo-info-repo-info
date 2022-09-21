## `amazoncorretto:19-alpine3.13-jdk`

```console
$ docker pull amazoncorretto@sha256:38f8c9b933c5caf34d8ea7f141ec82b4d774b4875cdc34e7b2bb9bd0f7c31e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.13-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d6be0d90a21b118bc5655c703229f0272f6fc5cc9f7187df4f0b785f9f4b606a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203045626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc41ac005ae26c2b73b7163e0e9382e928c39aaf615320220990bfc31ec778ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 20 Sep 2022 23:20:50 GMT
ARG version=19.0.0.36.1
# Tue, 20 Sep 2022 23:20:56 GMT
# ARGS: version=19.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Tue, 20 Sep 2022 23:20:57 GMT
ENV LANG=C.UTF-8
# Tue, 20 Sep 2022 23:20:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Sep 2022 23:20:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043acc2bb7379bd11a1907b5afb5778b7eb80491224f500b7c50b4935be63a98`  
		Last Modified: Tue, 20 Sep 2022 23:24:24 GMT  
		Size: 200.2 MB (200218055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
