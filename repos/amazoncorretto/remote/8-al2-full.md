## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:52467193e6f446a3bbe6172f9a2f314f3acd2792a794fddff3d3f44a9e4c7e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:36ede9ee499243c633c9f1a564d6e6778bcecc0a1dd54ac04f6e3b2c5edededb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137228963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2504e87fa9a72b931331c3a8896094bace65ae2a2315d1e299d6296299313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 24 Feb 2021 19:19:48 GMT
ADD file:40bc6ac9b95149d9077e8e692feea2208fcd1c5883673953b295e6acd014ea38 in / 
# Wed, 24 Feb 2021 19:19:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Mar 2021 01:19:26 GMT
ARG version=1.8.0_282.b08-1
# Thu, 18 Mar 2021 01:19:40 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 18 Mar 2021 01:19:40 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:19:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9da98c321efd693e1dc19cc24c7c2cfa365c649f178da8ebdfdc5243d0b2f91a`  
		Last Modified: Wed, 24 Feb 2021 10:37:31 GMT  
		Size: 61.9 MB (61935160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376e88159f3d6c2882e0ed403c2a5a0c9e9deb0bd43bed9e388ce2f142ef7534`  
		Last Modified: Thu, 18 Mar 2021 01:22:53 GMT  
		Size: 75.3 MB (75293803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:eb475220da1f317ef658e22e64175c2d264b097cfb0d40908cd2575797dfc37f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123024874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab53f79844d085ce1843d2fe1dff6ed40d75d11322fdf65aa7b3fee4bf08545`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:58 GMT
ADD file:540e42c4903b87925bc490b00820f555e531041d1b1fcea6ee56f4cc3bbc895d in / 
# Tue, 30 Mar 2021 22:00:02 GMT
CMD ["/bin/bash"]
# Wed, 31 Mar 2021 14:31:04 GMT
ARG version=1.8.0_282.b08-1
# Wed, 31 Mar 2021 14:31:37 GMT
# ARGS: version=1.8.0_282.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 31 Mar 2021 14:31:39 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 14:31:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7d8296f22a3c3f786ce15fb5be7dce44af09932e617f9a981183619985014031`  
		Last Modified: Tue, 30 Mar 2021 22:01:09 GMT  
		Size: 63.7 MB (63660038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25605f6c77fc13bff20fc61e4a04b20bfbc4458861d5faacafb5bbc953eaa766`  
		Last Modified: Wed, 31 Mar 2021 14:34:29 GMT  
		Size: 59.4 MB (59364836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
