## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:76be0bb09a7bb37ff8eceb1c62d919ecdc1b09d9ccde42e32a3367219594db40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8cddf00a8b4da53f629a98e3c8b673ba54ab799ffb2710a0aab5b9e61ae63fd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214613608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ce665d81acad945d2910b42909bc721dcef40a4332057e873cbebe5ddba998`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:40 GMT
COPY dir:7964ac201a93d838933b1631de52186ab9a9c98f572a75fd024299ea94e621fa in / 
# Wed, 20 Dec 2023 08:49:41 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:30:09 GMT
ARG version=17.0.9.8-1
# Wed, 20 Dec 2023 09:30:34 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Dec 2023 09:30:35 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:30:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:99e9b04a7dc206f4a47a0937a2039102066a5273ce57a11fa6894d90fe3957bc`  
		Last Modified: Wed, 20 Dec 2023 08:50:39 GMT  
		Size: 62.6 MB (62645506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0963e6073ac3f065213a0c60697c42bd1af142580e566bff53976320118487`  
		Last Modified: Wed, 20 Dec 2023 09:41:46 GMT  
		Size: 152.0 MB (151968102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9732099102c7c60ee3b4370049670b676b6c4d7851f9cb0f50e81f5a1fd56804
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214945103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7358ae197b3f8f608c8796495e22ba216d4fe28b2b0296347fad52de7cbad58b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:23 GMT
COPY dir:380956fd469c5bff2cfd19545c66184d8301b431f1a3cd9c8338b2680a7f7a2b in / 
# Wed, 20 Dec 2023 01:32:24 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 02:00:07 GMT
ARG version=17.0.9.8-1
# Wed, 20 Dec 2023 02:00:26 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Dec 2023 02:00:28 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:00:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1cdee3d784afc8dc3a31863ea6b75bfb24c3394d454dd5ca221d29fbd4c3f130`  
		Last Modified: Wed, 20 Dec 2023 01:32:56 GMT  
		Size: 64.4 MB (64445029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035eedf641b19325430a856835c0a575fc233850e274dd401e276392336d1a42`  
		Last Modified: Wed, 20 Dec 2023 02:09:30 GMT  
		Size: 150.5 MB (150500074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
