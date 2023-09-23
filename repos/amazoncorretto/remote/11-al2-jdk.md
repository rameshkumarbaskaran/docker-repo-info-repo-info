## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:007ec87ab886d3ed734e992457002b651668d0d168713472dacb99cf22b4cd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fff8bbb42af4b2c39c0396c995cc077afe3a54c5ecc9d36a6ffdee9003289830
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210250900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051c170e42b66efbe551c220db95983305209909e197c124b510034641059cda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:25 GMT
COPY dir:a2da562c67b011c1b42effadc6ff06b6f82996c9f8d8c5778282cf441aac39a5 in / 
# Sat, 23 Sep 2023 00:20:25 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:41:29 GMT
ARG version=11.0.20.9-1
# Sat, 23 Sep 2023 00:42:06 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 00:42:06 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:42:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9aa850931a9d85a578215adaccd39361fe6ec5a8c81ead1837d4c5d43415b66b`  
		Last Modified: Mon, 18 Sep 2023 18:32:31 GMT  
		Size: 62.5 MB (62469678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690581237f4b99c2e5fb4449e509fbee80aa97b1152155f2a93096baeffee662`  
		Last Modified: Sat, 23 Sep 2023 00:57:52 GMT  
		Size: 147.8 MB (147781222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:81ecf13839f23ec7d13ce8c47f685c97df737c9a47c73c68dd82aca5a20faa75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209064725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954e399461b57d3adee5acf4ae59600055a011172e1c108a9e431c3b01248e49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:42:11 GMT
ARG version=11.0.20.9-1
# Fri, 08 Sep 2023 21:42:32 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 08 Sep 2023 21:42:33 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:42:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c9ca958d143c7af3c3a576bc2cc78206b0b882d65dc8ac65c21eb4ba5f51f0`  
		Last Modified: Fri, 08 Sep 2023 21:52:09 GMT  
		Size: 144.9 MB (144934731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
