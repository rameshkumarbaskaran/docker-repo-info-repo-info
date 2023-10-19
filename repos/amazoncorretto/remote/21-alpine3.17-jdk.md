## `amazoncorretto:21-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:1313c6fd5a7e7751961e6108b2c5570bd6d281869c2bffb85ea0bf41b9b8304f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:87c129f77cbfcdbf23c3f1062fd4b25ee02650c863a872fa72b514b6167abadc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162563539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e407bd1e4ccfc6a80e6b0e73723d84b2d395216ee2cdda0f6c70f849a54868e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Sep 2023 00:23:34 GMT
ARG version=21.0.0.35.1
# Fri, 22 Sep 2023 00:23:41 GMT
# ARGS: version=21.0.0.35.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Fri, 22 Sep 2023 00:23:41 GMT
ENV LANG=C.UTF-8
# Fri, 22 Sep 2023 00:23:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Sep 2023 00:23:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a60f2e30e2b4a5279ea40448c98f387d3ae1e4461e162dbddd1531106b8a55`  
		Last Modified: Fri, 22 Sep 2023 00:29:23 GMT  
		Size: 159.2 MB (159184930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:af2bb3bf51d5a57db673ca0c67c1c5c6f163afce2f501b2581b46e7b20dd1a54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160453792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc8fadd79a9adb4b0321bb2dea4955d79663605055f3b351793a1e41334fbe9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:49:56 GMT
ARG version=21.0.1.12.1
# Thu, 19 Oct 2023 00:50:01 GMT
# ARGS: version=21.0.1.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:50:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:50:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:50:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e1173cbb0391bbad077ab43510c861210e8414c4101e5606c019ede4736b89`  
		Last Modified: Thu, 19 Oct 2023 01:07:41 GMT  
		Size: 157.2 MB (157195502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
