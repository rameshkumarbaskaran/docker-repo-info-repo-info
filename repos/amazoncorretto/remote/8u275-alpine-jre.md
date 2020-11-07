## `amazoncorretto:8u275-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:0bb9fdef90b3b86e30399fe7862d08427362f44307129d15c82f82a6578f30d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u275-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e594b311cebb8e6656db82fc11dee9d36f08b097bc86e17d431e416dbdf834ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43108234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2726dd125b063d493dd15d743c9ad7fdfa6a97c4f39e365d4454fa00e3fdfc36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Sat, 07 Nov 2020 00:20:29 GMT
ARG version=8.275.01.2
# Sat, 07 Nov 2020 00:20:43 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Sat, 07 Nov 2020 00:20:44 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db4fc975476101ee565b4d9aa3d6acd2e1483342197e37f5a8e9529fb63311`  
		Last Modified: Sat, 07 Nov 2020 00:22:24 GMT  
		Size: 40.3 MB (40311374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
