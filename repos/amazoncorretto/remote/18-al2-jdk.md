## `amazoncorretto:18-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:f8ce56ea11bd3b8f2ec8c80f164d7537baedc191b4aae5c7b57f54ad6b955c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:18-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:faa6b673f59e9e0442cb846a8c8802ed6ec6fe2eeed296773de67567ebafdaab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215014747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d981e22f2b92a8232b18bd968fc3821f665dfd476b269928a323282d3db3227`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 03:01:29 GMT
ARG version=18.0.2.9-1
# Fri, 12 Aug 2022 03:01:55 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Aug 2022 03:01:56 GMT
ENV LANG=C.UTF-8
# Fri, 12 Aug 2022 03:01:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188a28cedc43dd2a2fb4b59c6bc7b5a07186690557cfb49f2750f1378654b259`  
		Last Modified: Fri, 12 Aug 2022 03:05:34 GMT  
		Size: 152.7 MB (152698531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:18-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7b586d734f779754dc7ce1b1a1677b509816364345db9765524bee7c69323da4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215313616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564b3e40a87cd59cbf8655cd1dcdbe60e912057972a5c408b2c8c23c94dae93a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 26 Aug 2022 00:39:31 GMT
ADD file:a0918d3dfd5c1b4e0594c53d0dfc4c97f1ebaf14085279c79f36f06cf7ed95ee in / 
# Fri, 26 Aug 2022 00:39:32 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 01:02:14 GMT
ARG version=18.0.2.9-1
# Fri, 26 Aug 2022 01:02:31 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 26 Aug 2022 01:02:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 01:02:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:12df598bc31e0ff3cadc2667d34dc645b837d712e7e15ce3e9080ae91744dcd0`  
		Last Modified: Mon, 22 Aug 2022 22:09:44 GMT  
		Size: 63.9 MB (63938765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa256c032ea30a19222d09b401bfe7a023caac99781de9f6a7de8ecd30a8b3c`  
		Last Modified: Fri, 26 Aug 2022 01:05:19 GMT  
		Size: 151.4 MB (151374851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
