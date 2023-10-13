## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:455691cb308c8e3fe013d84ac5f25fe80d1356228c59c8e070490bc220769f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:52ebc5d9fa76a45d2cc98e438483aacec395c488f6fb48ee538d8672c57eff83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210251270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c42ea816665cfa23f2f6c4a783c46333d253923adf50950ce4d6cfc7f495dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:38:11 GMT
COPY dir:bba3c324992ed0e5d34f0f5796fe9c0e46ced00dc01939b98cad3bc355594b38 in / 
# Thu, 12 Oct 2023 22:38:11 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:05:49 GMT
ARG version=11.0.20.9-1
# Thu, 12 Oct 2023 23:06:26 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 12 Oct 2023 23:06:26 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:06:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2b92a4a464539d6c28ffd6b40875226086ace1e24d6598d771d8a65a6938acb1`  
		Last Modified: Fri, 29 Sep 2023 04:44:19 GMT  
		Size: 62.5 MB (62469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79df7dfdf502fc9c02c304bf6c817cac80578997e8d228df375fe25c7e7c4c51`  
		Last Modified: Thu, 12 Oct 2023 23:21:54 GMT  
		Size: 147.8 MB (147781625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:811fcff01fc68fe4473e0edac24ffac5a852869e1df78c0b94367b64594d5a91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209091414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191dc1d5da7ada60820103414cdc14efcb6b42617baaab6848e7305ce4d33e3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:24:12 GMT
COPY dir:826b274d38ec470bf9beb46977486da92a3347aff5fcb970deb82f445fd7f20e in / 
# Thu, 12 Oct 2023 22:24:13 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:13:40 GMT
ARG version=11.0.20.9-1
# Thu, 12 Oct 2023 23:14:08 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 12 Oct 2023 23:14:09 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:14:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d503fbdb054df5fe68cd13e3abb40a519885fcda4fbaf301b0667ae8c1285f4f`  
		Last Modified: Tue, 03 Oct 2023 00:59:41 GMT  
		Size: 64.2 MB (64163711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20632a8414daad1aade64c2ecb06212120aabb6240e7d566585f90f72cbb59a`  
		Last Modified: Thu, 12 Oct 2023 23:26:32 GMT  
		Size: 144.9 MB (144927703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
