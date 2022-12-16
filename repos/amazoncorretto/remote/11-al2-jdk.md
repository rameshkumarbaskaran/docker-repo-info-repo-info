## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:7c16097869e15a870cd48d24e91682d5d964e7221b3d77b49be2c3a5d34d8ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0e2f33bb26829a198dfd79eded0ca88284375e73322b3f9ed13eba69591ebf53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210031621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607f21ee6285afb5e32da35cc224fe7a5cf5a7008e7a56816f5fd6ac1b12ba9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:50:32 GMT
ARG version=11.0.17.8-1
# Thu, 17 Nov 2022 01:50:56 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:50:56 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:50:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef215ea8d074f0c94eaca01c6b06d36fb0f4c6fba48ee0ef78e27af949e1d2b`  
		Last Modified: Thu, 17 Nov 2022 01:55:26 GMT  
		Size: 147.8 MB (147769396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3070e9b57800dfb065e589addc5244e6f87d4d810eee7a2186a9f99149c417c4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208870138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26169c52bdb96d4502b677575e0eeab91bc8b3d8e6470a9b7befd656f0615c5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 00:59:23 GMT
ARG version=11.0.17.8-1
# Fri, 16 Dec 2022 00:59:42 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 00:59:44 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 00:59:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aade9a94f7c23d8fc79b4c11ce14d37b8569a6fec3017a295169ff500ec8d8`  
		Last Modified: Fri, 16 Dec 2022 01:03:43 GMT  
		Size: 144.9 MB (144905924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
