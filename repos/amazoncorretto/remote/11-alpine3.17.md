## `amazoncorretto:11-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:747164d32d3b0324ab9503887de05d21eb1da5a3faf6b5b5eeb37abd1478bd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d44361bb73de03355ba19a615e446505e5c3587818bf96e40a286cb31a594c18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144754369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49ce9a41b74bddca3371f1ace012f237a54d530db007ae0ad176d61fb88369a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2023 22:26:44 GMT
ARG version=11.0.20.9.1
# Fri, 08 Sep 2023 22:26:49 GMT
# ARGS: version=11.0.20.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Fri, 08 Sep 2023 22:26:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 22:26:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 Sep 2023 22:26:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1834a667b4678c22b066258acc4dbc7d32eef05d30b211283e152db4e2311d09`  
		Last Modified: Fri, 08 Sep 2023 22:37:50 GMT  
		Size: 141.4 MB (141375760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3987f88ff89d4d653df488baa7bc9781bf0efd7ca53b660506011c83d750eaf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143001693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622856fa1ad91d040d08d2be947705302336a10a3d863b983aa75f9afa887ab2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:44:32 GMT
ARG version=11.0.21.9.1
# Thu, 19 Oct 2023 00:44:37 GMT
# ARGS: version=11.0.21.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:44:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:44:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7c1e3518e7b991969766a020596da0b3cb79a2633c45d3c01548867a341c6d`  
		Last Modified: Thu, 19 Oct 2023 00:59:29 GMT  
		Size: 139.7 MB (139743403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
