## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:101477838542c0783d8fc4d6d182a442ad0bee0cdc6e5091f832a9f843685d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8d6f82f312b32c4b47d4356ce354e7a04f230176206d715be3587f04fa910c61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214186030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e4e722eb3e4f4bd8a25cc5944407a385bc991718951b2f9057d340492ee7bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:51:16 GMT
ARG version=17.0.5.8-1
# Thu, 17 Nov 2022 01:51:40 GMT
# ARGS: version=17.0.5.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:51:41 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:51:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d137d23130653f2307ef578a322d90337873796341997aae991c075dac9870e8`  
		Last Modified: Thu, 17 Nov 2022 01:56:06 GMT  
		Size: 151.9 MB (151923805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ad4248e3089a39eb7124dc44425e6a6fb75519355b00a1728690d610774b8e2c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214414779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf8a548dd9c790ea163b80bb75c9c9ae292a44f89b403a06b47abfb3c2d2a76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:00:39 GMT
ARG version=17.0.5.8-1
# Fri, 16 Dec 2022 01:00:58 GMT
# ARGS: version=17.0.5.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Dec 2022 01:00:59 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 01:00:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11aa0c7a3bd8ae851a9908ba8d42e08746088a1d711999259f963258799e85c`  
		Last Modified: Fri, 16 Dec 2022 01:05:04 GMT  
		Size: 150.5 MB (150450565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
