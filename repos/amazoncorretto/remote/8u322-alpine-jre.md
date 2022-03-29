## `amazoncorretto:8u322-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:4ae3a2f0b602ee491bc7ce0321dfdd8cc7846c94c0a90f288478938f0cce3bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4bd6bdcc4e3ade550b8db21fd52d2f0bcb0931034e242915302fc1137ac7216b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43195598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d42271b38731c86cbe15e3dec23dc26e5a98218e42ee9d8fc41f8f8c8703775`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:23:57 GMT
ARG version=8.322.06.2
# Tue, 29 Mar 2022 05:24:08 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/java /usr/bin/java &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/jjs /usr/bin/jjs &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/keytool /usr/bin/keytool &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/pack200 /usr/bin/pack200 &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/rmid /usr/bin/rmid &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/rmiregistry /usr/bin/rmiregistry &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/unpack200 /usr/bin/unpack200
# Tue, 29 Mar 2022 05:24:08 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 05:24:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5838f7e19b57bb7c5c652bc05b3dfe494043e529c31b512ae20bb4e85a54392b`  
		Last Modified: Tue, 29 Mar 2022 05:29:21 GMT  
		Size: 40.4 MB (40381086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
