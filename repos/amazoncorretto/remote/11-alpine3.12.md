## `amazoncorretto:11-alpine3.12`

```console
$ docker pull amazoncorretto@sha256:d02f1f73058b2a1e14c698959ef9eea82f8a28475911f5011cb823fa59ecc276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.12` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f88a55a23aeae4b536180bdb23334bbeae60bb93cbb6fc4e2f65733a1f39c356
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196269706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd77db5edb1112e5650a5f001be4d7e797460dd70d0ee42f0ee738338f237bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:19 GMT
ADD file:c1aa87a3b464fca64d769444b5201bc0426a1f517c91c4a7916270e10f8b300b in / 
# Tue, 05 Apr 2022 00:20:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:50:59 GMT
ARG version=11.0.14.9.1
# Tue, 05 Apr 2022 03:51:05 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 05 Apr 2022 03:51:06 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:51:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 05 Apr 2022 03:51:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1b7ca6aea1ddfe716f3694edb811ab35114db9e93f3ce38d7dab6b4d9270cb0c`  
		Last Modified: Tue, 05 Apr 2022 00:21:10 GMT  
		Size: 2.8 MB (2808060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6146c69fc65c9033b0862e02330f39cd4d01983d72e32e6973fa48ff5af6ff96`  
		Last Modified: Tue, 05 Apr 2022 03:56:51 GMT  
		Size: 193.5 MB (193461646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
