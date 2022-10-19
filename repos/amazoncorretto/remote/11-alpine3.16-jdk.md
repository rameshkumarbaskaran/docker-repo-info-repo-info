## `amazoncorretto:11-alpine3.16-jdk`

```console
$ docker pull amazoncorretto@sha256:9eddcd0fc6e35c4a09fc402bf67e0aac986ae01e96fb0cb74059f4914016a24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.16-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1e776ebafea54c75375228a9677cdecaf6ece1cd69e1abf957aba81913c90994
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196348572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382ae610c270829671d242bb6ed3574830d4a20b502633cf47c6c102197db97d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:39:06 GMT
ARG version=11.0.17.8.1
# Tue, 18 Oct 2022 23:39:12 GMT
# ARGS: version=11.0.17.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 18 Oct 2022 23:39:13 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372ddc08eae678be43adcc9ce9cf8f6b4e20364e62b95676d574004fb3768acd`  
		Last Modified: Tue, 18 Oct 2022 23:48:51 GMT  
		Size: 193.5 MB (193542518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
