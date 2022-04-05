## `amazoncorretto:11-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:0cf01c73671e07de44ad3161f5b9444d80580b21249117f0e0bab54dbc6d4f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:204b68b211a1509fc5e112c222dc21f1cf8b3b1bd0122dfd66f793c36cd77cfa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196281277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2f291d3d6e770aaf5f3987832cbb61b08e911a8a2a236d6264b52829ae49ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:51:09 GMT
ARG version=11.0.14.9.1
# Tue, 05 Apr 2022 03:51:14 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 05 Apr 2022 03:51:15 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:51:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 05 Apr 2022 03:51:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5a4d2918db0fc18a3dcffc5f415f6cad4d5673b2275df4e29f4e910a972815`  
		Last Modified: Tue, 05 Apr 2022 03:57:19 GMT  
		Size: 193.5 MB (193461965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
