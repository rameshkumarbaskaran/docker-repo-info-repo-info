## `amazoncorretto:15-alpine`

```console
$ docker pull amazoncorretto@sha256:0cfdc770fdbc39457bf06a1549a9c5e9762a02f19e380104c4d6a1bfc734915a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2d49338d06551b0a31848cecad668c1b877f8f27818d66b45de7f763bc3e1972
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207714787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e96f35759b93bdadf20ca3e05a6982515670dfb155f0d700abc50d6b91ac00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Wed, 28 Oct 2020 00:21:12 GMT
ARG version=15.0.1.9.1
# Wed, 28 Oct 2020 00:21:19 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Wed, 28 Oct 2020 00:21:19 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Oct 2020 00:21:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de3f84eb66e9b0962199bb01018f641091674b315a07635034f849249cadb56`  
		Last Modified: Wed, 28 Oct 2020 00:23:30 GMT  
		Size: 204.9 MB (204917927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
