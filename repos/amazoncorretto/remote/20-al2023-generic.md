## `amazoncorretto:20-al2023-generic`

```console
$ docker pull amazoncorretto@sha256:681119c7599dab3addb2dc71c7f51d87c9e62e203032a839b6f3563ded0b2cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2023-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b43dc62091290a3165fe33624616b5f04268d1daf2c32b852db56829449e3e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260589924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffc4599e6a3bce24919fe4550c688038601b25bd4b39e65498585220b5685ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:51:15 GMT
ARG version=20.0.2.10-1
# Sat, 23 Sep 2023 00:51:43 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Sat, 23 Sep 2023 00:51:44 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:51:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c289733dc48a8302b74dfd9eda42a3c5e4a6039817aae3334efb861c2d36ec`  
		Last Modified: Sat, 23 Sep 2023 01:03:42 GMT  
		Size: 208.2 MB (208213842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2023-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8b56d54aaca807361dd864e78a2fb23ec38b1e80fa4e22ec60654e8c26a14191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257615560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b5a1ccfc228c2c6d7e61c901eee84a752fc513960e6eb0f69846243cc94d10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:31 GMT
COPY dir:03fe38cdd5cc2f8a990979b08efd5210e06e9c3897e52ada3c6c1600d3c4dd2a in / 
# Sat, 23 Sep 2023 00:39:32 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:20:54 GMT
ARG version=20.0.2.10-1
# Sat, 23 Sep 2023 01:21:17 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Sat, 23 Sep 2023 01:21:20 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:21:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:154360ae54dfa1d6974917dc29086d4d678d1f640f9c2fe7a2152a2b7a62c6c1`  
		Last Modified: Thu, 21 Sep 2023 00:56:16 GMT  
		Size: 51.5 MB (51457152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ac30d721b8bd9f569da553033cb5a0d82d814d9f90fddcc2d62d9965987a1`  
		Last Modified: Sat, 23 Sep 2023 01:31:23 GMT  
		Size: 206.2 MB (206158408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
