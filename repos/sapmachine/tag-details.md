<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.16.1`](#sapmachine110161)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.4.1`](#sapmachine17041)
-	[`sapmachine:18`](#sapmachine18)
-	[`sapmachine:18.0.2.1`](#sapmachine18021)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:3017aedf60c62b9d422b4ad6080812502b4f8b4fca600b68064366b8aab37356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d0c1b8d5fa072f60dcbdf236d5ddde104f830a502ec8c2e0f000177eba50fb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234784231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d3f73f73a527298f1e2bba75944dd08efce603848b303fd89678ca742ac488`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:11 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 25 Aug 2022 18:25:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d646b317d36d8a2bbfa1f401078a335256d2f7527a0fd651fc5d1a2a3ef9f45`  
		Last Modified: Thu, 25 Aug 2022 18:26:57 GMT  
		Size: 198.3 MB (198291393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.16.1`

```console
$ docker pull sapmachine@sha256:3017aedf60c62b9d422b4ad6080812502b4f8b4fca600b68064366b8aab37356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.16.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d0c1b8d5fa072f60dcbdf236d5ddde104f830a502ec8c2e0f000177eba50fb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234784231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d3f73f73a527298f1e2bba75944dd08efce603848b303fd89678ca742ac488`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:11 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 25 Aug 2022 18:25:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d646b317d36d8a2bbfa1f401078a335256d2f7527a0fd651fc5d1a2a3ef9f45`  
		Last Modified: Thu, 25 Aug 2022 18:26:57 GMT  
		Size: 198.3 MB (198291393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:b40d9f329299e123b98b47fd2a98054bf87dfa5ca63a082cdde5557068d89cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:7625cd7411d8b5e9907e72c425229aad60773c19ab80ba6e1adce2d0b4e8b413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee26e49d3653c043ee171c18ab31b896cfa4474d0326ebec5897137a80d9b82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:47 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 25 Aug 2022 18:25:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a3d0b942880710e44d79a9fc7ee9cf36c54928a08099251a191c64d2c89bd3`  
		Last Modified: Thu, 25 Aug 2022 18:27:22 GMT  
		Size: 197.8 MB (197764607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.4.1`

```console
$ docker pull sapmachine@sha256:b40d9f329299e123b98b47fd2a98054bf87dfa5ca63a082cdde5557068d89cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.4.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:7625cd7411d8b5e9907e72c425229aad60773c19ab80ba6e1adce2d0b4e8b413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee26e49d3653c043ee171c18ab31b896cfa4474d0326ebec5897137a80d9b82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:47 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 25 Aug 2022 18:25:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a3d0b942880710e44d79a9fc7ee9cf36c54928a08099251a191c64d2c89bd3`  
		Last Modified: Thu, 25 Aug 2022 18:27:22 GMT  
		Size: 197.8 MB (197764607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18`

```console
$ docker pull sapmachine@sha256:c14fe7a8745bc993ccfa2eaa262f6f6f4c9b725b3b9f52a907163f7ebb59858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18` - linux; amd64

```console
$ docker pull sapmachine@sha256:29d32a469b9fbc7ee8aa4c09c27f53eda981dd9054dd62a2db0460f194656e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235300653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0892cb60a19c1fff453cfaac071e8cbf6c6266f2501e1d5eca024eb4b86e9f5a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:26:25 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:26:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Thu, 25 Aug 2022 18:26:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a48d0bb025263416e1fabfc1b6224bd16fdf37c52d81fb21055d125108afae`  
		Last Modified: Thu, 25 Aug 2022 18:27:49 GMT  
		Size: 198.8 MB (198807815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18.0.2.1`

```console
$ docker pull sapmachine@sha256:c14fe7a8745bc993ccfa2eaa262f6f6f4c9b725b3b9f52a907163f7ebb59858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18.0.2.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:29d32a469b9fbc7ee8aa4c09c27f53eda981dd9054dd62a2db0460f194656e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235300653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0892cb60a19c1fff453cfaac071e8cbf6c6266f2501e1d5eca024eb4b86e9f5a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:26:25 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:26:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Thu, 25 Aug 2022 18:26:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a48d0bb025263416e1fabfc1b6224bd16fdf37c52d81fb21055d125108afae`  
		Last Modified: Thu, 25 Aug 2022 18:27:49 GMT  
		Size: 198.8 MB (198807815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:c14fe7a8745bc993ccfa2eaa262f6f6f4c9b725b3b9f52a907163f7ebb59858b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:29d32a469b9fbc7ee8aa4c09c27f53eda981dd9054dd62a2db0460f194656e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235300653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0892cb60a19c1fff453cfaac071e8cbf6c6266f2501e1d5eca024eb4b86e9f5a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:26:25 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:26:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Thu, 25 Aug 2022 18:26:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a48d0bb025263416e1fabfc1b6224bd16fdf37c52d81fb21055d125108afae`  
		Last Modified: Thu, 25 Aug 2022 18:27:49 GMT  
		Size: 198.8 MB (198807815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:b40d9f329299e123b98b47fd2a98054bf87dfa5ca63a082cdde5557068d89cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:7625cd7411d8b5e9907e72c425229aad60773c19ab80ba6e1adce2d0b4e8b413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee26e49d3653c043ee171c18ab31b896cfa4474d0326ebec5897137a80d9b82`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:47 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Aug 2022 18:25:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 25 Aug 2022 18:25:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a3d0b942880710e44d79a9fc7ee9cf36c54928a08099251a191c64d2c89bd3`  
		Last Modified: Thu, 25 Aug 2022 18:27:22 GMT  
		Size: 197.8 MB (197764607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
