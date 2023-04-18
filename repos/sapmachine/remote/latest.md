## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:b466fc9871bb7027dec3bd783de62cba00c3073d09fdae54921de7a57480fe14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:5305baf0b92f8e614e32c9f4fb89579f90589faedc7bef7943884bbbecfbfb26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244212786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d0f3cda91a5c3047e4a04027f88947b8ca4d60da44a42b1972e14c693361b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:18:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:14 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 01:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaa7fcf1d088a5e28885bcd22e9b185e81e5f63d784be8e835865efa147ef11`  
		Last Modified: Tue, 18 Apr 2023 01:21:26 GMT  
		Size: 7.9 MB (7917699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491290f1581ae2267641201c694aa8e06bb983e6bdd6e8b5c1ba020394c15091`  
		Last Modified: Tue, 18 Apr 2023 01:22:48 GMT  
		Size: 207.7 MB (207716524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:27a4b6ef72b96a8caf5abbf2d0eacc7d484feac490e9bb17c2d9eab864d6b419
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240999552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54ae5c5eef571b7ac4ef76f0e8e85b7e12f22edc265d4f1a805ed6357d4994b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 02:25:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 02:27:22 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 02:27:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 02:27:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e067d4172369eec8f6d3194c1339fa98c65b02bd1ae08f1fb5947a3792b1cb`  
		Last Modified: Tue, 18 Apr 2023 02:27:39 GMT  
		Size: 7.8 MB (7756992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3c535b5c592ce2c032792cd11ed7d6c689f9bdb936d09df5582cf3c0ae7375`  
		Last Modified: Tue, 18 Apr 2023 02:28:49 GMT  
		Size: 206.0 MB (206046164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3ca051ce1a1932d780eabc7bace9ea43bd6ef2ca7de9060d892da3eba14efa3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251189847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4457e5898c3a9f81b9f9eb3c6d85a9bbeda6f54e98067a3e6a8fa3c302b9618d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:21:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 18 Apr 2023 01:22:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7b240a15bddb0a3f238ea0f9dd5dcffb15162dfa03f4e233171b45b41c03e9`  
		Last Modified: Tue, 18 Apr 2023 01:22:20 GMT  
		Size: 9.3 MB (9316592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c519a469c815fedc87e0131e8dce65b06ba4bfec7ba2edf79e9c420bf869ba7`  
		Last Modified: Tue, 18 Apr 2023 01:24:28 GMT  
		Size: 208.6 MB (208572275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
