## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:582fbf5a116eca7e2f9d1bc0e1888e121eebb980e929270c28f8e6a33fea2d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2-jdk` - linux; amd64

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

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:09282fab4d28a944d8ee4b4290f05f827c227647acd23eb575a78d9345c128ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227579801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d1fa2374e54f427d9e91d8b8879fb70584e5a0fb194d32cd3b18a636a4f771`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:47 GMT
COPY dir:5885a696cc03fd82c0c021dd701725b8b1bc11902dc8789780147154a555ba2a in / 
# Sat, 23 Sep 2023 00:39:48 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:21:28 GMT
ARG version=21.0.0.35-1
# Sat, 23 Sep 2023 01:21:57 GMT
# ARGS: version=21.0.0.35-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 01:21:59 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:21:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0cd473df417d2282c9d0586281fb9293e3faf1fb6481fa584bac46295844f59e`  
		Last Modified: Mon, 18 Sep 2023 18:32:30 GMT  
		Size: 64.2 MB (64161861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c7a6981e61245ecb44e9bb9700f8aeac7de20dbfaafa6359fd5f6c47a78ba9`  
		Last Modified: Sat, 23 Sep 2023 01:31:53 GMT  
		Size: 163.4 MB (163417940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
