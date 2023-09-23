## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:7a66c1812f9d13b1bf6dde0ad427d11126523ae101ffcae58f5ee1c0418a083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05c1cabf48830427ea6e6f376b31016702a0a3d48fc6f809af8d98631197d364
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227876477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffed29b826ac7cbdf1839316581b9c49371a9da7b2af80d115d9cbb63a8d8d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:25 GMT
COPY dir:a2da562c67b011c1b42effadc6ff06b6f82996c9f8d8c5778282cf441aac39a5 in / 
# Sat, 23 Sep 2023 00:20:25 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:51:58 GMT
ARG version=21.0.0.35-1
# Sat, 23 Sep 2023 00:52:35 GMT
# ARGS: version=21.0.0.35-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 00:52:36 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:52:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9aa850931a9d85a578215adaccd39361fe6ec5a8c81ead1837d4c5d43415b66b`  
		Last Modified: Mon, 18 Sep 2023 18:32:31 GMT  
		Size: 62.5 MB (62469678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0724b3f6613877623136c451ccd11ab13bd72a60d9a135966b61ba46eadae`  
		Last Modified: Sat, 23 Sep 2023 01:04:17 GMT  
		Size: 165.4 MB (165406799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6ed4890ca33bf3cb783f32ff2c5ca543f09a370978aa55a74a21d030e87eaad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227556390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7a51e5df1ea179ab2163df5d40ebe9d368b3652d85163f6cb28f499799e13f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 00:41:55 GMT
ARG version=21.0.0.35-1
# Fri, 22 Sep 2023 00:42:25 GMT
# ARGS: version=21.0.0.35-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Sep 2023 00:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 22 Sep 2023 00:42:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767eee88b4ae7a157734359dc319f9c169d69214a709f5a6f261e10541616792`  
		Last Modified: Fri, 22 Sep 2023 00:46:34 GMT  
		Size: 163.4 MB (163426396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
