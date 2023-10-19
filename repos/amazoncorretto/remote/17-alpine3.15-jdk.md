## `amazoncorretto:17-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:af450fb14df27494ee8678bf6430fb6d8fc11b076b31c76f7b6d00f32a7e7908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8c90f93e7c1979f1dfb50c056d60ba56ede5dcd3bb377b92a50cc57afcc77ce8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148569111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b43b599e4ae1e4fb64ee9fadc13d267d4e35685f4b9b024774ce96fb03346f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2023 22:30:41 GMT
ARG version=17.0.8.8.1
# Fri, 08 Sep 2023 22:30:46 GMT
# ARGS: version=17.0.8.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Fri, 08 Sep 2023 22:30:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 22:30:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 Sep 2023 22:30:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4da4eb2a067334890184c1bb5634d828825afe56f0f2437601a88d8e365dcb`  
		Last Modified: Fri, 08 Sep 2023 22:41:16 GMT  
		Size: 145.7 MB (145743105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-alpine3.15-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27eb5d1f58c7010df5087215e60278b4b9c0ab25bf9aba89197aac9d5d42a906
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146734899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5230512999fea1eb55c04c1f7c7c0bac9079b57d131b525ad5055bc681e8d197`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:47:39 GMT
ARG version=17.0.9.8.1
# Thu, 19 Oct 2023 00:47:44 GMT
# ARGS: version=17.0.9.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:47:46 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:47:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:47:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4921b033beacf6f42166ed5d59cd34c11a0f5b51cf27ca8c1c4b10b1e1b34c7e`  
		Last Modified: Thu, 19 Oct 2023 01:03:06 GMT  
		Size: 144.0 MB (144014031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
