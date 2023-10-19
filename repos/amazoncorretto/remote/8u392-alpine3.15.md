## `amazoncorretto:8u392-alpine3.15`

```console
$ docker pull amazoncorretto@sha256:ea9b6cc72946d22d1e4982972b705671f5b1a774fcb61868a1472f7660516546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `amazoncorretto:8u392-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:81c389ce521a778137a7515b3b20f50aac77ca1539078751cee50905cc738083
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102526468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0632fbc707df8a45fef5ec0d72d7585ac5c1e59e0d4a9ec1624a56f92f037a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:40:52 GMT
ARG version=8.392.08.1
# Thu, 19 Oct 2023 00:40:56 GMT
# ARGS: version=8.392.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:40:57 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:40:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:40:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c2240e817ffd6df2a6148bc10d39628c18436d01f6dbf243910a2ba98db79f`  
		Last Modified: Thu, 19 Oct 2023 00:53:54 GMT  
		Size: 99.8 MB (99805600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
