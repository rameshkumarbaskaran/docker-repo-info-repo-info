## `amazoncorretto:8u272-alpine`

```console
$ docker pull amazoncorretto@sha256:8d1066057e460bb18119533df28fd36403d926dbf4e10576e03dd7f80eff21a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u272-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76fc6ca6fc6c038cd5f54778418ad8901a80971994590222145091db38f6a19e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101765845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c48bb5281a8e51b8a2af9d0996e7860e9c1cff7281f94bfb07d13a6fb7f4f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:20:01 GMT
ARG version=8.272.10.4
# Wed, 28 Oct 2020 00:20:18 GMT
# ARGS: version=8.272.10.4
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 28 Oct 2020 00:20:19 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:20:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Oct 2020 00:20:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3401c03af81c0a0987aae5fe034b6952731a8a6a765fdd627e04490d9d8e69`  
		Last Modified: Wed, 28 Oct 2020 00:22:17 GMT  
		Size: 99.0 MB (98968985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
