## `amazoncorretto:17-alpine3.16-full`

```console
$ docker pull amazoncorretto@sha256:a658aefcd1165fc56832c9c662274c34f82f14e1c4c717c0780006d1e0c7cef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-alpine3.16-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8caa7e4490a3e55ee5f5db5c82feccdcb2ed0022a1575af5b3cead980945daa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148550323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673fde86c921089bf8b1855b87ed553934e5d3600087bf0aa5f1e170dfa2e039`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2023 22:30:50 GMT
ARG version=17.0.8.8.1
# Fri, 08 Sep 2023 22:30:56 GMT
# ARGS: version=17.0.8.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Fri, 08 Sep 2023 22:30:56 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 22:30:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 Sep 2023 22:30:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9f508b59677c45a412ce7f5be365916678a4318aefc27316202e824d2b982`  
		Last Modified: Fri, 08 Sep 2023 22:41:41 GMT  
		Size: 145.7 MB (145742640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-alpine3.16-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c78bfcbd3f6b51aad014b895d1820d5eb145d2c8c6a51ea95d7411e0437d4ac0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146722121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fefe9b85aba0b72144a337ea3f1858bc2ec23dc045e38f054bf3404d14ddf17`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:47:49 GMT
ARG version=17.0.9.8.1
# Thu, 19 Oct 2023 00:47:53 GMT
# ARGS: version=17.0.9.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:47:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:47:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:47:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d5e34678ea2c3f784ab14f73975fde35e39ab5fc3978fe76e8f36d6d06c5da`  
		Last Modified: Thu, 19 Oct 2023 01:03:30 GMT  
		Size: 144.0 MB (144014098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
