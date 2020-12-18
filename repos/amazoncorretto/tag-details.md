<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazoncorretto`

-	[`amazoncorretto:11`](#amazoncorretto11)
-	[`amazoncorretto:11.0.9`](#amazoncorretto1109)
-	[`amazoncorretto:11.0.9-al2`](#amazoncorretto1109-al2)
-	[`amazoncorretto:11.0.9-alpine`](#amazoncorretto1109-alpine)
-	[`amazoncorretto:11-al2-full`](#amazoncorretto11-al2-full)
-	[`amazoncorretto:11-al2-jdk`](#amazoncorretto11-al2-jdk)
-	[`amazoncorretto:11-alpine`](#amazoncorretto11-alpine)
-	[`amazoncorretto:11-alpine-full`](#amazoncorretto11-alpine-full)
-	[`amazoncorretto:11-alpine-jdk`](#amazoncorretto11-alpine-jdk)
-	[`amazoncorretto:15`](#amazoncorretto15)
-	[`amazoncorretto:15.0.1`](#amazoncorretto1501)
-	[`amazoncorretto:15.0.1-al2`](#amazoncorretto1501-al2)
-	[`amazoncorretto:15.0.1-alpine`](#amazoncorretto1501-alpine)
-	[`amazoncorretto:15-al2-full`](#amazoncorretto15-al2-full)
-	[`amazoncorretto:15-al2-jdk`](#amazoncorretto15-al2-jdk)
-	[`amazoncorretto:15-alpine`](#amazoncorretto15-alpine)
-	[`amazoncorretto:15-alpine-full`](#amazoncorretto15-alpine-full)
-	[`amazoncorretto:15-alpine-jdk`](#amazoncorretto15-alpine-jdk)
-	[`amazoncorretto:8`](#amazoncorretto8)
-	[`amazoncorretto:8-al2-full`](#amazoncorretto8-al2-full)
-	[`amazoncorretto:8-al2-jdk`](#amazoncorretto8-al2-jdk)
-	[`amazoncorretto:8-alpine`](#amazoncorretto8-alpine)
-	[`amazoncorretto:8-alpine-full`](#amazoncorretto8-alpine-full)
-	[`amazoncorretto:8-alpine-jdk`](#amazoncorretto8-alpine-jdk)
-	[`amazoncorretto:8-alpine-jre`](#amazoncorretto8-alpine-jre)
-	[`amazoncorretto:8u275`](#amazoncorretto8u275)
-	[`amazoncorretto:8u275-al2`](#amazoncorretto8u275-al2)
-	[`amazoncorretto:8u275-alpine`](#amazoncorretto8u275-alpine)
-	[`amazoncorretto:8u275-alpine-jre`](#amazoncorretto8u275-alpine-jre)
-	[`amazoncorretto:latest`](#amazoncorrettolatest)

## `amazoncorretto:11`

```console
$ docker pull amazoncorretto@sha256:80198fcd9c159a94625ef7cb7337d40923d1f6eaee2418dd472f4e9e9c04c63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7a0d16921b93517fb9519a97b0c9e5dd0f0fdbde5e5751d2ae40f8af709937a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208475715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449c6b5fb3b12fe894b363487d41cc26d1cb25acc3baa4dfe3f2f5e00e32f1cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:54 GMT
ARG version=11.0.9.12-1
# Fri, 18 Dec 2020 09:27:11 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa4d5051eccba8a34b0c5943e7d3af1b699630442bcab5c4e6327140c73b25f`  
		Last Modified: Fri, 18 Dec 2020 09:29:06 GMT  
		Size: 146.5 MB (146467196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57edd843ac8e146169033b76a9449ae70b2d9e5af686c8efb213cb908c0277d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208173169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858d2f8c29c1b3513dfaca2be02bfa1161a7c310d3a9e2ec7a19c149f5b90b99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:06 GMT
ARG version=11.0.9.12-1
# Thu, 17 Dec 2020 23:07:34 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f87068084c62f6785078d6926dbd1770554b01e03da0bd3aadf6343dae011f`  
		Last Modified: Thu, 17 Dec 2020 23:09:37 GMT  
		Size: 144.5 MB (144497469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.9`

```console
$ docker pull amazoncorretto@sha256:80198fcd9c159a94625ef7cb7337d40923d1f6eaee2418dd472f4e9e9c04c63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.9` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7a0d16921b93517fb9519a97b0c9e5dd0f0fdbde5e5751d2ae40f8af709937a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208475715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449c6b5fb3b12fe894b363487d41cc26d1cb25acc3baa4dfe3f2f5e00e32f1cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:54 GMT
ARG version=11.0.9.12-1
# Fri, 18 Dec 2020 09:27:11 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa4d5051eccba8a34b0c5943e7d3af1b699630442bcab5c4e6327140c73b25f`  
		Last Modified: Fri, 18 Dec 2020 09:29:06 GMT  
		Size: 146.5 MB (146467196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.9` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57edd843ac8e146169033b76a9449ae70b2d9e5af686c8efb213cb908c0277d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208173169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858d2f8c29c1b3513dfaca2be02bfa1161a7c310d3a9e2ec7a19c149f5b90b99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:06 GMT
ARG version=11.0.9.12-1
# Thu, 17 Dec 2020 23:07:34 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f87068084c62f6785078d6926dbd1770554b01e03da0bd3aadf6343dae011f`  
		Last Modified: Thu, 17 Dec 2020 23:09:37 GMT  
		Size: 144.5 MB (144497469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.9-al2`

```console
$ docker pull amazoncorretto@sha256:80198fcd9c159a94625ef7cb7337d40923d1f6eaee2418dd472f4e9e9c04c63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11.0.9-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7a0d16921b93517fb9519a97b0c9e5dd0f0fdbde5e5751d2ae40f8af709937a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208475715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449c6b5fb3b12fe894b363487d41cc26d1cb25acc3baa4dfe3f2f5e00e32f1cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:54 GMT
ARG version=11.0.9.12-1
# Fri, 18 Dec 2020 09:27:11 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa4d5051eccba8a34b0c5943e7d3af1b699630442bcab5c4e6327140c73b25f`  
		Last Modified: Fri, 18 Dec 2020 09:29:06 GMT  
		Size: 146.5 MB (146467196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11.0.9-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57edd843ac8e146169033b76a9449ae70b2d9e5af686c8efb213cb908c0277d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208173169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858d2f8c29c1b3513dfaca2be02bfa1161a7c310d3a9e2ec7a19c149f5b90b99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:06 GMT
ARG version=11.0.9.12-1
# Thu, 17 Dec 2020 23:07:34 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f87068084c62f6785078d6926dbd1770554b01e03da0bd3aadf6343dae011f`  
		Last Modified: Thu, 17 Dec 2020 23:09:37 GMT  
		Size: 144.5 MB (144497469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11.0.9-alpine`

```console
$ docker pull amazoncorretto@sha256:76acd2ab267cb71abeab875af97d91fb483d81bc4e372d1dd28bad32d8ccd693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11.0.9-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ad16f7b90421b975a18429d141c94895cd4fe1d4489bc610d53cf7e18ecf4527
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194996787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10971533e52923f349ed175ba9841881fb4d18cee46d345c854debb6093601e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:23 GMT
ARG version=11.0.9.12.1
# Thu, 17 Dec 2020 00:50:30 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 17 Dec 2020 00:50:30 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63066bc434b60a2bf6ab277b7713d0cdf8436126ed3ad4fc88a7c72d79e7070c`  
		Last Modified: Thu, 17 Dec 2020 00:52:24 GMT  
		Size: 192.2 MB (192197721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:80198fcd9c159a94625ef7cb7337d40923d1f6eaee2418dd472f4e9e9c04c63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7a0d16921b93517fb9519a97b0c9e5dd0f0fdbde5e5751d2ae40f8af709937a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208475715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449c6b5fb3b12fe894b363487d41cc26d1cb25acc3baa4dfe3f2f5e00e32f1cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:54 GMT
ARG version=11.0.9.12-1
# Fri, 18 Dec 2020 09:27:11 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa4d5051eccba8a34b0c5943e7d3af1b699630442bcab5c4e6327140c73b25f`  
		Last Modified: Fri, 18 Dec 2020 09:29:06 GMT  
		Size: 146.5 MB (146467196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57edd843ac8e146169033b76a9449ae70b2d9e5af686c8efb213cb908c0277d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208173169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858d2f8c29c1b3513dfaca2be02bfa1161a7c310d3a9e2ec7a19c149f5b90b99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:06 GMT
ARG version=11.0.9.12-1
# Thu, 17 Dec 2020 23:07:34 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f87068084c62f6785078d6926dbd1770554b01e03da0bd3aadf6343dae011f`  
		Last Modified: Thu, 17 Dec 2020 23:09:37 GMT  
		Size: 144.5 MB (144497469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:80198fcd9c159a94625ef7cb7337d40923d1f6eaee2418dd472f4e9e9c04c63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7a0d16921b93517fb9519a97b0c9e5dd0f0fdbde5e5751d2ae40f8af709937a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208475715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449c6b5fb3b12fe894b363487d41cc26d1cb25acc3baa4dfe3f2f5e00e32f1cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:54 GMT
ARG version=11.0.9.12-1
# Fri, 18 Dec 2020 09:27:11 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa4d5051eccba8a34b0c5943e7d3af1b699630442bcab5c4e6327140c73b25f`  
		Last Modified: Fri, 18 Dec 2020 09:29:06 GMT  
		Size: 146.5 MB (146467196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57edd843ac8e146169033b76a9449ae70b2d9e5af686c8efb213cb908c0277d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208173169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858d2f8c29c1b3513dfaca2be02bfa1161a7c310d3a9e2ec7a19c149f5b90b99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:06 GMT
ARG version=11.0.9.12-1
# Thu, 17 Dec 2020 23:07:34 GMT
# ARGS: version=11.0.9.12-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f87068084c62f6785078d6926dbd1770554b01e03da0bd3aadf6343dae011f`  
		Last Modified: Thu, 17 Dec 2020 23:09:37 GMT  
		Size: 144.5 MB (144497469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:76acd2ab267cb71abeab875af97d91fb483d81bc4e372d1dd28bad32d8ccd693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ad16f7b90421b975a18429d141c94895cd4fe1d4489bc610d53cf7e18ecf4527
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194996787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10971533e52923f349ed175ba9841881fb4d18cee46d345c854debb6093601e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:23 GMT
ARG version=11.0.9.12.1
# Thu, 17 Dec 2020 00:50:30 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 17 Dec 2020 00:50:30 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63066bc434b60a2bf6ab277b7713d0cdf8436126ed3ad4fc88a7c72d79e7070c`  
		Last Modified: Thu, 17 Dec 2020 00:52:24 GMT  
		Size: 192.2 MB (192197721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:76acd2ab267cb71abeab875af97d91fb483d81bc4e372d1dd28bad32d8ccd693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ad16f7b90421b975a18429d141c94895cd4fe1d4489bc610d53cf7e18ecf4527
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194996787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10971533e52923f349ed175ba9841881fb4d18cee46d345c854debb6093601e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:23 GMT
ARG version=11.0.9.12.1
# Thu, 17 Dec 2020 00:50:30 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 17 Dec 2020 00:50:30 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63066bc434b60a2bf6ab277b7713d0cdf8436126ed3ad4fc88a7c72d79e7070c`  
		Last Modified: Thu, 17 Dec 2020 00:52:24 GMT  
		Size: 192.2 MB (192197721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:76acd2ab267cb71abeab875af97d91fb483d81bc4e372d1dd28bad32d8ccd693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ad16f7b90421b975a18429d141c94895cd4fe1d4489bc610d53cf7e18ecf4527
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194996787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10971533e52923f349ed175ba9841881fb4d18cee46d345c854debb6093601e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:23 GMT
ARG version=11.0.9.12.1
# Thu, 17 Dec 2020 00:50:30 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 17 Dec 2020 00:50:30 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63066bc434b60a2bf6ab277b7713d0cdf8436126ed3ad4fc88a7c72d79e7070c`  
		Last Modified: Thu, 17 Dec 2020 00:52:24 GMT  
		Size: 192.2 MB (192197721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15`

```console
$ docker pull amazoncorretto@sha256:2ddc1907db80b125739883bd84a84b976f28b89bdc0724c0901096fb01ed5b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ec851bbaaff7e97cc0a84c07b8ca6c7d6ad223cdaea3c21534090cf7bf712b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8760ee01cbb0a508b643f32f2b2c64c391e03cbe40200cd4ee5a2e9365db0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:27:26 GMT
ARG version=15.0.1.9-1
# Fri, 18 Dec 2020 09:27:48 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a962697c7bb711e82ff306efdb1e23f54cb3a73308995bcee1ef0986d86a7`  
		Last Modified: Fri, 18 Dec 2020 09:29:36 GMT  
		Size: 155.7 MB (155663879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:028ea8f8304dcb94b0ba23bd9860452105445c73ffe5f6150d68600fb0606a4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219211194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0acb2c1b4c67bf5caf166a4f4938c2fe13b7d800de9c7b6a35d25b878cae89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:43 GMT
ARG version=15.0.1.9-1
# Thu, 17 Dec 2020 23:08:12 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:08:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabd893f46c6ff949915ab59c407c77ae779a5ca21dbb49b0f5fe0d40bf34cb`  
		Last Modified: Thu, 17 Dec 2020 23:10:20 GMT  
		Size: 155.5 MB (155535494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.1`

```console
$ docker pull amazoncorretto@sha256:2ddc1907db80b125739883bd84a84b976f28b89bdc0724c0901096fb01ed5b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15.0.1` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ec851bbaaff7e97cc0a84c07b8ca6c7d6ad223cdaea3c21534090cf7bf712b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8760ee01cbb0a508b643f32f2b2c64c391e03cbe40200cd4ee5a2e9365db0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:27:26 GMT
ARG version=15.0.1.9-1
# Fri, 18 Dec 2020 09:27:48 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a962697c7bb711e82ff306efdb1e23f54cb3a73308995bcee1ef0986d86a7`  
		Last Modified: Fri, 18 Dec 2020 09:29:36 GMT  
		Size: 155.7 MB (155663879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15.0.1` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:028ea8f8304dcb94b0ba23bd9860452105445c73ffe5f6150d68600fb0606a4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219211194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0acb2c1b4c67bf5caf166a4f4938c2fe13b7d800de9c7b6a35d25b878cae89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:43 GMT
ARG version=15.0.1.9-1
# Thu, 17 Dec 2020 23:08:12 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:08:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabd893f46c6ff949915ab59c407c77ae779a5ca21dbb49b0f5fe0d40bf34cb`  
		Last Modified: Thu, 17 Dec 2020 23:10:20 GMT  
		Size: 155.5 MB (155535494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.1-al2`

```console
$ docker pull amazoncorretto@sha256:2ddc1907db80b125739883bd84a84b976f28b89bdc0724c0901096fb01ed5b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15.0.1-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ec851bbaaff7e97cc0a84c07b8ca6c7d6ad223cdaea3c21534090cf7bf712b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8760ee01cbb0a508b643f32f2b2c64c391e03cbe40200cd4ee5a2e9365db0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:27:26 GMT
ARG version=15.0.1.9-1
# Fri, 18 Dec 2020 09:27:48 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a962697c7bb711e82ff306efdb1e23f54cb3a73308995bcee1ef0986d86a7`  
		Last Modified: Fri, 18 Dec 2020 09:29:36 GMT  
		Size: 155.7 MB (155663879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15.0.1-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:028ea8f8304dcb94b0ba23bd9860452105445c73ffe5f6150d68600fb0606a4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219211194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0acb2c1b4c67bf5caf166a4f4938c2fe13b7d800de9c7b6a35d25b878cae89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:43 GMT
ARG version=15.0.1.9-1
# Thu, 17 Dec 2020 23:08:12 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:08:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabd893f46c6ff949915ab59c407c77ae779a5ca21dbb49b0f5fe0d40bf34cb`  
		Last Modified: Thu, 17 Dec 2020 23:10:20 GMT  
		Size: 155.5 MB (155535494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15.0.1-alpine`

```console
$ docker pull amazoncorretto@sha256:20c82ab4e62bf9f91630d7841ed3c9dc943c17f5f5c94857764a2ffd54b2f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15.0.1-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c25de619e51e7c78a486bf70808b754a3abd610411f8e1f87c8fedabf59734c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207717112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e56b0bd70ace662b71fe9d3638c944ad640bfe394dc200355bc53aef77a452a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:39 GMT
ARG version=15.0.1.9.1
# Thu, 17 Dec 2020 00:50:47 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 17 Dec 2020 00:50:47 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d14c6e3b1c71aadf5ad20b205d0c58ed6721023a96da8bb8ccaf98a9edd08`  
		Last Modified: Thu, 17 Dec 2020 00:52:52 GMT  
		Size: 204.9 MB (204918046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-al2-full`

```console
$ docker pull amazoncorretto@sha256:2ddc1907db80b125739883bd84a84b976f28b89bdc0724c0901096fb01ed5b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ec851bbaaff7e97cc0a84c07b8ca6c7d6ad223cdaea3c21534090cf7bf712b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8760ee01cbb0a508b643f32f2b2c64c391e03cbe40200cd4ee5a2e9365db0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:27:26 GMT
ARG version=15.0.1.9-1
# Fri, 18 Dec 2020 09:27:48 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a962697c7bb711e82ff306efdb1e23f54cb3a73308995bcee1ef0986d86a7`  
		Last Modified: Fri, 18 Dec 2020 09:29:36 GMT  
		Size: 155.7 MB (155663879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:028ea8f8304dcb94b0ba23bd9860452105445c73ffe5f6150d68600fb0606a4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219211194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0acb2c1b4c67bf5caf166a4f4938c2fe13b7d800de9c7b6a35d25b878cae89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:43 GMT
ARG version=15.0.1.9-1
# Thu, 17 Dec 2020 23:08:12 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:08:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabd893f46c6ff949915ab59c407c77ae779a5ca21dbb49b0f5fe0d40bf34cb`  
		Last Modified: Thu, 17 Dec 2020 23:10:20 GMT  
		Size: 155.5 MB (155535494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:2ddc1907db80b125739883bd84a84b976f28b89bdc0724c0901096fb01ed5b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ec851bbaaff7e97cc0a84c07b8ca6c7d6ad223cdaea3c21534090cf7bf712b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217672398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8760ee01cbb0a508b643f32f2b2c64c391e03cbe40200cd4ee5a2e9365db0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:27:26 GMT
ARG version=15.0.1.9-1
# Fri, 18 Dec 2020 09:27:48 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:27:48 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:27:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807a962697c7bb711e82ff306efdb1e23f54cb3a73308995bcee1ef0986d86a7`  
		Last Modified: Fri, 18 Dec 2020 09:29:36 GMT  
		Size: 155.7 MB (155663879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:028ea8f8304dcb94b0ba23bd9860452105445c73ffe5f6150d68600fb0606a4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219211194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0acb2c1b4c67bf5caf166a4f4938c2fe13b7d800de9c7b6a35d25b878cae89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:07:43 GMT
ARG version=15.0.1.9-1
# Thu, 17 Dec 2020 23:08:12 GMT
# ARGS: version=15.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:08:14 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabd893f46c6ff949915ab59c407c77ae779a5ca21dbb49b0f5fe0d40bf34cb`  
		Last Modified: Thu, 17 Dec 2020 23:10:20 GMT  
		Size: 155.5 MB (155535494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine`

```console
$ docker pull amazoncorretto@sha256:20c82ab4e62bf9f91630d7841ed3c9dc943c17f5f5c94857764a2ffd54b2f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c25de619e51e7c78a486bf70808b754a3abd610411f8e1f87c8fedabf59734c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207717112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e56b0bd70ace662b71fe9d3638c944ad640bfe394dc200355bc53aef77a452a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:39 GMT
ARG version=15.0.1.9.1
# Thu, 17 Dec 2020 00:50:47 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 17 Dec 2020 00:50:47 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d14c6e3b1c71aadf5ad20b205d0c58ed6721023a96da8bb8ccaf98a9edd08`  
		Last Modified: Thu, 17 Dec 2020 00:52:52 GMT  
		Size: 204.9 MB (204918046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine-full`

```console
$ docker pull amazoncorretto@sha256:20c82ab4e62bf9f91630d7841ed3c9dc943c17f5f5c94857764a2ffd54b2f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c25de619e51e7c78a486bf70808b754a3abd610411f8e1f87c8fedabf59734c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207717112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e56b0bd70ace662b71fe9d3638c944ad640bfe394dc200355bc53aef77a452a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:39 GMT
ARG version=15.0.1.9.1
# Thu, 17 Dec 2020 00:50:47 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 17 Dec 2020 00:50:47 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d14c6e3b1c71aadf5ad20b205d0c58ed6721023a96da8bb8ccaf98a9edd08`  
		Last Modified: Thu, 17 Dec 2020 00:52:52 GMT  
		Size: 204.9 MB (204918046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:15-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:20c82ab4e62bf9f91630d7841ed3c9dc943c17f5f5c94857764a2ffd54b2f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c25de619e51e7c78a486bf70808b754a3abd610411f8e1f87c8fedabf59734c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207717112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e56b0bd70ace662b71fe9d3638c944ad640bfe394dc200355bc53aef77a452a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:39 GMT
ARG version=15.0.1.9.1
# Thu, 17 Dec 2020 00:50:47 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 17 Dec 2020 00:50:47 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d14c6e3b1c71aadf5ad20b205d0c58ed6721023a96da8bb8ccaf98a9edd08`  
		Last Modified: Thu, 17 Dec 2020 00:52:52 GMT  
		Size: 204.9 MB (204918046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:c0cee418710672eb0bf832f77505491958db377d08f946d8b9a5dac594474c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93920a42ddb25dbf5a91fbd128891eb383f22a09813bbe30cfd0b912ca139806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101779760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408df7b07ec1b2ac7817ba9a4ea4e9076db21bd598337d83c6578595a18b871f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:10 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 17 Dec 2020 00:50:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b381c2ee7bec3c1c893e503740a32e185ae03be120aefea696cccb7c05eef9e`  
		Last Modified: Thu, 17 Dec 2020 00:51:37 GMT  
		Size: 99.0 MB (98980694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:c0cee418710672eb0bf832f77505491958db377d08f946d8b9a5dac594474c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93920a42ddb25dbf5a91fbd128891eb383f22a09813bbe30cfd0b912ca139806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101779760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408df7b07ec1b2ac7817ba9a4ea4e9076db21bd598337d83c6578595a18b871f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:10 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 17 Dec 2020 00:50:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b381c2ee7bec3c1c893e503740a32e185ae03be120aefea696cccb7c05eef9e`  
		Last Modified: Thu, 17 Dec 2020 00:51:37 GMT  
		Size: 99.0 MB (98980694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:c0cee418710672eb0bf832f77505491958db377d08f946d8b9a5dac594474c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93920a42ddb25dbf5a91fbd128891eb383f22a09813bbe30cfd0b912ca139806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101779760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408df7b07ec1b2ac7817ba9a4ea4e9076db21bd598337d83c6578595a18b871f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:10 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 17 Dec 2020 00:50:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b381c2ee7bec3c1c893e503740a32e185ae03be120aefea696cccb7c05eef9e`  
		Last Modified: Thu, 17 Dec 2020 00:51:37 GMT  
		Size: 99.0 MB (98980694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:aedc0ecf66062469f241f82390ea25f9494c887aa157ac82de4781720b8844f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b94869b52e01c0c40f03e8d3a3cf2e49f41ddf135d49ed73b789a7dbf10c2492
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43110423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9156cb8de3e445ab055fb847efe67434f3ce8e41f815a60837d8306ab2a853`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:18 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 17 Dec 2020 00:50:18 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f035a010dfd1600f99094ad26b4dca951c136885ee00aa2c6ea111ee1794f370`  
		Last Modified: Thu, 17 Dec 2020 00:52:02 GMT  
		Size: 40.3 MB (40311357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u275` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u275` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275-al2`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u275-al2` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u275-al2` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275-alpine`

```console
$ docker pull amazoncorretto@sha256:c0cee418710672eb0bf832f77505491958db377d08f946d8b9a5dac594474c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u275-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93920a42ddb25dbf5a91fbd128891eb383f22a09813bbe30cfd0b912ca139806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101779760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408df7b07ec1b2ac7817ba9a4ea4e9076db21bd598337d83c6578595a18b871f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:10 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 17 Dec 2020 00:50:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Dec 2020 00:50:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b381c2ee7bec3c1c893e503740a32e185ae03be120aefea696cccb7c05eef9e`  
		Last Modified: Thu, 17 Dec 2020 00:51:37 GMT  
		Size: 99.0 MB (98980694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:8u275-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:aedc0ecf66062469f241f82390ea25f9494c887aa157ac82de4781720b8844f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u275-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b94869b52e01c0c40f03e8d3a3cf2e49f41ddf135d49ed73b789a7dbf10c2492
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43110423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9156cb8de3e445ab055fb847efe67434f3ce8e41f815a60837d8306ab2a853`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:50:05 GMT
ARG version=8.275.01.2
# Thu, 17 Dec 2020 00:50:18 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 17 Dec 2020 00:50:18 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 00:50:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f035a010dfd1600f99094ad26b4dca951c136885ee00aa2c6ea111ee1794f370`  
		Last Modified: Thu, 17 Dec 2020 00:52:02 GMT  
		Size: 40.3 MB (40311357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:ff0a943f49b9b81843dcc6bdba5bf20313825c9fa7a5e5f6f8faf1277c3c6e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:713264664eed4bd2b0d6674ed83bb6c3595517d83774913fc990fa18a82af36b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137287671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19e85a8144caf493426046e063138d7dc246d0a877b32c17d8ea5929f13ba5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Dec 2020 07:04:34 GMT
ADD file:63bb1089f29109498e6000d9884216288b7b1b9093e0c247b99df2a8ba64d601 in / 
# Fri, 18 Dec 2020 07:04:35 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 09:26:32 GMT
ARG version=1.8.0_275.b01-1
# Fri, 18 Dec 2020 09:26:47 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 18 Dec 2020 09:26:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 09:26:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:b6f03d5d6f5a93eede753139822eca5ce4a921a8c35922b9969996cfc31deb60`  
		Last Modified: Wed, 09 Dec 2020 16:33:37 GMT  
		Size: 62.0 MB (62008519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6f58facb3659bb3697cd51471f37ec5e30d4b0ddd0a28de875b8b667b5f8c9`  
		Last Modified: Fri, 18 Dec 2020 09:28:44 GMT  
		Size: 75.3 MB (75279152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6618ae7649a52f6869bcbc1488e9b1eb00b4f474440b32397db457ecd78c6e23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123027945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1f7aec02c7ec5a99c2d809d5a1178dc5c9ec83636c614acb2e012d9b89e8ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Dec 2020 22:48:34 GMT
ADD file:fef50d3f23c05efa2cb62375be9cc62cd47bb605bd119f813fa1c7f529d9d27c in / 
# Thu, 17 Dec 2020 22:48:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 23:06:25 GMT
ARG version=1.8.0_275.b01-1
# Thu, 17 Dec 2020 23:06:58 GMT
# ARGS: version=1.8.0_275.b01-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Dec 2020 23:06:59 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 23:07:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ee4590ce5e19453a11908348603e8da0375a376105f9b2e130afce2344f42677`  
		Last Modified: Wed, 09 Dec 2020 22:47:33 GMT  
		Size: 63.7 MB (63675700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda0d28738ebf400b9e9d08508b79c6c8f7bcf27a4a9c5639355711317bb9da2`  
		Last Modified: Thu, 17 Dec 2020 23:08:57 GMT  
		Size: 59.4 MB (59352245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
