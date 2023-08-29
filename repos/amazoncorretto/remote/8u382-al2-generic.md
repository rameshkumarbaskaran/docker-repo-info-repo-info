## `amazoncorretto:8u382-al2-generic`

```console
$ docker pull amazoncorretto@sha256:49e4440032d1f4af91fa0ac75346827b673e26bffcb6b8caf5ab609176ff3fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u382-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9fc46d663c8530e6e5432b68ac3e8c83ae86902250e3eeaca54a659ee3c66e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138056932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a77c65494d61e071eb540703cbb3a1931b390f6fc0388e2cc5abb3b0df2caa6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:39:03 GMT
ARG version=1.8.0_382.b05-1
# Tue, 29 Aug 2023 19:39:23 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:39:24 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:39:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2777c08acd60bdc608943c816f90f481bd66683594a52f6a9338c94fb0dd386`  
		Last Modified: Tue, 29 Aug 2023 19:52:03 GMT  
		Size: 75.6 MB (75579654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u382-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:582fe18bbde93f0ed88c44e3b17b6438a98a67c4d34b478559edf3c461f7dbee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123752078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e30d6cf1800ccc01a678e65774bdc8fabae324604117175a5750f3eddc0288e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:06:26 GMT
ARG version=1.8.0_382.b05-1
# Tue, 29 Aug 2023 19:06:42 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 29 Aug 2023 19:06:43 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:06:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fa55c5082bb206f57cd8989ecad654c6a065d7edbc3380b023251441fc467f`  
		Last Modified: Tue, 29 Aug 2023 19:16:21 GMT  
		Size: 59.6 MB (59622084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
