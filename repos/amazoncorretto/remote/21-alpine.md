## `amazoncorretto:21-alpine`

```console
$ docker pull amazoncorretto@sha256:e8728b86cc8092f49e737a84faaae31695ff759d1d21baa54b16e81fcb4fef79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efe096e8c803810b29ba1f96d5422193b0040d937c5739fa43d3dc9133ac6c31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162587132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30357837d905581d283effdbb2847a1ce1b69427d72280a1c9e3002d97c811fb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:34:45 GMT
ARG version=21.0.0.35.1
# Thu, 28 Sep 2023 23:34:51 GMT
# ARGS: version=21.0.0.35.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Thu, 28 Sep 2023 23:34:51 GMT
ENV LANG=C.UTF-8
# Thu, 28 Sep 2023 23:34:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 28 Sep 2023 23:34:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893de0d50a9da759e1be67c7650b3797dfea1ea371339a641d62f40f09683de7`  
		Last Modified: Thu, 28 Sep 2023 23:40:24 GMT  
		Size: 159.2 MB (159185165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6fc23076fa874f3f6d44054b465b5644fe3000743bc1017497e99fff5b5e98b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160528141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9896b32780f20a5c22566236584c13008f4e488259e08a492a9fdb24dc2f748f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 00:50:05 GMT
ARG version=21.0.1.12.1
# Thu, 19 Oct 2023 00:50:10 GMT
# ARGS: version=21.0.1.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Thu, 19 Oct 2023 00:50:12 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:50:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Oct 2023 00:50:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4dc8b2fadc81913fa67a84d2641a875eb61b3acffb8969fb8dae0324a85e2a`  
		Last Modified: Thu, 19 Oct 2023 01:08:33 GMT  
		Size: 157.2 MB (157196310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
