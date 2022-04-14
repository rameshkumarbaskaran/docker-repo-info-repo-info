## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:e587eb20f87ba6109297db508ce7c49f4d6fbbcd770b0e56b851c5d26013ba93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:50309dc382998097b5bc4d52cecfaf7431cd39af32e602c4f7007812e6e7092c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137768762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0c017b0410650fda14cbd11091c5ab95f49a9917fe9fd165a86d1418e6f38c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 22:08:38 GMT
ARG version=1.8.0_322.b06-2
# Wed, 13 Apr 2022 22:08:59 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 13 Apr 2022 22:08:59 GMT
ENV LANG=C.UTF-8
# Wed, 13 Apr 2022 22:08:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904c7434460bc3b4682babf27e648f116a88dcd5bd021c6fca766e8f9cd12281`  
		Last Modified: Wed, 13 Apr 2022 22:13:01 GMT  
		Size: 75.5 MB (75531121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ddfd7b82c4df6cfd31bce1829f5275aa7f96a77d5742c96807b92e045800f40e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123424932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1475d6c83ef31ccd3c08019cc0902c67ead4719f61ee14825e7f8e1df202479c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 21:56:56 GMT
ARG version=1.8.0_322.b06-2
# Wed, 13 Apr 2022 21:57:07 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 13 Apr 2022 21:57:08 GMT
ENV LANG=C.UTF-8
# Wed, 13 Apr 2022 21:57:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b1aba29608f79d6bdcd656b371450070727de3f0a587248b01efd9c1a0b00d`  
		Last Modified: Wed, 13 Apr 2022 21:59:08 GMT  
		Size: 59.6 MB (59554651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
