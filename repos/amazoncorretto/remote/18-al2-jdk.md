## `amazoncorretto:18-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:322a3ba5ec7983180ab7feecfe4d9fb281dfac4b3e987074d8b3b32c20b77eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:18-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:faa6b673f59e9e0442cb846a8c8802ed6ec6fe2eeed296773de67567ebafdaab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215014747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d981e22f2b92a8232b18bd968fc3821f665dfd476b269928a323282d3db3227`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 03:01:29 GMT
ARG version=18.0.2.9-1
# Fri, 12 Aug 2022 03:01:55 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 12 Aug 2022 03:01:56 GMT
ENV LANG=C.UTF-8
# Fri, 12 Aug 2022 03:01:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188a28cedc43dd2a2fb4b59c6bc7b5a07186690557cfb49f2750f1378654b259`  
		Last Modified: Fri, 12 Aug 2022 03:05:34 GMT  
		Size: 152.7 MB (152698531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:18-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a4cac4cf942d8c8979139ffb6a4920530aa5e66caa4e5ee3d0eaa710eb6d6007
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215270964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b4f2bd2372d7f7bd58e12f2364d5a381760edfa4fb9fec93f65fa53fd72692`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 23:39:32 GMT
ADD file:ce3840583311a5848d47c22463b3a966c40bbf4824f1c9b9b2c51e2fb939de3a in / 
# Tue, 21 Jun 2022 23:39:33 GMT
CMD ["/bin/bash"]
# Wed, 20 Jul 2022 06:01:54 GMT
ARG version=18.0.2.9-1
# Wed, 20 Jul 2022 06:02:13 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Jul 2022 06:02:13 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 06:02:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:8cd18ebacb4abd924911c002d3ec5b8d76247c7ed5fff822c8cfb3961846f05a`  
		Last Modified: Wed, 15 Jun 2022 22:09:35 GMT  
		Size: 63.9 MB (63918642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bc5f828d044d382ed3806efb3ad9219b30d4bda213a4ca8897a42940755c10`  
		Last Modified: Wed, 20 Jul 2022 06:04:54 GMT  
		Size: 151.4 MB (151352322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
