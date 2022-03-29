## `amazoncorretto:8-alpine3.13-jdk`

```console
$ docker pull amazoncorretto@sha256:9e9ab2c60dae52881e9a8c7949dbbf9be8b02afa9449226d2e16bd4783293eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.13-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4bbaa5b1d282a41f20b2d3a8d1f8fd4c25ca2291bf9d4b1f9539263037e9ceea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101929344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fccc6f0766c4912941db5c2debdff11d77e06d7e95e4b05fc45f83b9316cf27`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:31 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:23:35 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 29 Mar 2022 05:23:36 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:23:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:23:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee2a8dc10fbff6c5d4814ca31252464b9395a202a7612c3f37e8759a458eb02`  
		Last Modified: Tue, 29 Mar 2022 05:27:42 GMT  
		Size: 99.1 MB (99110121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
