## `amazoncorretto:8-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:1bfabe33f80c506d2bab0247bac938baa514b28e6da418be99991c8c88b8af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:772924289a02e77424b5876ca1fd7b135d04fbb8dd3e29353193074efeccad76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101917992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449348e78d8d5cf9a53d44dcf2e7e4cdf83cbb5504306da6ca0bc99a8620f1a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:57 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:24:01 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 29 Mar 2022 05:24:01 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:24:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:24:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2acd6ebf440bf9e3bf1669cf9ad18155dc6d2f9581c270fa22ddd4aa267a773`  
		Last Modified: Tue, 29 Mar 2022 05:28:54 GMT  
		Size: 99.1 MB (99103480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
