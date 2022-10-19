## `amazoncorretto:8u352-alpine3.13-jre`

```console
$ docker pull amazoncorretto@sha256:bcc95745e1df2075dcc5d0b57d6465512bca0edfc57894a89d345c1f88814bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u352-alpine3.13-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1477995fe2f3129252366ff503c175d271a6e325e5dec03314cecb567aa4f705
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43258512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c5ecf5a4231ab81272c1bd9815701477195456707b29ce38969f5dd176a912`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:37:17 GMT
ARG version=8.352.08.1
# Tue, 18 Oct 2022 23:37:27 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 18 Oct 2022 23:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:37:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5fcb1c575dcce3fa4b458bf0dd2784387b2d0df182f16e8bd4f135e43ca8ec`  
		Last Modified: Tue, 18 Oct 2022 23:44:32 GMT  
		Size: 40.4 MB (40430941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
