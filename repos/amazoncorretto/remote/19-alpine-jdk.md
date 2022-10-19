## `amazoncorretto:19-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:b56e93c64f61233c016f1a94ae67ef37761adba65b2ecbd74c4579cbae2b44ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e3bdc488d0a1b07dc32b40cae814629b1d393fcd43cddaf3d691c5ca6e178585
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203283982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d9b40a87cf07e07cc847ffebbdff423aeaed1ebbc6b0899870c6ab1aece81e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:41:34 GMT
ARG version=19.0.1.10.1
# Tue, 18 Oct 2022 23:41:40 GMT
# ARGS: version=19.0.1.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Tue, 18 Oct 2022 23:41:41 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:41:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:41:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc07900d255ced73f99d9cfa89ed71f700953127fd0c9b0d20ea680fe7fc3aa`  
		Last Modified: Tue, 18 Oct 2022 23:54:14 GMT  
		Size: 200.5 MB (200477928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
