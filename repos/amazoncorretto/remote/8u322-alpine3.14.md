## `amazoncorretto:8u322-alpine3.14`

```console
$ docker pull amazoncorretto@sha256:a6a06331cec28c60ed6381736f22ae57975304cf8decb71180109abbabf22da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.14` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e135649043a670d0fff67374bfacfdda540cbeb08776ccfa34a1dc493637238
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101921873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509cdd2b28a7184e4a1a4e2556823c22bf84383c3fa7b6dc0c06a49fbfbe6c37`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:44 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:23:48 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 29 Mar 2022 05:23:48 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:23:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 29 Mar 2022 05:23:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65f7fa5214b45995d4bc0b7d0b8fac89cf1013b9aa10ea493071374f18e5950`  
		Last Modified: Tue, 29 Mar 2022 05:28:17 GMT  
		Size: 99.1 MB (99103519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
