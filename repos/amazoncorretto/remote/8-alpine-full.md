## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:668540ef71e60cc529c1b218a2125db59df84b9ceadf5a849f1193548c760800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2ffd60a7447d28cf150f8412a3f9489cbb0a6d3f8475d4a8bc2ee2424c524fb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101871514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55fbde46e52e52ee3ffbab186b0a569b07aa201dad3f8fe1006d684d6f59779`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:19:38 GMT
ARG version=8.312.07.1
# Wed, 01 Dec 2021 02:19:45 GMT
# ARGS: version=8.312.07.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 01 Dec 2021 02:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 01 Dec 2021 02:19:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 01 Dec 2021 02:19:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2b0c20764c154ee9c6b8319444c482c110e1c734177be1126b212e70aaf3ba`  
		Last Modified: Wed, 01 Dec 2021 02:22:10 GMT  
		Size: 99.1 MB (99053101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
