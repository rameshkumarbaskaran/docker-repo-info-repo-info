## `amazoncorretto:20-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:042fa51f19b9e419822ac290840c4a333042d121e368b4979b0be7ab2dd19300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d6e4316d91fc912d475fc48fbb57dd38cae80b5e91e820f12f58501538e40324
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223377952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9984ae923c0a0d9cddadd2d71baf2df3b0dfc0d0429fa51a74074a49d8e48376`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:25 GMT
COPY dir:a2da562c67b011c1b42effadc6ff06b6f82996c9f8d8c5778282cf441aac39a5 in / 
# Sat, 23 Sep 2023 00:20:25 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:50:34 GMT
ARG version=20.0.2.10-1
# Sat, 23 Sep 2023 00:51:10 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 00:51:11 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:51:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:9aa850931a9d85a578215adaccd39361fe6ec5a8c81ead1837d4c5d43415b66b`  
		Last Modified: Mon, 18 Sep 2023 18:32:31 GMT  
		Size: 62.5 MB (62469678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87d431b98218fdc21fdcfc1a1f8315a5d0f52fb1194a57982321868250ff532`  
		Last Modified: Sat, 23 Sep 2023 01:03:02 GMT  
		Size: 160.9 MB (160908274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b531ff52ce642b9a4c0e15179c91ce4eee8a8cd0d1be567431c8d410a2e41395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223122794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1204be6c07ddd02d6334d2233113860787c6966ce86c8c460e4e40debdf3c6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:47 GMT
COPY dir:5885a696cc03fd82c0c021dd701725b8b1bc11902dc8789780147154a555ba2a in / 
# Sat, 23 Sep 2023 00:39:48 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:20:21 GMT
ARG version=20.0.2.10-1
# Sat, 23 Sep 2023 01:20:49 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 23 Sep 2023 01:20:51 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:20:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:0cd473df417d2282c9d0586281fb9293e3faf1fb6481fa584bac46295844f59e`  
		Last Modified: Mon, 18 Sep 2023 18:32:30 GMT  
		Size: 64.2 MB (64161861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732f7ae25422c2bd64a9bbcee7a788a49055dfe2e1c212bca862e3f77220fe86`  
		Last Modified: Sat, 23 Sep 2023 01:30:49 GMT  
		Size: 159.0 MB (158960933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
