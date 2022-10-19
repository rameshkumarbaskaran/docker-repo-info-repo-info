## `amazoncorretto:8u352-alpine3.16-jre`

```console
$ docker pull amazoncorretto@sha256:f62281846b8bc777fcf90c8eeaf2b31e7a9685f6d1f786e6553f81631de16492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u352-alpine3.16-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b1540336ca5ddcfaf115d0789cda14306d8c9d661d158ac7b408ff3834e8b58d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43242984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b59b4519e02aa3c51b22f48807316b324f2abb267f036a178b90e9a7f9272e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:37:55 GMT
ARG version=8.352.08.1
# Tue, 18 Oct 2022 23:38:06 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 18 Oct 2022 23:38:06 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:38:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7b11296130ca7ea70118ff5b9c7668c9de2e21e5e83944687f5fc6500b015d`  
		Last Modified: Tue, 18 Oct 2022 23:46:31 GMT  
		Size: 40.4 MB (40436930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
