## `amazoncorretto:19-alpine`

```console
$ docker pull amazoncorretto@sha256:8536a448a795efbf8a3743cdc263c03e512b865cce23814751702eb3730b973d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5997c3cc6d631537647d347ad747cab8a2a52da75b5b6e73714afee9576f0503
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203038805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243f57ea5353523b8a9473acdce4fac0a428704d5d0af1f67db85bef34dd2bb1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 20 Sep 2022 23:21:10 GMT
ARG version=19.0.0.36.1
# Tue, 20 Sep 2022 23:21:15 GMT
# ARGS: version=19.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Tue, 20 Sep 2022 23:21:16 GMT
ENV LANG=C.UTF-8
# Tue, 20 Sep 2022 23:21:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Sep 2022 23:21:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a184229a93323a48cf80995991b8583a71a849e194a643277e61e19b8b9fdd3`  
		Last Modified: Tue, 20 Sep 2022 23:25:23 GMT  
		Size: 200.2 MB (200215293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
