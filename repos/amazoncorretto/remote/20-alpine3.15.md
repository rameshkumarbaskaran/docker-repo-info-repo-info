## `amazoncorretto:20-alpine3.15`

```console
$ docker pull amazoncorretto@sha256:54645e163c32b11c68e5a11e2e85d884de111333c2669f29e6c6f75570a5e211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:20-alpine3.15` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b2f409f1c25c075160fe3330ba5ea39bdea89e432255339ea34cb813e7020123
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206554079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190bef7cea53bc1e3ab0683ff16e30c96f17c911781a1f9dd98bad3c9fc91d4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Wed, 22 Mar 2023 23:25:28 GMT
ARG version=20.0.0.36.1
# Wed, 22 Mar 2023 23:25:35 GMT
# ARGS: version=20.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0
# Wed, 22 Mar 2023 23:25:35 GMT
ENV LANG=C.UTF-8
# Wed, 22 Mar 2023 23:25:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Mar 2023 23:25:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd1839e45bbcdcb4b484224ac5d417e3ffe63087013de4fe4b4bb0a09e592f0`  
		Last Modified: Wed, 22 Mar 2023 23:28:46 GMT  
		Size: 203.7 MB (203727933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
