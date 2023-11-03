## `amazoncorretto:11-al2-generic`

```console
$ docker pull amazoncorretto@sha256:470b09720563a5d0ff73f5542128825223670f81c383584220048c9e17b5fbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:99c0a453af9632171f6dda1b9c21d373771a6240135ce567a0da96d4ace79373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210569463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8611ac48630c791d6a2a8a88cef73f02af4e3d0b7464f93530ead4b334784d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:53 GMT
COPY dir:3e6cf913ede7c7c09de0465c096dad9a8bea883f026db356d68f0e799e2e3847 in / 
# Fri, 03 Nov 2023 22:21:53 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:41:45 GMT
ARG version=11.0.21.9-1
# Fri, 03 Nov 2023 22:42:10 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:42:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:42:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6ebddf7084e9402a3ba6cf1360703e12633f9c49f51772f99c298cd1048d728e`  
		Last Modified: Fri, 03 Nov 2023 11:40:21 GMT  
		Size: 62.6 MB (62646469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636990ccbef4dfc236792b8440e76d8bad27ebe5a7e271085b486f79f16ee517`  
		Last Modified: Fri, 03 Nov 2023 22:54:30 GMT  
		Size: 147.9 MB (147922994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d2168bddae33776b8d236e3657bdf1ba52f5c23f40fa61872635664ef097f761
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209413463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7882f3f3e3f7f768752fdf0cffd88378469e7476ae78341ea4c25fea9f943c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:57:53 GMT
ARG version=11.0.21.9-1
# Fri, 03 Nov 2023 22:58:11 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:58:13 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:58:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1caf17af52a0f5870773eff2466a3e46fd343129663aa68cfc416fa0dbd1ea`  
		Last Modified: Fri, 03 Nov 2023 23:08:27 GMT  
		Size: 145.0 MB (145033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
