## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:530ed98ce8d82d0405fecab6933190f30a4abba20eda2d6bbcf8f30fbf8e1f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:605efacf5e397e0bc4e53dd064b5378e88a4055f9189db796ce0a8adbd3dac20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228121628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bae5cdf7c35d26f53a7b2bfa4350a825a7ea128805bdeed5b185fdff26eeca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:53 GMT
COPY dir:3e6cf913ede7c7c09de0465c096dad9a8bea883f026db356d68f0e799e2e3847 in / 
# Fri, 03 Nov 2023 22:21:53 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:48:56 GMT
ARG version=21.0.1.12-1
# Fri, 03 Nov 2023 22:49:26 GMT
# ARGS: version=21.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 22:49:27 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:49:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6ebddf7084e9402a3ba6cf1360703e12633f9c49f51772f99c298cd1048d728e`  
		Last Modified: Fri, 03 Nov 2023 11:40:21 GMT  
		Size: 62.6 MB (62646469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf55775b2d1a4d4ae4a83622b994e1380b5953027c623bbc018b87ac1292059e`  
		Last Modified: Fri, 03 Nov 2023 22:59:50 GMT  
		Size: 165.5 MB (165475159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75fb1cd29c249da51d6aa44c89a9d0134d8f18e8ab3eb1efaf022ef24ba53279
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227858258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e863a2480e79ee762686f002d096623dc1c62e6d4e62679675fee97b18f38b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:03:33 GMT
ARG version=21.0.1.12-1
# Fri, 03 Nov 2023 23:03:52 GMT
# ARGS: version=21.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Nov 2023 23:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 23:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ab6ff395f3a905e4c0f87f9aeee8af9e3f2f856c144523a350b70104a94c01`  
		Last Modified: Fri, 03 Nov 2023 23:13:09 GMT  
		Size: 163.5 MB (163478055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
