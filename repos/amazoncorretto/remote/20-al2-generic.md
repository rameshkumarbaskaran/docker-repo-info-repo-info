## `amazoncorretto:20-al2-generic`

```console
$ docker pull amazoncorretto@sha256:fa2019e772a5a5d21cb9b44165a919d74ae189405093caf89322a69f0aef0713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:08e6f3836b086f478bb1c68d1125667b9c0cf55b5c4a3a2ea344975a7a5e9752
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223378349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d64b2adb80831eb69b6f3d136566f1387b48ffe2666e1e1377905e17c8e11e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:38:11 GMT
COPY dir:bba3c324992ed0e5d34f0f5796fe9c0e46ced00dc01939b98cad3bc355594b38 in / 
# Thu, 12 Oct 2023 22:38:11 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:14:45 GMT
ARG version=20.0.2.10-1
# Thu, 12 Oct 2023 23:15:22 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 12 Oct 2023 23:15:22 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:15:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:2b92a4a464539d6c28ffd6b40875226086ace1e24d6598d771d8a65a6938acb1`  
		Last Modified: Fri, 29 Sep 2023 04:44:19 GMT  
		Size: 62.5 MB (62469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e2ae33200141fd4607751bb457b645086a1410c32e8ed27a2e8817f64ecf5d`  
		Last Modified: Thu, 12 Oct 2023 23:26:59 GMT  
		Size: 160.9 MB (160908704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:72bb5ccd62a1f8aef48baac1f333e6a546767a3c0f8c1e61d5ee369e9d264cc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223131289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42819bc1cb600fe4c843e42886aa4f451ed2a88fb0f7adcd00612a93b462b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:24:12 GMT
COPY dir:826b274d38ec470bf9beb46977486da92a3347aff5fcb970deb82f445fd7f20e in / 
# Thu, 12 Oct 2023 22:24:13 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:20:21 GMT
ARG version=20.0.2.10-1
# Thu, 12 Oct 2023 23:20:49 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 12 Oct 2023 23:20:50 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:20:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:d503fbdb054df5fe68cd13e3abb40a519885fcda4fbaf301b0667ae8c1285f4f`  
		Last Modified: Tue, 03 Oct 2023 00:59:41 GMT  
		Size: 64.2 MB (64163711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c3acd8096f64e92105487b02b17b7295b82a30af65af6990439ef7043cea12`  
		Last Modified: Thu, 12 Oct 2023 23:31:07 GMT  
		Size: 159.0 MB (158967578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
