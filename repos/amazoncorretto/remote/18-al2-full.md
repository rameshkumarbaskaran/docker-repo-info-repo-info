## `amazoncorretto:18-al2-full`

```console
$ docker pull amazoncorretto@sha256:1128cff77f7fb4512215a4ded2bf0a6ec3cd2bf0f414a72136b1bb1d5f6b0518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:18-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93f471ef631d67bbfa043e077381c0b702e95f2491dac80757b48d1011a64546
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215005549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79453c969606ced150e58269b6a1071034c5f3ab68473c37308b66b14075d21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 01:10:09 GMT
ARG version=18.0.2.9-1
# Fri, 21 Oct 2022 01:10:34 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 21 Oct 2022 01:10:35 GMT
ENV LANG=C.UTF-8
# Fri, 21 Oct 2022 01:10:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd810cad0bdf6453bee2dabf5abe8def538559a37f10dd606b86c1a61d9247`  
		Last Modified: Fri, 21 Oct 2022 01:15:45 GMT  
		Size: 152.7 MB (152698907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:18-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:37f6b76c24b03ab5c93bbb1af157a6b15a45fbfe6c9be1585c47c035810de19c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215264403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a00c689f36ea46db3092bbe6ef346107d8026aa6d2e0499a412e57a66abfee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Oct 2022 23:39:31 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Thu, 20 Oct 2022 23:39:32 GMT
CMD ["/bin/bash"]
# Thu, 20 Oct 2022 23:57:52 GMT
ARG version=18.0.2.9-1
# Thu, 20 Oct 2022 23:58:04 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Oct 2022 23:58:05 GMT
ENV LANG=C.UTF-8
# Thu, 20 Oct 2022 23:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d79b74e04609c53b3251846bbfc91daae1e1e0143fa7547e36c706d8b4c63c`  
		Last Modified: Fri, 21 Oct 2022 00:01:21 GMT  
		Size: 151.3 MB (151344534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
