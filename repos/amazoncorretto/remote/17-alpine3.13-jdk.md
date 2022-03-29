## `amazoncorretto:17-alpine3.13-jdk`

```console
$ docker pull amazoncorretto@sha256:7269bd026f97ee2ed6c4707655a2de4f54d3c242950c55fd0eb5e643db5a7036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.13-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b47ab4daf1e4b7f4e2fe2cbb41b2cd66fc7bb5c4564b7d28f63fe8751de174ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194628931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bf5daab60ef4e8018ed6fcbf0fdefed55debd06b08011d0ab9ddcc397ad614`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:25:08 GMT
ARG version=17.0.2.8.1
# Tue, 29 Mar 2022 05:25:14 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 29 Mar 2022 05:25:15 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:25:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:25:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f02595ed9a51102bc40fa085f86dbbbed7c5c450cd4c641eb138f22f9df3c4`  
		Last Modified: Tue, 29 Mar 2022 05:32:21 GMT  
		Size: 191.8 MB (191809708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
