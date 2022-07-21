<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.16`](#sapmachine11016)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.4`](#sapmachine1704)
-	[`sapmachine:18`](#sapmachine18)
-	[`sapmachine:18.0.2`](#sapmachine1802)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:bdd9f40b1bbd08f7adeca93cdbb9f1489219253a2d7166e867b52579768b7817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:6e97ce65eb01ad9d0b9292c2e37a21efdcf294678e9a0ee4976c2033474b7545
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234333432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707054307ab72fbb8f50cac94659f5a59cb3057d197ebe989676a644a3a489fd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:21 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 21 Jul 2022 17:21:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48956d0b31c3429b214d01fc023826de94f77b918fbe83d5a835305a466cfc1`  
		Last Modified: Thu, 21 Jul 2022 17:23:00 GMT  
		Size: 197.8 MB (197834440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.16`

```console
$ docker pull sapmachine@sha256:bdd9f40b1bbd08f7adeca93cdbb9f1489219253a2d7166e867b52579768b7817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.16` - linux; amd64

```console
$ docker pull sapmachine@sha256:6e97ce65eb01ad9d0b9292c2e37a21efdcf294678e9a0ee4976c2033474b7545
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234333432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707054307ab72fbb8f50cac94659f5a59cb3057d197ebe989676a644a3a489fd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:21 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 21 Jul 2022 17:21:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48956d0b31c3429b214d01fc023826de94f77b918fbe83d5a835305a466cfc1`  
		Last Modified: Thu, 21 Jul 2022 17:23:00 GMT  
		Size: 197.8 MB (197834440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:4e9c1b9f921c88fd86b7e694efa1e22e97d914f82ab201a73c8b48250642ec48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:717b0c8a8a72b746d0c46de52e5e88ab30eb0e2c4a34abc732eeeaf38aec4e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233714838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e69ae943614681e281c4eac393c2f1558069004fc5bd7edb55613f65e5a5d1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 21 Jul 2022 17:21:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a60d8080bcd61c781a196c0c1b98a2d76fa5e4697147b21ed11b88f9457a8d`  
		Last Modified: Thu, 21 Jul 2022 17:23:26 GMT  
		Size: 197.2 MB (197215846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.4`

```console
$ docker pull sapmachine@sha256:4e9c1b9f921c88fd86b7e694efa1e22e97d914f82ab201a73c8b48250642ec48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.4` - linux; amd64

```console
$ docker pull sapmachine@sha256:717b0c8a8a72b746d0c46de52e5e88ab30eb0e2c4a34abc732eeeaf38aec4e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233714838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e69ae943614681e281c4eac393c2f1558069004fc5bd7edb55613f65e5a5d1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 21 Jul 2022 17:21:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a60d8080bcd61c781a196c0c1b98a2d76fa5e4697147b21ed11b88f9457a8d`  
		Last Modified: Thu, 21 Jul 2022 17:23:26 GMT  
		Size: 197.2 MB (197215846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18`

```console
$ docker pull sapmachine@sha256:a2433b41995a55b68a9bbb3188e64b279b5ef05e31cb3be347c3b1c897f5f9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18` - linux; amd64

```console
$ docker pull sapmachine@sha256:b5f9e4b5c71ec6cd6d288338c2eaf6498e382f8318c60fbe96e691a4128dde9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234762390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1fee7bf97e96ff33c3c0ddd576e83d40c6424c77f8fd1ef5aa0456b4506bd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:22:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:22:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Thu, 21 Jul 2022 17:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3386d3d75e11670a7761283f77616accdc44bee7fbb29c643b39fb23245005`  
		Last Modified: Thu, 21 Jul 2022 17:23:52 GMT  
		Size: 198.3 MB (198263398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18.0.2`

```console
$ docker pull sapmachine@sha256:a2433b41995a55b68a9bbb3188e64b279b5ef05e31cb3be347c3b1c897f5f9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18.0.2` - linux; amd64

```console
$ docker pull sapmachine@sha256:b5f9e4b5c71ec6cd6d288338c2eaf6498e382f8318c60fbe96e691a4128dde9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234762390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1fee7bf97e96ff33c3c0ddd576e83d40c6424c77f8fd1ef5aa0456b4506bd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:22:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:22:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Thu, 21 Jul 2022 17:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3386d3d75e11670a7761283f77616accdc44bee7fbb29c643b39fb23245005`  
		Last Modified: Thu, 21 Jul 2022 17:23:52 GMT  
		Size: 198.3 MB (198263398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:a2433b41995a55b68a9bbb3188e64b279b5ef05e31cb3be347c3b1c897f5f9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:b5f9e4b5c71ec6cd6d288338c2eaf6498e382f8318c60fbe96e691a4128dde9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234762390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1fee7bf97e96ff33c3c0ddd576e83d40c6424c77f8fd1ef5aa0456b4506bd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:22:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:22:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Thu, 21 Jul 2022 17:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3386d3d75e11670a7761283f77616accdc44bee7fbb29c643b39fb23245005`  
		Last Modified: Thu, 21 Jul 2022 17:23:52 GMT  
		Size: 198.3 MB (198263398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:4e9c1b9f921c88fd86b7e694efa1e22e97d914f82ab201a73c8b48250642ec48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:717b0c8a8a72b746d0c46de52e5e88ab30eb0e2c4a34abc732eeeaf38aec4e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233714838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e69ae943614681e281c4eac393c2f1558069004fc5bd7edb55613f65e5a5d1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:58:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jul 2022 17:21:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 21 Jul 2022 17:21:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe776cde7ad2a2b7a4d2c92bae129822b7fe24c87f0491eb7c7e449bf80c59a`  
		Last Modified: Tue, 07 Jun 2022 02:01:02 GMT  
		Size: 7.9 MB (7926360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a60d8080bcd61c781a196c0c1b98a2d76fa5e4697147b21ed11b88f9457a8d`  
		Last Modified: Thu, 21 Jul 2022 17:23:26 GMT  
		Size: 197.2 MB (197215846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
