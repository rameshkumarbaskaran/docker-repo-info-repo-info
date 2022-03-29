## `amazoncorretto:8u322-alpine3.13-jre`

```console
$ docker pull amazoncorretto@sha256:56e0794b35f70edf2f5e90ef417692fdbfb3c0bc3818c67fd262525b9bac3fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.13-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ebc7d94ac3f6a88c25eead492e1425dbb7ef902abea4978339db3a41d7d3f059
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43191204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d509849fe98e0e9732aba0f5dfc850d361e97603c37918bd75a3bde4aa2d18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:31 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:23:41 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 29 Mar 2022 05:23:41 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:23:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4756208b38f655ac01b741179e77bb2da1231b5a9bf9ea23d5f242f01fb917`  
		Last Modified: Tue, 29 Mar 2022 05:28:00 GMT  
		Size: 40.4 MB (40371981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
