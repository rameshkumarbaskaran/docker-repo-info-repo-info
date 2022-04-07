## `amazoncorretto:18-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:d74645031b89b83865476e51f0ec34b52b53f329ddf086161a2cdbf43d6a0924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:18-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8c47c216b0137cc815cfe18b217775a547412150cff3799ce5f3a21895ad04e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195709014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea196aa1453a33bb76ecad7a3e297c11978db0c73acb42ad50fee9d03085dea`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Wed, 06 Apr 2022 22:21:05 GMT
ARG version=18.0.0.37.1
# Wed, 06 Apr 2022 22:21:11 GMT
# ARGS: version=18.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-18=$version-r0
# Wed, 06 Apr 2022 22:21:12 GMT
ENV LANG=C.UTF-8
# Wed, 06 Apr 2022 22:21:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 06 Apr 2022 22:21:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ea8bd6c630c3c4c2acdcc03e884516dabd320d787e8614acce9b815af0c29`  
		Last Modified: Wed, 06 Apr 2022 22:24:57 GMT  
		Size: 192.9 MB (192889702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
