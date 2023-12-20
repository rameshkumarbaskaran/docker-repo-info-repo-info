## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:5ab1a8aacdc1b8ef23d062c851c19f4de90b10294641dab7cc16a22444370478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7737e93e7718a1a4aa9d0f22293133fafba258b21f25247c5bd242cb27e2cf08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138248447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae02625b53628fd07021da33863eefe546b3d746668e14255b4c6fc07800c3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:40 GMT
COPY dir:7964ac201a93d838933b1631de52186ab9a9c98f572a75fd024299ea94e621fa in / 
# Wed, 20 Dec 2023 08:49:41 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:23:43 GMT
ARG version=1.8.0_392.b08-1
# Wed, 20 Dec 2023 09:24:06 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Dec 2023 09:24:07 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:24:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:99e9b04a7dc206f4a47a0937a2039102066a5273ce57a11fa6894d90fe3957bc`  
		Last Modified: Wed, 20 Dec 2023 08:50:39 GMT  
		Size: 62.6 MB (62645506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb390d8979c2b8833a436211f4ecfa689ccf3fe01cd30343a39774736506c9`  
		Last Modified: Wed, 20 Dec 2023 09:37:22 GMT  
		Size: 75.6 MB (75602941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bf79a4907f04c37ff8e224a53dc62a0255212dbf294959df54372e9fbc17faac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124034573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def11a705b06e51ac12b4c9de39dbfa05dc8bea04b968b470c0e75b09d93d159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:23 GMT
COPY dir:380956fd469c5bff2cfd19545c66184d8301b431f1a3cd9c8338b2680a7f7a2b in / 
# Wed, 20 Dec 2023 01:32:24 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 01:56:00 GMT
ARG version=1.8.0_392.b08-1
# Wed, 20 Dec 2023 01:56:17 GMT
# ARGS: version=1.8.0_392.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Dec 2023 01:56:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 01:56:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1cdee3d784afc8dc3a31863ea6b75bfb24c3394d454dd5ca221d29fbd4c3f130`  
		Last Modified: Wed, 20 Dec 2023 01:32:56 GMT  
		Size: 64.4 MB (64445029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf586bf4b234c52d16445878b16df79ac70c1af822e0e75ba06fbb12928d9dd`  
		Last Modified: Wed, 20 Dec 2023 02:05:54 GMT  
		Size: 59.6 MB (59589544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
