## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:017d5ea6dc3f3b0eddb361692d188160a481a5e4a9ea70771729edb53570eb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1e6504391f098a6caaa50bddebea8bf0d429d820f54406c2881bc8586b4fe7e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101777542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0fcf1cb6749439c05f67b1e907407141175ae215e9948fbe0d44fda8b52314`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Sat, 07 Nov 2020 00:20:29 GMT
ARG version=8.275.01.2
# Sat, 07 Nov 2020 00:20:35 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Sat, 07 Nov 2020 00:20:36 GMT
ENV LANG=C.UTF-8
# Sat, 07 Nov 2020 00:20:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 07 Nov 2020 00:20:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32c7e974323f767722394c4c1f81243960f6bdb3ba2e75afd1f5f0e79440d07`  
		Last Modified: Sat, 07 Nov 2020 00:22:11 GMT  
		Size: 99.0 MB (98980682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
