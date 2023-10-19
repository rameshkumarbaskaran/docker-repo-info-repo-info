## `amazoncorretto:11-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:bdbd7706e56429d591a699a65d59e716607ec55cbc13c2024f28d426ca5615b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce5add67b7993f4beaf8d74ee07f89e374d9de2931f3d96ad80bc717632c3d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144201151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5a17fa41d93c8e932934b9f6553d6cad887164c0d1783046020682049524dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2023 22:26:26 GMT
ARG version=11.0.20.9.1
# Fri, 08 Sep 2023 22:26:31 GMT
# ARGS: version=11.0.20.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Fri, 08 Sep 2023 22:26:32 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 22:26:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 Sep 2023 22:26:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b15319ab4fdf41ae611cb74aaa89a7720b25f8d82fcb69590e9a1c8306c2cc6`  
		Last Modified: Fri, 08 Sep 2023 22:37:03 GMT  
		Size: 141.4 MB (141375145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.15-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dafc12a6d062a1ec0deafe1309f07522d991a1d3d8e5d39a280cb150dc2f9265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142462868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7caa1dcf2a01f17b7c570f9d88bf233faf64bad4979c0c4170126250382237`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:44:15 GMT
ARG version=11.0.21.9.1
# Thu, 19 Oct 2023 00:44:20 GMT
# ARGS: version=11.0.21.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:44:21 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:44:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:44:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f744592dadb81776d72743161b21943c28cdb90885c8d0e0ce1f3d462847092f`  
		Last Modified: Thu, 19 Oct 2023 00:58:42 GMT  
		Size: 139.7 MB (139742000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
