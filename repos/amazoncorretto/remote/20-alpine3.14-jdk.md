## `amazoncorretto:20-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:91db6527b89a42962ecef80c80c75d6f0def6b399ea3b50de905f66723195dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:20-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:366780b81635bc8934c57bb6dfd534b0a92305349edbb17b1398bbee47e0b7c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206557519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a18372ad8b56ab860db00194df9b801e97482d81a8b08434c2cfba7abcee361`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Wed, 22 Mar 2023 23:25:19 GMT
ARG version=20.0.0.36.1
# Wed, 22 Mar 2023 23:25:25 GMT
# ARGS: version=20.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0
# Wed, 22 Mar 2023 23:25:25 GMT
ENV LANG=C.UTF-8
# Wed, 22 Mar 2023 23:25:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Mar 2023 23:25:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fd260f1d7bb121ffa002b4301922a9aa039f9167e6e478e31c988087d5e23f`  
		Last Modified: Wed, 22 Mar 2023 23:28:19 GMT  
		Size: 203.7 MB (203727886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
