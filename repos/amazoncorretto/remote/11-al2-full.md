## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:7dcf8170225a8c7c528fec21cd9e6ecd048a6d776082fa6f3a17bd7a6e46ad18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:95a6191f10ac7cbfa0d61b39254837f23091975406b1485fa937fe8730467432
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209752215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a3506a5a41167125633212f978be153cdc4506f46ae4be32e000192a4a97f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 03:00:00 GMT
ARG version=11.0.16.8-1
# Fri, 12 Aug 2022 03:00:34 GMT
# ARGS: version=11.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Aug 2022 03:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Aug 2022 03:00:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03998099518a939dc747f777d8e43d6794e0162d7c78e4ce8345302f79532756`  
		Last Modified: Fri, 12 Aug 2022 03:04:21 GMT  
		Size: 147.4 MB (147435999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d8427f53baedc688e939d63a287364623f95ab2afe9228c781862ce4600affc4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208477177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83521579e5cb37fb728e9b36afafb988d4f419ae99cf1fef148a85fd6b2ba1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 23:39:32 GMT
ADD file:ce3840583311a5848d47c22463b3a966c40bbf4824f1c9b9b2c51e2fb939de3a in / 
# Tue, 21 Jun 2022 23:39:33 GMT
CMD ["/bin/bash"]
# Wed, 20 Jul 2022 06:01:07 GMT
ARG version=11.0.16.8-1
# Wed, 20 Jul 2022 06:01:21 GMT
# ARGS: version=11.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Jul 2022 06:01:21 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 06:01:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8cd18ebacb4abd924911c002d3ec5b8d76247c7ed5fff822c8cfb3961846f05a`  
		Last Modified: Wed, 15 Jun 2022 22:09:35 GMT  
		Size: 63.9 MB (63918642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fb9d3d0781011380d35b4add2ba8fa609ab9311980da8bba30fe71049c5c23`  
		Last Modified: Wed, 20 Jul 2022 06:03:44 GMT  
		Size: 144.6 MB (144558535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
