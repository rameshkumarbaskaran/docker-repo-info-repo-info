## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:d7f69338d3cb2e1b8c136ee3b9815ca8f1fe23305c2052d3c5b43ef74660c718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11db63d4886ec89e362d954a5284741d9f2c406d05fa8ca45c770d52b269a783
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137889968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c1e1965a0588cdf58b32ccfb103843e231bb6657204aa2ef24827e669c1547`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 02:59:13 GMT
ARG version=1.8.0_342.b07-4
# Fri, 12 Aug 2022 02:59:39 GMT
# ARGS: version=1.8.0_342.b07-4
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Aug 2022 02:59:39 GMT
ENV LANG=C.UTF-8
# Fri, 12 Aug 2022 02:59:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2ed3f8d08aa74e8f95ecdbb438976bc6be9725b4cfd8226c0951916bad35f2`  
		Last Modified: Fri, 12 Aug 2022 03:03:40 GMT  
		Size: 75.6 MB (75573752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1f297325ea6cab3a93c4e38545c3e4c3d4719ba1c3dd6c0a806b21922a7f4c4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123521027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11a26019f9240a0f6b4386a6f83af44a4b237e833775bd325f0bccf96a2507d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 23:39:32 GMT
ADD file:ce3840583311a5848d47c22463b3a966c40bbf4824f1c9b9b2c51e2fb939de3a in / 
# Tue, 21 Jun 2022 23:39:33 GMT
CMD ["/bin/bash"]
# Fri, 29 Jul 2022 19:39:24 GMT
ARG version=1.8.0_342.b07-4
# Fri, 29 Jul 2022 19:39:39 GMT
# ARGS: version=1.8.0_342.b07-4
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 29 Jul 2022 19:39:39 GMT
ENV LANG=C.UTF-8
# Fri, 29 Jul 2022 19:39:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8cd18ebacb4abd924911c002d3ec5b8d76247c7ed5fff822c8cfb3961846f05a`  
		Last Modified: Wed, 15 Jun 2022 22:09:35 GMT  
		Size: 63.9 MB (63918642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8f60aacf01af6baad600fbdc1827a45e57f77af3ecffb101b18e8231622bdb`  
		Last Modified: Fri, 29 Jul 2022 19:40:52 GMT  
		Size: 59.6 MB (59602385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
