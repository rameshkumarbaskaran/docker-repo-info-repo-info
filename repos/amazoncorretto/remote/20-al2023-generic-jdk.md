## `amazoncorretto:20-al2023-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:9535d3d6478ef23cd0ed2b6d535af64016f35cd88d6e26684a1b5f711835aa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2023-generic-jdk` - linux; amd64

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

### `amazoncorretto:20-al2023-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c84f6ab0349ff930ef6729328a9132bb9e7956c42b6c7f6edf4c0d28b10f42b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257444338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe67ce18cef280ab825de1b26eeac93cfe7319be9fd645d09f8c945509e5f11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:40:45 GMT
COPY dir:0004a2667b3e5dc5080ba46954457d05835caf07f7030d94b953f1c3cede9b0c in / 
# Tue, 29 Aug 2023 18:40:47 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:49:23 GMT
ARG version=20.0.2.10-1
# Fri, 08 Sep 2023 21:49:47 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Fri, 08 Sep 2023 21:49:50 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:49:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:8e2acd49419010bc77a61e38a85963f09e403f004635f24c436d177a08df1040`  
		Last Modified: Sat, 26 Aug 2023 03:06:10 GMT  
		Size: 51.3 MB (51324150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519715d08dc2b6582a23a1ccc00d08a45d0430fe1d04afc01b5802072861fef`  
		Last Modified: Fri, 08 Sep 2023 22:00:07 GMT  
		Size: 206.1 MB (206120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
