## `amazoncorretto:19-al2-full`

```console
$ docker pull amazoncorretto@sha256:477d26c4c6b5b2f1895c5b26281e53f3880c188524054638ed552da766b2c01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:19-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:26f615cfee50efd08402fd9f35cf254c7af21646d47b116ff6954707793d98c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221884986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380109f38c3efa8deeca89b845cd12e05cf923c67895c0d6ef969f1aacb638c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:24 GMT
COPY dir:1fe253a28ffa7545ac05b2d6b2410c0b48083e8195b6557287b6a94e845122d3 in / 
# Fri, 10 Mar 2023 01:20:24 GMT
CMD ["/bin/bash"]
# Fri, 10 Mar 2023 01:40:22 GMT
ARG version=19.0.2.7-1
# Fri, 10 Mar 2023 01:40:45 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 10 Mar 2023 01:40:46 GMT
ENV LANG=C.UTF-8
# Fri, 10 Mar 2023 01:40:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:07e4d356f367b468402d36db62e60b734522576ce93a8e7246f1b36899c58f5e`  
		Last Modified: Thu, 09 Mar 2023 17:52:43 GMT  
		Size: 62.5 MB (62477005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07418909368483576e92d83eed35df62064232d12d3768e8df6811d624550a7a`  
		Last Modified: Fri, 10 Mar 2023 01:45:22 GMT  
		Size: 159.4 MB (159407981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:19-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:074a41c817f7105ea5ca497acd5e6f2cc1e6704b6fdd7a1d2271956110aa9d9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221978811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87764a74c3d957ec02ede7f61d5e20cd566b896c89aac914928eaadb94066fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:35 GMT
COPY dir:1997e4057e1f8b7df06806432d2b2c303c1f6ef5b18e8273d4393b867415d8b2 in / 
# Fri, 10 Mar 2023 01:39:36 GMT
CMD ["/bin/bash"]
# Fri, 10 Mar 2023 02:04:36 GMT
ARG version=19.0.2.7-1
# Fri, 10 Mar 2023 02:04:54 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 10 Mar 2023 02:04:56 GMT
ENV LANG=C.UTF-8
# Fri, 10 Mar 2023 02:04:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:042c9cfa8a36c0ffe86667a7dd7d488f78cbe295aa845213c01fdf8784165a92`  
		Last Modified: Fri, 10 Mar 2023 01:40:11 GMT  
		Size: 64.1 MB (64125204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e5bbfe81c1d8765bef145c6de9cbe0fa98bbc60365e6704f781812581df20b`  
		Last Modified: Fri, 10 Mar 2023 02:07:07 GMT  
		Size: 157.9 MB (157853607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
