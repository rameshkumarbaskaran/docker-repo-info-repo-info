## `amazoncorretto:20-al2023-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:8c6a5a0daeb1c53881f6e901e93c1435f101a245cea657834e0ded2ab403245f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2023-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:da4a89745a5f6d2cefb183761af895f590a2c7d1127033f74f387ecf069a416b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260598468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b049101593d4f0cef7bfa83526c76fc5131af3a8e113b3ec5fd48049ee59d769`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:37:51 GMT
COPY dir:73a08d9acd2707b5f429ab7e4f26f6f5880d94265654591f74d7102f20954c66 in / 
# Thu, 12 Oct 2023 22:37:52 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:15:26 GMT
ARG version=20.0.2.10-1
# Thu, 12 Oct 2023 23:15:55 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Thu, 12 Oct 2023 23:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:15:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:860bcbd64bf9485a06bc1858b0de975763ffab4b4fb53fb19b66b42536e48fe7`  
		Last Modified: Wed, 11 Oct 2023 21:33:29 GMT  
		Size: 52.4 MB (52395746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9003245fbad1dc3b5f5c30fddaf1f36ec913298c17981794b750f38a4130f86b`  
		Last Modified: Thu, 12 Oct 2023 23:27:38 GMT  
		Size: 208.2 MB (208202722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2023-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6131b88018a7cd1f171008d93715caca7deb49b8e799be205e6f1a11a9a02daf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257641050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443e6f0ff51648567e0a7ed68513bf740734ddd051e8e6f9f339601448329add`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:23:51 GMT
COPY dir:23c4f526fba599c79c471bcc9a859c715cfebcd3d79aabf95868c2189962dde3 in / 
# Thu, 12 Oct 2023 22:23:51 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:20:55 GMT
ARG version=20.0.2.10-1
# Thu, 12 Oct 2023 23:21:19 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Thu, 12 Oct 2023 23:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:21:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:d726870119c530d3b141cccd8b55693be0fc259a674ed2bc3bcf5999ff1434d3`  
		Last Modified: Thu, 12 Oct 2023 01:34:33 GMT  
		Size: 51.5 MB (51474358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed3fa821f186a2985f95e5901c4cd0b4eeefaab8e3d9312ce4f36b072b8b99d`  
		Last Modified: Thu, 12 Oct 2023 23:31:43 GMT  
		Size: 206.2 MB (206166692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
