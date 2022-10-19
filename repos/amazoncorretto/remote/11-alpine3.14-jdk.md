## `amazoncorretto:11-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:e010adf35f4af34a1f0194b98910c8b9facce430e0a6d87e802eae5fe2787bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1c8a56e20c01d0b76a7beee47dc486171a4f7184e6351d7fea887f00dc4c7860
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196369875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b4c2a58257bd17effc29c863d32258b52503356da4e8a69575835ddfca2eb2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:38:47 GMT
ARG version=11.0.17.8.1
# Tue, 18 Oct 2022 23:38:53 GMT
# ARGS: version=11.0.17.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 18 Oct 2022 23:38:53 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:38:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:38:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2f9c2f8931854f7d923e9222e3cb6581088edbd083d0e052c934a8e72c578`  
		Last Modified: Tue, 18 Oct 2022 23:47:55 GMT  
		Size: 193.5 MB (193542386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
