## `amazoncorretto:8-alpine3.16-full`

```console
$ docker pull amazoncorretto@sha256:035a8928e22477fb7c8508d386e807899e01f17a39cec49031144608dec2c7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.16-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bf0ab360c0a1d07a5d8c5fb81d955067d9e83479c043876a6e20f291ec14f28c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101604241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e18a44f6aeef677e65316316da4b4dbd70b24b39604f07bdde679d7c9764a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:37:55 GMT
ARG version=8.352.08.1
# Tue, 18 Oct 2022 23:37:59 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 18 Oct 2022 23:37:59 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:38:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:38:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d4d667345667874585d2424a5c037d5dd2c83303a42b57f288943897d130b0`  
		Last Modified: Tue, 18 Oct 2022 23:46:03 GMT  
		Size: 98.8 MB (98798187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
