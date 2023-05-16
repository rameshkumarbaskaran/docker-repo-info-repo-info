## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:2740f34f475ff2fd1961eb7b2b58ae91961ef74a6f2d18ff32de78afe60def75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:dd86543f59520f317599a56451050f712c0a117c420e4e6e30cbcc1fb8db8b84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31779170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940ae3002ffa7baadfa10c87d888bb9be5fe56c1d95565f40821ed9ff2b94bea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:02:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:02:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 May 2023 01:02:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 May 2023 01:02:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:02:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2372d6e43648bec4df62a3d55e7f95e72243565b07c6d5920d3406d6eefbd5a8`  
		Last Modified: Tue, 16 May 2023 01:03:22 GMT  
		Size: 4.8 MB (4821195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620a82a5993926d5580487c99ad1a0938a9b68875b3c29746a0f4374f50e4ed6`  
		Last Modified: Tue, 16 May 2023 01:03:21 GMT  
		Size: 1.7 KB (1664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fb021293ae8fb1060eeeb057accbc60b7390f8cf2b9edfa122e80294f3de7c`  
		Last Modified: Tue, 16 May 2023 01:03:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638c786576ffd5a24ecad657d482b765f09fa254580fc4d6a4ab147d457f6a89`  
		Last Modified: Tue, 16 May 2023 01:03:21 GMT  
		Size: 240.3 KB (240297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd3984fa38330d1b3b2590d00da5c0e2052ec84b96bd48683df7d0fd5bc299b`  
		Last Modified: Tue, 16 May 2023 01:03:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bionic-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:51567a48e4ee4ab6244cac21df91a34de9ac8631e64cb62003c3692aaa09b61d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c879b3d4ab74022bc603e9e94dff0eec069290bf4d4a3de32a44954b0d82dd38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:31:18 GMT
ARG RELEASE
# Fri, 12 May 2023 09:31:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:31:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:31:18 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:31:23 GMT
ADD file:65c814904a00832cc69b4ef05c54d1cd3b570be2c12d8891a1472a73d6534cda in / 
# Fri, 12 May 2023 09:31:24 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:25:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:25:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 16 May 2023 01:25:39 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 16 May 2023 01:25:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:25:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs
```

-	Layers:
	-	`sha256:d3196e9fda85b1ae1aa48fdd42a05894cf36dbbe8d2b8b75f46691b12cba022d`  
		Last Modified: Tue, 16 May 2023 01:26:21 GMT  
		Size: 23.7 MB (23740923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592501afdaec24bcc465ef26abc1b7d532782a85c6cbe7893a7fd774b7ddb8c1`  
		Last Modified: Tue, 16 May 2023 01:26:19 GMT  
		Size: 4.4 MB (4403694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0312aba612c00a457099681cef3a29c3e73ce54ce0e4aac34fdd08b0adfeb`  
		Last Modified: Tue, 16 May 2023 01:26:18 GMT  
		Size: 1.7 KB (1665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fdfd9ebabe147a93ab87064e56e524fc5ae9821794b68014d92124bd1ce284`  
		Last Modified: Tue, 16 May 2023 01:26:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d273709265897dc91aaf15ee076766e0c6660e13254c4aade22b856ed3e5bca`  
		Last Modified: Tue, 16 May 2023 01:26:18 GMT  
		Size: 241.1 KB (241071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2a8256b93deb2dd3244eaf3d152d923018cd4332060d4a4ec7842e728aae9b`  
		Last Modified: Tue, 16 May 2023 01:26:29 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
