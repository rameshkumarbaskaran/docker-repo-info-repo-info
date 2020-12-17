## `amazoncorretto:15-al2-full`

```console
$ docker pull amazoncorretto@sha256:b1346650a3a3597016c660fc614ff82f0ab3b992f0c47aa69b19464e6f05a69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8de06d3a5c0cd1c69bf18730214f5f23cfa0bc6745ed1dc53fb1c851add1b9d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987efd713809d9d86d659d999e9c17a840553850d1d59f45724ff6de9cf925bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 31 Jul 2020 22:19:45 GMT
ADD file:92220f428664788288d5cda805c94b48f6a5e957d4c7724085f3278d0a864f6d in / 
# Fri, 31 Jul 2020 22:19:46 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 00:20:38 GMT
ARG version=15.0.1.9-1
# Wed, 28 Oct 2020 00:21:04 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 28 Oct 2020 00:21:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Oct 2020 00:21:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:37373184fe69e0fc20370c26317bf4c5b9b843c60b375563d4ee1c7766a89782`  
		Last Modified: Fri, 31 Jul 2020 22:20:37 GMT  
		Size: 61.7 MB (61716540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f63bb5d5eb2077eabce2a847bd08bfed17d34b549ba4b4839b065a377194a54`  
		Last Modified: Wed, 28 Oct 2020 00:22:52 GMT  
		Size: 155.6 MB (155631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:028ea8f8304dcb94b0ba23bd9860452105445c73ffe5f6150d68600fb0606a4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219211194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0acb2c1b4c67bf5caf166a4f4938c2fe13b7d800de9c7b6a35d25b878cae89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:43 GMT
ARG version=15.0.1.9-1
# Thu, 17 Dec 2020 23:08:12 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:08:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabd893f46c6ff949915ab59c407c77ae779a5ca21dbb49b0f5fe0d40bf34cb`  
		Last Modified: Thu, 17 Dec 2020 23:10:20 GMT  
		Size: 155.5 MB (155535494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
