## `amazoncorretto:17-alpine3.16`

```console
$ docker pull amazoncorretto@sha256:c05e52706db17fe23a6853502c73dafebca0640b4b157324fea028fe5730191c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:70e74be695e77491200d1c8e45dd4b87836cd5a0c63752be598b2d43f7752aff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194740890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80b67a1b71a1aa593d7829fb0173c9114bec3852b0d577a7f4a38dcf33de7b8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 18 Oct 2022 23:40:14 GMT
ARG version=17.0.5.8.1
# Tue, 18 Oct 2022 23:40:20 GMT
# ARGS: version=17.0.5.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Tue, 18 Oct 2022 23:40:20 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:40:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 18 Oct 2022 23:40:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6579f4308b83675c7b753a62dab3a8dfe68e9f5d7836c44ac0d8be9fad5054c`  
		Last Modified: Tue, 18 Oct 2022 23:51:27 GMT  
		Size: 191.9 MB (191934836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
