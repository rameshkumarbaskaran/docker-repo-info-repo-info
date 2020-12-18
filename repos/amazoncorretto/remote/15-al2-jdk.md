## `amazoncorretto:15-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:2ddc1907db80b125739883bd84a84b976f28b89bdc0724c0901096fb01ed5b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ec851bbaaff7e97cc0a84c07b8ca6c7d6ad223cdaea3c21534090cf7bf712b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8760ee01cbb0a508b643f32f2b2c64c391e03cbe40200cd4ee5a2e9365db0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:27:26 GMT
ARG version=15.0.1.9-1
# Fri, 18 Dec 2020 09:27:48 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a962697c7bb711e82ff306efdb1e23f54cb3a73308995bcee1ef0986d86a7`  
		Last Modified: Fri, 18 Dec 2020 09:29:36 GMT  
		Size: 155.7 MB (155663879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-jdk` - linux; arm64 variant v8

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
