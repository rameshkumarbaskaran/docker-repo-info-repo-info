## `amazoncorretto:17-alpine3.15-full`

```console
$ docker pull amazoncorretto@sha256:a1063c6ed29f785db0ca7803650ba582a072bc66491a62602611bf2a4887fe4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.15-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f081994a2d076b8b42048be30865f722a1a53c4c8d9aca118f2af130f26b6516
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194584756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ae7bc2c2dfc6787a9515eff4378a05f85d6b66d4631c1a8caca5422246c8c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:20:26 GMT
ARG version=17.0.1.12.1
# Wed, 01 Dec 2021 02:20:32 GMT
# ARGS: version=17.0.1.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Wed, 01 Dec 2021 02:20:32 GMT
ENV LANG=C.UTF-8
# Wed, 01 Dec 2021 02:20:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 01 Dec 2021 02:20:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ac5b91a69aa4eb82e5e8ce53c662bc747835961e0aae4726242f4745f63c1d`  
		Last Modified: Wed, 01 Dec 2021 02:23:58 GMT  
		Size: 191.8 MB (191766343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
