## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
