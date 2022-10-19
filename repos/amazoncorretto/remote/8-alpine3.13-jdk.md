## `amazoncorretto:8-alpine3.13-jdk`

```console
$ docker pull amazoncorretto@sha256:ef36f1a0456f03891ea7a7f2b68091ae657610d2d1f84ac34b5b125077487e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.13-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e145290949d7f72477844220c8fd20019959ffc8416bbd8258e021e281b65fb1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101626878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d1d1dc9e740f421eb6eae853a7f8eb88d2d25d103dc228a5a5fe4cb7cb43ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:37:17 GMT
ARG version=8.352.08.1
# Tue, 18 Oct 2022 23:37:20 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 18 Oct 2022 23:37:21 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:37:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:37:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba08372bd0c1e6dce76e29ce4d33028e54cea8b34a2e6107da19eef81f32f66`  
		Last Modified: Tue, 18 Oct 2022 23:44:13 GMT  
		Size: 98.8 MB (98799307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
