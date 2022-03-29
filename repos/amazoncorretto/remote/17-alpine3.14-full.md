## `amazoncorretto:17-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:b12e58ab9f3b1431475d762aaeeca76826c4f46dafc486037684628c8d4e5a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:abaf2f7d3e99740a6b4a96efaefbc9e2246c020d324ddfc274942858d96a3102
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194632693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5491b2bdf909487517407d7a4b733ade075615ed9d0843a6dfda07e09ad9d67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:25:18 GMT
ARG version=17.0.2.8.1
# Tue, 29 Mar 2022 05:25:23 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 29 Mar 2022 05:25:24 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:25:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:25:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36241347d03f0f2a9001691f838b607420561494cc08808792d13ec3c5bad198`  
		Last Modified: Tue, 29 Mar 2022 05:32:50 GMT  
		Size: 191.8 MB (191814339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
