## `amazoncorretto:20-al2-full`

```console
$ docker pull amazoncorretto@sha256:ee82a5b29166180b1bb5af975f938ae427e33acf47c43ba4bd9776189d921398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:09187f6b2c9c56fb78771a0e513da4ed9deb7041dfc58fea791c1dc4cbfb1635
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223256576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f60acbeb49b2f071e00482f21dd81c88e279cc4e8c42bc422400dd05589ab72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 19:20:11 GMT
COPY dir:1ad47ba01d0d349e7e7d7ca6f7f5a60739b61c1a0bb68b6f66605d9af77bb0d5 in / 
# Mon, 05 Jun 2023 19:20:12 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:41:56 GMT
ARG version=20.0.1.9-1
# Mon, 05 Jun 2023 19:42:19 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 05 Jun 2023 19:42:20 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:42:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:a168ccb1c126cd9267eedd2686bc6d0e5415b7fe1009cd832c78ba00655a34d9`  
		Last Modified: Wed, 24 May 2023 21:22:43 GMT  
		Size: 62.5 MB (62493087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50472d35bcaf1dac70c662dbd806d8ddd2cd1ce134dfcef4c0139613607e13`  
		Last Modified: Mon, 05 Jun 2023 19:47:37 GMT  
		Size: 160.8 MB (160763489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c89e43d733b0ff6b32dfde2b48b3c2ba1f3156f0d95c5c2ed0892eb6d15c3a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222916756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5980e07732b96a531f69f320af5957e5f2fab61bbb47d128f5292094193f0f2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 19:39:49 GMT
COPY dir:dfd59a801cb05cf6d9b2d75085c49494763e9b18842c146030985cf41b66d3ca in / 
# Mon, 05 Jun 2023 19:39:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:59:09 GMT
ARG version=20.0.1.9-1
# Mon, 05 Jun 2023 19:59:29 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 05 Jun 2023 19:59:31 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:59:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:d916dc829437e3254e7c7e665dd90678298358e7fb563161caa849ca46390827`  
		Last Modified: Wed, 24 May 2023 23:14:13 GMT  
		Size: 64.1 MB (64136791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba14e8e7588270a2605d46eb72f5f563cb7ad6f124b2183030b978070a57b6b`  
		Last Modified: Mon, 05 Jun 2023 20:04:20 GMT  
		Size: 158.8 MB (158779965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
