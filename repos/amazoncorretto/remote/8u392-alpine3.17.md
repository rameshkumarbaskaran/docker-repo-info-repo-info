## `amazoncorretto:8u392-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:ed57dc37f9a807ff6c30c12a4455973b839a3a689dc567095209107dd376041d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazoncorretto:8u392-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:721aadf451fbe49d04e5fccd2851cf1b125bf75a7df47e695ea074b7467c80d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103063823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0cf33c59eeb93ddbd5659a3f288a8d9d65e09341cc8f14510972d0b5fecc36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:41:15 GMT
ARG version=8.392.08.1
# Thu, 19 Oct 2023 00:41:18 GMT
# ARGS: version=8.392.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:41:19 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:41:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:41:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12387dd841c0ae621772a4a15b4c0747cb75e764ff6f0291b346ef8b9d6e8c50`  
		Last Modified: Thu, 19 Oct 2023 00:55:07 GMT  
		Size: 99.8 MB (99805533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
