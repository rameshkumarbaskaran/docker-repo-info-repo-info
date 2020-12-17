## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:76acd2ab267cb71abeab875af97d91fb483d81bc4e372d1dd28bad32d8ccd693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ad16f7b90421b975a18429d141c94895cd4fe1d4489bc610d53cf7e18ecf4527
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194996787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10971533e52923f349ed175ba9841881fb4d18cee46d345c854debb6093601e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:23 GMT
ARG version=11.0.9.12.1
# Thu, 17 Dec 2020 00:50:30 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 17 Dec 2020 00:50:30 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63066bc434b60a2bf6ab277b7713d0cdf8436126ed3ad4fc88a7c72d79e7070c`  
		Last Modified: Thu, 17 Dec 2020 00:52:24 GMT  
		Size: 192.2 MB (192197721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
