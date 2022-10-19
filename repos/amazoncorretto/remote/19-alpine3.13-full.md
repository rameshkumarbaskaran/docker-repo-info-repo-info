## `amazoncorretto:19-alpine3.13-full`

```console
$ docker pull amazoncorretto@sha256:ef798e476cd47e8973eb94709a79f1835c1a33ce70e0e9cca676f7796533733f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.13-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:afb5c1014444a47a6b5e468137b6ce31ab87c33e21f757fc7333a2b8b6205a01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203302280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cbb5f9c87b4de71142bc6bc4298f7e9954b371a1540c0bca8d257584dc340f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:41:05 GMT
ARG version=19.0.1.10.1
# Tue, 18 Oct 2022 23:41:11 GMT
# ARGS: version=19.0.1.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Tue, 18 Oct 2022 23:41:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:41:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:41:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7822e5660e6242e215c864f0364ef56463835c604cf0f1799f86bb4b97715bd`  
		Last Modified: Tue, 18 Oct 2022 23:52:46 GMT  
		Size: 200.5 MB (200474709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
