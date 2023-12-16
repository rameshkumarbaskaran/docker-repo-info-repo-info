## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:e4385a5867437cb9161c35e52eae5c330a2ebaa86af22b0f1033a25838c66409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:dd98e2fd3586d8d97d8286777753e7eb7aab1c2524b7ecb4fff5624f17d308c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243874424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43849d43c32bf74d7cdd4ab8bf9eb7c49b60aaa27e0a74f4ad24af25292df8d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:09:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Sat, 16 Dec 2023 12:09:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Sat, 16 Dec 2023 12:09:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c951fda003d75af60c2f29ffa076873f7c586ee11c1988fd64932795e4a0040f`  
		Last Modified: Sat, 16 Dec 2023 12:16:51 GMT  
		Size: 213.4 MB (213427847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dee1e093102e9b7aff9f5a66b229718681d2f0d322150108f2e13942701465d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239977094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b90b912eff8be47beaf633eac0f34372051083db71d97397d117afdd47edddc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:52:06 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:52:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Sat, 16 Dec 2023 11:52:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be3a4ab401992c037769ef60e29a9aef0f28fd84e73795832976c389cfd4a2e`  
		Last Modified: Sat, 16 Dec 2023 11:58:16 GMT  
		Size: 211.6 MB (211576812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ce66fcab37a87aff200a146e3e9b0e9f3c7532a094157534aba45a48b5a72053
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250300124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fdea2989c157748ca4819b4138ca6b988510b4e744ea02ce013d4113cac9f8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:39:33 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:39:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Sat, 16 Dec 2023 11:39:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420d2b5e794fb90690f913aa3d5b5a4a5e913cfe60e94dfcec283423a17f99b0`  
		Last Modified: Sat, 16 Dec 2023 11:47:35 GMT  
		Size: 214.6 MB (214644837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
