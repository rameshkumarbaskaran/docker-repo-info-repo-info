<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.18`](#sapmachine11018)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.6`](#sapmachine1706)
-	[`sapmachine:19`](#sapmachine19)
-	[`sapmachine:19.0.2`](#sapmachine1902)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:4ac378aff27c8ad0167370ac466797f3d27cfb82d88ea31273076b6dab7d0e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:72c362b08333fca0798a1ed8087215d954151b46ac0f7acc2a6e5a8617240e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235421864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa92130ac0cf8eee1d26eae9790a60b3778d3e1babcddea51ca1c0de1d05f64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 01 Feb 2023 19:37:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c728cc98f722939b5f6eece7de8a58fa59bc037bc7d5cf79db19932d28de5a`  
		Last Modified: Wed, 01 Feb 2023 19:38:54 GMT  
		Size: 198.9 MB (198930596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:693b06ce21085b10f158f0e28372f02656fa7344e5cfcbbe7f39e6b90d036a4b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231815685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b7555f7c41cad682dd12099684a6e580268d62b8a1a3deec7d40d900c22971`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:37 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 01 Feb 2023 19:11:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee3eb84787a1f747e8d3f6f17c44fe5f526f479192b26669f0257a08c7ff67`  
		Last Modified: Wed, 01 Feb 2023 19:13:13 GMT  
		Size: 196.9 MB (196866478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3b76188e9b984558494e1244e1849a9030822a8b07e539458879ff966c8b3ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227462768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee288d19f4cd3c28c101086d608404a323ed901bdff77132b38a3c08f6101431`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:09:20 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:09:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 01 Feb 2023 19:09:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cba2156fb4dc20c4d25aeab39226b25f08353fb5c85241053e2e46298417269`  
		Last Modified: Wed, 01 Feb 2023 19:13:55 GMT  
		Size: 184.8 MB (184848820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.18`

```console
$ docker pull sapmachine@sha256:4ac378aff27c8ad0167370ac466797f3d27cfb82d88ea31273076b6dab7d0e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11.0.18` - linux; amd64

```console
$ docker pull sapmachine@sha256:72c362b08333fca0798a1ed8087215d954151b46ac0f7acc2a6e5a8617240e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235421864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa92130ac0cf8eee1d26eae9790a60b3778d3e1babcddea51ca1c0de1d05f64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 01 Feb 2023 19:37:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c728cc98f722939b5f6eece7de8a58fa59bc037bc7d5cf79db19932d28de5a`  
		Last Modified: Wed, 01 Feb 2023 19:38:54 GMT  
		Size: 198.9 MB (198930596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11.0.18` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:693b06ce21085b10f158f0e28372f02656fa7344e5cfcbbe7f39e6b90d036a4b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231815685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b7555f7c41cad682dd12099684a6e580268d62b8a1a3deec7d40d900c22971`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:37 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 01 Feb 2023 19:11:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ee3eb84787a1f747e8d3f6f17c44fe5f526f479192b26669f0257a08c7ff67`  
		Last Modified: Wed, 01 Feb 2023 19:13:13 GMT  
		Size: 196.9 MB (196866478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11.0.18` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3b76188e9b984558494e1244e1849a9030822a8b07e539458879ff966c8b3ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227462768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee288d19f4cd3c28c101086d608404a323ed901bdff77132b38a3c08f6101431`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:09:20 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:09:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 01 Feb 2023 19:09:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cba2156fb4dc20c4d25aeab39226b25f08353fb5c85241053e2e46298417269`  
		Last Modified: Wed, 01 Feb 2023 19:13:55 GMT  
		Size: 184.8 MB (184848820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:59256782ddeee1d03cd850169ece419692cfd5e1f697febd9f692bfa072f26d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:491692ebf316872b255177fc930ba3084de3113ad87e62af61e374970e85c3d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234571983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa31241389be195db14fed7c1338986a4e7a34ad8fddcdf94d9b51f70b65618`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:37:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d55b004b5a63431a7feffb61b7520f20068c280979145331f1749cd9a53a402`  
		Last Modified: Wed, 01 Feb 2023 19:39:17 GMT  
		Size: 198.1 MB (198080715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c38fd0d89cdb54e217837bd36e610641f25d6f1f17a938ffe9887608b3cc4cec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231057468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afb3adb9de96ddb807fda47517542f5fdedb2c2ae34d30894b783c8a8bb60eb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:12:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afab7854d2a348f242d4dd8183106fd8f0b2db6b5cc40c19f8c49a84184fa481`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 196.1 MB (196108261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2b514c04219e3cc923c7c4ac0354e5c0ed43560980aa6dcb04a0ba3227cf0d1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240837838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbf946bc3acd12b9ff58ae35d3bd4bd3841af44312492fa4ec95981a90eb90c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:10:57 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:11:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2fea3b8447c3560525677504b1451371cf2f58ab7ea8c2b67e10d314511589`  
		Last Modified: Wed, 01 Feb 2023 19:14:33 GMT  
		Size: 198.2 MB (198223890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.6`

```console
$ docker pull sapmachine@sha256:59256782ddeee1d03cd850169ece419692cfd5e1f697febd9f692bfa072f26d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17.0.6` - linux; amd64

```console
$ docker pull sapmachine@sha256:491692ebf316872b255177fc930ba3084de3113ad87e62af61e374970e85c3d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234571983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa31241389be195db14fed7c1338986a4e7a34ad8fddcdf94d9b51f70b65618`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:37:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d55b004b5a63431a7feffb61b7520f20068c280979145331f1749cd9a53a402`  
		Last Modified: Wed, 01 Feb 2023 19:39:17 GMT  
		Size: 198.1 MB (198080715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17.0.6` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c38fd0d89cdb54e217837bd36e610641f25d6f1f17a938ffe9887608b3cc4cec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231057468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afb3adb9de96ddb807fda47517542f5fdedb2c2ae34d30894b783c8a8bb60eb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:12:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afab7854d2a348f242d4dd8183106fd8f0b2db6b5cc40c19f8c49a84184fa481`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 196.1 MB (196108261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17.0.6` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2b514c04219e3cc923c7c4ac0354e5c0ed43560980aa6dcb04a0ba3227cf0d1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240837838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbf946bc3acd12b9ff58ae35d3bd4bd3841af44312492fa4ec95981a90eb90c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:10:57 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:11:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2fea3b8447c3560525677504b1451371cf2f58ab7ea8c2b67e10d314511589`  
		Last Modified: Wed, 01 Feb 2023 19:14:33 GMT  
		Size: 198.2 MB (198223890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19`

```console
$ docker pull sapmachine@sha256:1aadc5c4866bafd9262234ec2eca1d786b544fb586809f2feda851211bcd1220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:19` - linux; amd64

```console
$ docker pull sapmachine@sha256:6d36e6a5bf713a919048d924562c470b8e50be4dafe3a9b6cde8c1a74eb5f655
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242929149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ddfe28188a3abe8540194091dfa7749e2887935053aa1991cd4d34188ae365`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:38:25 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:38:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:38:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe1b91d5dd2fa1b13bd345338b6329d4f4d48a4e2493f049fdaa0f32cfd8b18`  
		Last Modified: Wed, 01 Feb 2023 19:39:42 GMT  
		Size: 206.4 MB (206437881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1cb07868b88cafbeb8e69d8ab9237b6210c2b840d8f860c13154560ac388533d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239516926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ae0497166def55f49285321bc3df731d8fce1845db180da33a3d889342803`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:41 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:12:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9ac49e72ffe30b4937feb49b694d4afbcbfe325fffceb3749a4cbb3a6b3cf`  
		Last Modified: Wed, 01 Feb 2023 19:13:57 GMT  
		Size: 204.6 MB (204567719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:aeb5c010fb1cb50da6596fd8b0ca74b28c3b2b629ff3ff571e3a87a50042b12d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249078848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69873218baef21d5d79d926a65af4b0263f8b59d32173ce1aa2a1e05e1a8e175`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb8fe38a2617687f1926d60eef95e4f0e67c679d02452c27b545aca152c2aa2`  
		Last Modified: Wed, 01 Feb 2023 19:15:13 GMT  
		Size: 206.5 MB (206464900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:19.0.2`

```console
$ docker pull sapmachine@sha256:1aadc5c4866bafd9262234ec2eca1d786b544fb586809f2feda851211bcd1220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:19.0.2` - linux; amd64

```console
$ docker pull sapmachine@sha256:6d36e6a5bf713a919048d924562c470b8e50be4dafe3a9b6cde8c1a74eb5f655
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242929149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ddfe28188a3abe8540194091dfa7749e2887935053aa1991cd4d34188ae365`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:38:25 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:38:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:38:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe1b91d5dd2fa1b13bd345338b6329d4f4d48a4e2493f049fdaa0f32cfd8b18`  
		Last Modified: Wed, 01 Feb 2023 19:39:42 GMT  
		Size: 206.4 MB (206437881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19.0.2` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1cb07868b88cafbeb8e69d8ab9237b6210c2b840d8f860c13154560ac388533d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239516926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ae0497166def55f49285321bc3df731d8fce1845db180da33a3d889342803`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:41 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:12:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9ac49e72ffe30b4937feb49b694d4afbcbfe325fffceb3749a4cbb3a6b3cf`  
		Last Modified: Wed, 01 Feb 2023 19:13:57 GMT  
		Size: 204.6 MB (204567719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:19.0.2` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:aeb5c010fb1cb50da6596fd8b0ca74b28c3b2b629ff3ff571e3a87a50042b12d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249078848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69873218baef21d5d79d926a65af4b0263f8b59d32173ce1aa2a1e05e1a8e175`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb8fe38a2617687f1926d60eef95e4f0e67c679d02452c27b545aca152c2aa2`  
		Last Modified: Wed, 01 Feb 2023 19:15:13 GMT  
		Size: 206.5 MB (206464900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:1aadc5c4866bafd9262234ec2eca1d786b544fb586809f2feda851211bcd1220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:6d36e6a5bf713a919048d924562c470b8e50be4dafe3a9b6cde8c1a74eb5f655
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242929149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ddfe28188a3abe8540194091dfa7749e2887935053aa1991cd4d34188ae365`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:38:25 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:38:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:38:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe1b91d5dd2fa1b13bd345338b6329d4f4d48a4e2493f049fdaa0f32cfd8b18`  
		Last Modified: Wed, 01 Feb 2023 19:39:42 GMT  
		Size: 206.4 MB (206437881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1cb07868b88cafbeb8e69d8ab9237b6210c2b840d8f860c13154560ac388533d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239516926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ae0497166def55f49285321bc3df731d8fce1845db180da33a3d889342803`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:41 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:12:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9ac49e72ffe30b4937feb49b694d4afbcbfe325fffceb3749a4cbb3a6b3cf`  
		Last Modified: Wed, 01 Feb 2023 19:13:57 GMT  
		Size: 204.6 MB (204567719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:aeb5c010fb1cb50da6596fd8b0ca74b28c3b2b629ff3ff571e3a87a50042b12d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249078848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69873218baef21d5d79d926a65af4b0263f8b59d32173ce1aa2a1e05e1a8e175`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 01 Feb 2023 19:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb8fe38a2617687f1926d60eef95e4f0e67c679d02452c27b545aca152c2aa2`  
		Last Modified: Wed, 01 Feb 2023 19:15:13 GMT  
		Size: 206.5 MB (206464900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:59256782ddeee1d03cd850169ece419692cfd5e1f697febd9f692bfa072f26d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:491692ebf316872b255177fc930ba3084de3113ad87e62af61e374970e85c3d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234571983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa31241389be195db14fed7c1338986a4e7a34ad8fddcdf94d9b51f70b65618`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:37:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d55b004b5a63431a7feffb61b7520f20068c280979145331f1749cd9a53a402`  
		Last Modified: Wed, 01 Feb 2023 19:39:17 GMT  
		Size: 198.1 MB (198080715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c38fd0d89cdb54e217837bd36e610641f25d6f1f17a938ffe9887608b3cc4cec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231057468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afb3adb9de96ddb807fda47517542f5fdedb2c2ae34d30894b783c8a8bb60eb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:12:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afab7854d2a348f242d4dd8183106fd8f0b2db6b5cc40c19f8c49a84184fa481`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 196.1 MB (196108261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2b514c04219e3cc923c7c4ac0354e5c0ed43560980aa6dcb04a0ba3227cf0d1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240837838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbf946bc3acd12b9ff58ae35d3bd4bd3841af44312492fa4ec95981a90eb90c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:10:57 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:11:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2fea3b8447c3560525677504b1451371cf2f58ab7ea8c2b67e10d314511589`  
		Last Modified: Wed, 01 Feb 2023 19:14:33 GMT  
		Size: 198.2 MB (198223890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
