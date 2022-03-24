## `amazoncorretto:8-alpine3.15-jre`

```console
$ docker pull amazoncorretto@sha256:6916398cc777bd4bec602b860be98552a673ee96c9e38e2a20f31d6468da04e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.15-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3bba63f1189b13bfc2314df91853ac2fa379baa4c4228ec051c497f6994fcf19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a458139731c4f787ba60100e2d4bb982df97a6d25d2083deb53a7d341750697`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 15:46:36 GMT
ARG version=8.322.06.2
# Thu, 24 Mar 2022 21:19:46 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/java /usr/bin/java &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/jjs /usr/bin/jjs &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/keytool /usr/bin/keytool &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/pack200 /usr/bin/pack200 &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/rmid /usr/bin/rmid &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/rmiregistry /usr/bin/rmiregistry &&     ln -s -f ../lib/jvm/default-jvm/jre/bin/unpack200 /usr/bin/unpack200
# Thu, 24 Mar 2022 21:19:46 GMT
ENV LANG=C.UTF-8
# Thu, 24 Mar 2022 21:19:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e868b552c0eb6bac488b395022a84dc8b2ff9a0ae3294011619e47567f11caeb`  
		Last Modified: Thu, 24 Mar 2022 21:21:46 GMT  
		Size: 40.4 MB (40381062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
