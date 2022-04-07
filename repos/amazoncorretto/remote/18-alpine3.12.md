## `amazoncorretto:18-alpine3.12`

```console
$ docker pull amazoncorretto@sha256:420009f2c7f3067bd545c3d750d95a510bdff656c7fa91d70e8482f063efd791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:18-alpine3.12` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f6a54858ccdeac0c1e46851d572b0ed1a8d114cf8c62719f0a96e6a22b834de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195697591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6366627ffcced69d3d2079462c918e10ed260909a2ddef22ff70ae851be32b8e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Wed, 06 Apr 2022 22:20:55 GMT
ARG version=18.0.0.37.1
# Wed, 06 Apr 2022 22:21:01 GMT
# ARGS: version=18.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-18=$version-r0
# Wed, 06 Apr 2022 22:21:02 GMT
ENV LANG=C.UTF-8
# Wed, 06 Apr 2022 22:21:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 06 Apr 2022 22:21:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc110542335790ea4ad61918acf23afb1a41d94426b52030f9c3021c8ba672d7`  
		Last Modified: Wed, 06 Apr 2022 22:24:28 GMT  
		Size: 192.9 MB (192889531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
