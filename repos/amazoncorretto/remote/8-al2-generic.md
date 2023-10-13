## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:dbbedd1373340e2aa4a7cbcb42d65a7946e01fb2c8cbd5b6d8325de6ea892a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:135fc7efe86982c0d7aa1a7cf0ad807bfbf90f0ba9b2519ce204cde139d35235
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138016594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95809c4381923c59880002edfd08a18e69fa4cdc044dc6e973060b89d4173351`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:38:11 GMT
COPY dir:bba3c324992ed0e5d34f0f5796fe9c0e46ced00dc01939b98cad3bc355594b38 in / 
# Thu, 12 Oct 2023 22:38:11 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:02:00 GMT
ARG version=1.8.0_382.b05-1
# Thu, 12 Oct 2023 23:02:34 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 12 Oct 2023 23:02:35 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:02:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2b92a4a464539d6c28ffd6b40875226086ace1e24d6598d771d8a65a6938acb1`  
		Last Modified: Fri, 29 Sep 2023 04:44:19 GMT  
		Size: 62.5 MB (62469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24257d040582222853d6094dcc978441cf1520d7ac27c3d36abe44c7cb3fe33`  
		Last Modified: Thu, 12 Oct 2023 23:19:44 GMT  
		Size: 75.5 MB (75546949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d6ed851b013b89b875fd0e8147ce96fc83750d28ae0b6ff6261c9a593cbb015e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123766448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2277f576fd564c2241cf6550b3415a04ec885d5ddcd6f079a13ef4715e3ba312`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:24:12 GMT
COPY dir:826b274d38ec470bf9beb46977486da92a3347aff5fcb970deb82f445fd7f20e in / 
# Thu, 12 Oct 2023 22:24:13 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:11:40 GMT
ARG version=1.8.0_382.b05-1
# Thu, 12 Oct 2023 23:12:05 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 12 Oct 2023 23:12:06 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:12:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d503fbdb054df5fe68cd13e3abb40a519885fcda4fbaf301b0667ae8c1285f4f`  
		Last Modified: Tue, 03 Oct 2023 00:59:41 GMT  
		Size: 64.2 MB (64163711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d7437ea8e14492f712a44b7637d4795d32ad72c614516e9556ac0a7a25379b`  
		Last Modified: Thu, 12 Oct 2023 23:24:55 GMT  
		Size: 59.6 MB (59602737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
