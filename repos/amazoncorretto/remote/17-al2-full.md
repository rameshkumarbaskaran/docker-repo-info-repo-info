## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:f0a7e67fe3c53618d2ebfb73e10992e5b7fee1b73b3e4b304d02c0070f9e0ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32619464ab96220ccb9cf57f79ddcf2d27a9ca190d23d1b155b741fe23eca3d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213500563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82c8b99f010fdf9ce991cc63ed60879e5e8f35c94d7cc0485ab401375885f15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Mon, 25 Oct 2021 18:24:03 GMT
ARG version=17.0.1.12-1
# Mon, 25 Oct 2021 18:24:26 GMT
# ARGS: version=17.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 25 Oct 2021 18:24:27 GMT
ENV LANG=C.UTF-8
# Mon, 25 Oct 2021 18:24:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80f94f4a30a2bec83c6c2256573124c8dd3a24493fbdd6d14d65778f3172cc6`  
		Last Modified: Mon, 25 Oct 2021 18:27:05 GMT  
		Size: 151.5 MB (151524455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3edb0f6919cf7faa13121cc750337c732ffc1f7f72afc97e71068f603051f602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213744057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de60664a01d2f9cceba8b02b2d2b53618de8759a787fdea0f816b849b2323bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 16:54:30 GMT
ARG version=17.0.1.12-1
# Fri, 03 Dec 2021 16:54:47 GMT
# ARGS: version=17.0.1.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 03 Dec 2021 16:54:47 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 16:54:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca22289d3bc8d639ce9c21bc5edc611c4a87f936cdb6557abb4af42a1d431143`  
		Last Modified: Fri, 03 Dec 2021 16:56:46 GMT  
		Size: 150.1 MB (150051510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
