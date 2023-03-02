## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:3738e9eea1e21533642c15865ec6f022cfd60a364fa32361caf42a0c3f00c042
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
$ docker pull sapmachine@sha256:253909009735c5fa006ec75a20a5ee051b0a82721f24899bfd621aeeebbf53a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231058835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b01c51b37e753b4ec19595dae83129cb73c99daa797e2943688b6da7670cdaa`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:55:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:56:29 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:56:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 02 Mar 2023 04:56:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbd1ef482bb7f6d134f88a74c3373576d23dffa4b7de76d8eaaf911cbb884d9`  
		Last Modified: Thu, 02 Mar 2023 04:57:20 GMT  
		Size: 7.8 MB (7756310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a2fe7502296e2b1cbb40bff213aa1fa9b734aba274ab093b32e518b97f5eda`  
		Last Modified: Thu, 02 Mar 2023 04:57:50 GMT  
		Size: 196.1 MB (196108004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3f273140ea5fcaf9642e47088d63796e00ab219c1fa51e2160466eb6f93d5f8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240841128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca190d901a35e5e96c87a48587157981b1640f860c0e836b516f17007864f0b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 05:13:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 05:16:57 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 05:17:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 02 Mar 2023 05:17:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c1a1c48cee329c0d94333d1fb94839d2d5166aedacdb58c84e5d4b61cedae5`  
		Last Modified: Thu, 02 Mar 2023 05:19:36 GMT  
		Size: 9.3 MB (9316642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cead3eaa13ac84b931225f1df185bf9be6713733cf454d649750bdf4f81fa394`  
		Last Modified: Thu, 02 Mar 2023 05:20:31 GMT  
		Size: 198.2 MB (198224107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
