## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:6cbe784a30ddcb816267bed236c3f8b0f0b8e5541f5c2c4395e75e8999445751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05faa748612c00581c674bc95afe565555ec78f23c038f603874bb7f863e340d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137907636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb4e34bd21e092f6168039e59905bfced83a457bd3dfaa417c1c22c65065a53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 22:20:04 GMT
ADD file:6ebab25a4f1aa82238dbf1a48f38d22c6421052d0d158cf88cbc1a4d01b5c5c1 in / 
# Thu, 26 Jan 2023 22:20:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Jan 2023 23:08:43 GMT
ARG version=1.8.0_362.b08-1
# Thu, 26 Jan 2023 23:09:04 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 26 Jan 2023 23:09:05 GMT
ENV LANG=C.UTF-8
# Thu, 26 Jan 2023 23:09:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1e78b99dd1fd1031c6513834c4b5f594fa3cec5d06cdeb4b65ee104180bc0d4c`  
		Last Modified: Thu, 26 Jan 2023 20:44:53 GMT  
		Size: 62.3 MB (62341068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb46b29d5999c10120c43bc672fe0da45f7b0f2b05f34230305ba537413f8a7`  
		Last Modified: Thu, 26 Jan 2023 23:13:11 GMT  
		Size: 75.6 MB (75566568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e4523d4406813e19385b46ba08823793d19862b7353ab3579b98de5fbed93a67
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123610754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779d6f7ee6b684e61009fbb75afe43ae373de9020f84a53ad3aeab225e9854e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:05:26 GMT
ARG version=1.8.0_362.b08-1
# Thu, 16 Feb 2023 21:05:42 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:05:43 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:05:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b9a0290cddf3ca6685e4cb9dc1139d87ec575d77a85f10794f976ef6927cab`  
		Last Modified: Thu, 16 Feb 2023 21:07:56 GMT  
		Size: 59.6 MB (59606949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
