## `amazoncorretto:20-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:c09fcb7b4ec68e54d5674adc9d987b64547e5ea9523942f5700f7d1bedb191ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:20-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fbdd09cca64cc5917b42c69c49c6a0baef2b697aaa3fb3d1cfbc920b37a05879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207102573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f781e011ece2790ccafdde36ea4dbcf6f4f3efb29937dbf822384ba016bcc747`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Wed, 22 Mar 2023 23:25:46 GMT
ARG version=20.0.0.36.1
# Wed, 22 Mar 2023 23:25:52 GMT
# ARGS: version=20.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0
# Wed, 22 Mar 2023 23:25:53 GMT
ENV LANG=C.UTF-8
# Wed, 22 Mar 2023 23:25:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Mar 2023 23:25:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482e0f4f49708c49e0382ef43b2933c585fa38b955d9a066379c432d0a99470f`  
		Last Modified: Wed, 22 Mar 2023 23:29:40 GMT  
		Size: 203.7 MB (203728127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
