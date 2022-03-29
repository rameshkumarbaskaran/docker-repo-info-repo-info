## `amazoncorretto:17-alpine3.12`

```console
$ docker pull amazoncorretto@sha256:35a443342555a0100ce29d435cf43c64106dbe79e493dbb9ddab1047d8214bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.12` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76e6623444b26978ff48bfee223a362911d158c5fe745ffe5bf5d00a61d81b35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194617683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0821d71005a86316f560894bd02d94fde743b9bc01ca8fe2d806de89ee1f5681`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:50 GMT
ADD file:cbe481f8a83651395a1e84bf344472e2fa9cc3551601514e50c000f76255e938 in / 
# Tue, 29 Mar 2022 00:19:51 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:24:58 GMT
ARG version=17.0.2.8.1
# Tue, 29 Mar 2022 05:25:04 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 29 Mar 2022 05:25:05 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:25:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:25:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9c4930dab7624ba1487a3aa1f29c65f2241e7a8fae81d26e8bc66eaa4086c440`  
		Last Modified: Tue, 29 Mar 2022 00:20:53 GMT  
		Size: 2.8 MB (2807997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f7a5fe706d0022d335c9277bf02da9151394a02398cfc6696e7cbec97716c9`  
		Last Modified: Tue, 29 Mar 2022 05:31:53 GMT  
		Size: 191.8 MB (191809686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
