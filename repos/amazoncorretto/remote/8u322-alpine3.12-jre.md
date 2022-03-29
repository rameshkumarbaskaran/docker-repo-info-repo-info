## `amazoncorretto:8u322-alpine3.12-jre`

```console
$ docker pull amazoncorretto@sha256:6b15e6e5998eaf7b7400527ce2f0024cd523517eb4f370a43c2382853ad25720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.12-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:daa20d306c7ac68c119cb8289a3cce448e6ddb08d948bafde1085ee4c9088c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43179779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2138eca6d4e6b465e0ec54f0f62eac6568eb2c4cd927d91c6966dd3f7bd8e4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:50 GMT
ADD file:cbe481f8a83651395a1e84bf344472e2fa9cc3551601514e50c000f76255e938 in / 
# Tue, 29 Mar 2022 00:19:51 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:18 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:23:28 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 29 Mar 2022 05:23:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:23:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:9c4930dab7624ba1487a3aa1f29c65f2241e7a8fae81d26e8bc66eaa4086c440`  
		Last Modified: Tue, 29 Mar 2022 00:20:53 GMT  
		Size: 2.8 MB (2807997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32683bf1c4a1a623494a629127e53dd13aa979ea33022a410424de3a80413581`  
		Last Modified: Tue, 29 Mar 2022 05:27:24 GMT  
		Size: 40.4 MB (40371782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
