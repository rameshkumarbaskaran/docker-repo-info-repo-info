## `amazoncorretto:8-alpine3.15`

```console
$ docker pull amazoncorretto@sha256:9ce3e919744eff27728292f14ba50c822c7a57f31d481ffe6836d3d6e96709bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.15` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3699368535752cafa54005cb11ec1b4ebd8013b778e16c77263bc39863f02c72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101622061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f6cea215a85284df31d8928ea6e8824305daeeae04532e230751016c125b54`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:37:42 GMT
ARG version=8.352.08.1
# Tue, 18 Oct 2022 23:37:47 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 18 Oct 2022 23:37:47 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:37:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:37:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad768ad0eadd71ce145022b71c36d6ce1ef438f9edf00053e26e3c6db0523371`  
		Last Modified: Tue, 18 Oct 2022 23:45:26 GMT  
		Size: 98.8 MB (98798549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
