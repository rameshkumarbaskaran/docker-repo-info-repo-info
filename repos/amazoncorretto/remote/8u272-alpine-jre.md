## `amazoncorretto:8u272-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:82af01d1fae8d62ba1e8d822f475d44eac45e83df270a9d05a5fd9b018bd0e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u272-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:055542e352146833e0683f78f6dfbdc5f86e2b564aef24dc8e72944af44c06fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43107091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12264aa4481f050f8c035b87cf7ff09d4a2e49130b8c1fc0ace4dded1acf8e9c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:20:01 GMT
ARG version=8.272.10.4
# Wed, 28 Oct 2020 00:20:29 GMT
# ARGS: version=8.272.10.4
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 28 Oct 2020 00:20:30 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:20:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b48d574c305da5c1b53dbaf7a78de17fa14c8677219545c016444dee8b1a6a0`  
		Last Modified: Wed, 28 Oct 2020 00:22:29 GMT  
		Size: 40.3 MB (40310231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
