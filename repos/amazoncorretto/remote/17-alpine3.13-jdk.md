## `amazoncorretto:17-alpine3.13-jdk`

```console
$ docker pull amazoncorretto@sha256:e6dfe960778a6f30e63f38008673b83e1af75366646209d566925fb691146741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.13-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1ee1fbae48ba728ec1425fb7211abb4d2bfd62eb73cb35c4c7578d4e5766dc73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194754870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5609901b8cfb4427ebbbd0b64f6d459d05fcfd4b97e2896ecf2a93bd1dc62658`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:39:45 GMT
ARG version=17.0.5.8.1
# Tue, 18 Oct 2022 23:39:51 GMT
# ARGS: version=17.0.5.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 18 Oct 2022 23:39:51 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:39:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:39:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becb7eac3368a13e26b7bc1ef7bc2084961dc5ac41a77cf0810bd5c9d7d2637`  
		Last Modified: Tue, 18 Oct 2022 23:50:00 GMT  
		Size: 191.9 MB (191927299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
