## `mono:6-slim`

```console
$ docker pull mono@sha256:23c4b774797417a1b890fd12dc8991291af44712dd440488455187e6090690ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:eb5ff6e26b3ca77b217977860be82905c329172a4cff5392de3411b0ab1f4335
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94440684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef5a11161de059f27b7b52323a06d8069b72f09f9a94e5ccbe1840540c92fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:44:20 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 04 Aug 2020 23:44:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9430cf70b26259617fdf6dea56de0841e6a2d05e7996d61d9b457d837624f2c`  
		Last Modified: Tue, 04 Aug 2020 23:59:08 GMT  
		Size: 255.9 KB (255895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b84988e9412eb7cdedbd0cd734d319d6e7694cf8b8c6b50383a7d9d0bd65408`  
		Last Modified: Tue, 04 Aug 2020 23:59:20 GMT  
		Size: 67.1 MB (67092668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:b0f43e9a57bbeaab6418b95863772cfe1c6ae615bd76182aab233c832e31829b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754880056c4b3b86d96022e96a2dcc933375a19bcd8cf97c1999857a9563e52f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:35:19 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 01:35:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:36:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf48cbcfca5d29687c690c6fddde7fd04dc76338af2e71db04388238c0e68c43`  
		Last Modified: Thu, 10 Sep 2020 01:44:16 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7c9921538853e2ba44c836f2160417c241ff09e40b2d8e831821a1c6671e0`  
		Last Modified: Thu, 10 Sep 2020 01:44:26 GMT  
		Size: 26.5 MB (26530542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bde9b3824ab39695651fdfbc0e193fec8077a22b43c6432e0da9e5e58cc64b18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48685264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a03a568c126139860bb8343cc4b1c68f73ce3929a413ed52d4293eb52bed37`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:44:49 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:45:20 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:46:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380cdf1d37e15da48ba99070332d703dd9658d7781d6c7615eccee8851e14181`  
		Last Modified: Thu, 10 Sep 2020 02:54:57 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2d0e80b990eda6fe103f55119aedccb613a1d53d5b94b21186a32d3bbb0fa4`  
		Last Modified: Thu, 10 Sep 2020 02:55:06 GMT  
		Size: 25.7 MB (25729434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:6a1929c74aa070a55437a4f53677f4813dc65db4a15e9d821e3242bb440fa32f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57854955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f99b38a2f8cd554d4ded6c9a639de090126a8f51ba5ff206ec6bddf01dc7471`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:37:26 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 04 Aug 2020 17:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:38:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c595d8e10cd557d558d9e01ea076ef5da32ff718496be7608c84052e132b7834`  
		Last Modified: Tue, 04 Aug 2020 17:44:39 GMT  
		Size: 255.9 KB (255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bab51ec9515275a4f4bdc9f85946d1c40dc270848c6a487bc1f7fce5e36441`  
		Last Modified: Tue, 04 Aug 2020 17:44:52 GMT  
		Size: 31.7 MB (31749732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:2a9fab669e67041d25fdb369e933e3590824683abc66c630331417cfc165ba14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99142396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc2e1b2ceaeba60abb7a332bf82875ce0709f9c94f0eda84ca9f39bc53f8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:37:15 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 10 Sep 2020 02:37:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:38:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a5b4050174b76ed23d2d3bbb436d66899f93eba56641cd1faf810f75242c67`  
		Last Modified: Thu, 10 Sep 2020 02:44:13 GMT  
		Size: 255.8 KB (255795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251d8984c7c93892d00e6d7ad246f6eb96eb1ccef85f2aa4931d99e3fa536d0`  
		Last Modified: Thu, 10 Sep 2020 02:44:42 GMT  
		Size: 71.1 MB (71136267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:64722be03610dd85f6e7084a7724051a45b6d36da870c298b373abd5d4d4f139
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60123819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe99b4bc17c93d39b69333043918c3be3607f0985fa38459715c3b238085ba7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:29:15 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 04 Aug 2020 09:30:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:31:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd17d4162fa0172eeb1ffbb8a68bbbd3e8cd9d7807b60534c8715d78b939a5fd`  
		Last Modified: Tue, 04 Aug 2020 09:46:37 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d11a57362d5a6f3eed02468a4517dcb2653afa80dfbdff1a90725d784884963`  
		Last Modified: Tue, 04 Aug 2020 09:46:44 GMT  
		Size: 29.3 MB (29349935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
