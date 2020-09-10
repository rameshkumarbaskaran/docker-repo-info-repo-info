<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.8`](#mono68)
-	[`mono:6.8.0`](#mono680)
-	[`mono:6.8.0.123`](#mono680123)
-	[`mono:6.8.0.123-slim`](#mono680123-slim)
-	[`mono:6.8.0-slim`](#mono680-slim)
-	[`mono:6.8-slim`](#mono68-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:e800281dce4b7d7f2b3119415ba23f5394d7252b1ef13f057cc31f0f70623aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:18384bd31a4d16c228a893267a7943b7aea1f263f75ed23cd9a139e5cd844b1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224729287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda9bfba7e60c3f947af76aa7f409fcb0ba0016af425a2c9469882c4cf09f2c`
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
# Tue, 04 Aug 2020 23:58:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:68ccfe204fbb0bc2d09a50ebeab14fc143f44a9a8fbf474784b0bb3b83f805a6`  
		Last Modified: Wed, 05 Aug 2020 00:00:24 GMT  
		Size: 130.3 MB (130288603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:d5258fbf327874144369bc85a96a28cd39d33424b6721ada7f59ffa3b12e9c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180581617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a0822afb7cdfadc889e7fa04c9808837d5277985bc6043a9e513e98ae44064`
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
# Thu, 10 Sep 2020 01:43:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:f0368391f22557528107e48ee0648f39d4efea0f944ff643e51ca88009b6eae6`  
		Last Modified: Thu, 10 Sep 2020 01:46:26 GMT  
		Size: 129.0 MB (128959139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:3c632c3e00c8c62f363191e51091a7e9b525708b7890d77f85b7004ea09cc98e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176481517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86817144f3250f1c4c03c5600aaef40dcf246bbf4464ec1f75fbe6dfa6f6b71`
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
# Thu, 10 Sep 2020 02:54:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:3c23bcd60f3ff4176c55bb33924aefcc999afddebde501b2c64d3d4964182b87`  
		Last Modified: Thu, 10 Sep 2020 02:57:00 GMT  
		Size: 127.8 MB (127796253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bd010af8be4554608415cca985d302543632b1f1823ac237bb40fa13bcd96124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203293612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ff1067bbf444ef4ff004624b28184195c00cb52b63828fcf4a3958029b1358`
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
# Tue, 04 Aug 2020 17:43:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ee22b804b8cafe31276889c5e678c467b171259147a4fdef109eea92fd6f4bf7`  
		Last Modified: Tue, 04 Aug 2020 17:47:01 GMT  
		Size: 145.4 MB (145438657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
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
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:62912aaadfc996b2e153f528812ceb6a2c074565deb9c97485f51d4d74e40612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192083470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ee9bc4061ae057ad9a252dd67dd5a8ce7e58ba14becc7b87dfbb80bf812008`
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
# Tue, 04 Aug 2020 09:45:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:0919fec4e424098a16af1cfc29104b97cabaace0158514dd3e83a7d414135fa8`  
		Last Modified: Tue, 04 Aug 2020 09:48:14 GMT  
		Size: 132.0 MB (131959651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:e800281dce4b7d7f2b3119415ba23f5394d7252b1ef13f057cc31f0f70623aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:18384bd31a4d16c228a893267a7943b7aea1f263f75ed23cd9a139e5cd844b1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224729287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda9bfba7e60c3f947af76aa7f409fcb0ba0016af425a2c9469882c4cf09f2c`
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
# Tue, 04 Aug 2020 23:58:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:68ccfe204fbb0bc2d09a50ebeab14fc143f44a9a8fbf474784b0bb3b83f805a6`  
		Last Modified: Wed, 05 Aug 2020 00:00:24 GMT  
		Size: 130.3 MB (130288603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:d5258fbf327874144369bc85a96a28cd39d33424b6721ada7f59ffa3b12e9c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180581617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a0822afb7cdfadc889e7fa04c9808837d5277985bc6043a9e513e98ae44064`
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
# Thu, 10 Sep 2020 01:43:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:f0368391f22557528107e48ee0648f39d4efea0f944ff643e51ca88009b6eae6`  
		Last Modified: Thu, 10 Sep 2020 01:46:26 GMT  
		Size: 129.0 MB (128959139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:3c632c3e00c8c62f363191e51091a7e9b525708b7890d77f85b7004ea09cc98e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176481517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86817144f3250f1c4c03c5600aaef40dcf246bbf4464ec1f75fbe6dfa6f6b71`
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
# Thu, 10 Sep 2020 02:54:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:3c23bcd60f3ff4176c55bb33924aefcc999afddebde501b2c64d3d4964182b87`  
		Last Modified: Thu, 10 Sep 2020 02:57:00 GMT  
		Size: 127.8 MB (127796253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bd010af8be4554608415cca985d302543632b1f1823ac237bb40fa13bcd96124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203293612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ff1067bbf444ef4ff004624b28184195c00cb52b63828fcf4a3958029b1358`
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
# Tue, 04 Aug 2020 17:43:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ee22b804b8cafe31276889c5e678c467b171259147a4fdef109eea92fd6f4bf7`  
		Last Modified: Tue, 04 Aug 2020 17:47:01 GMT  
		Size: 145.4 MB (145438657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
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
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:62912aaadfc996b2e153f528812ceb6a2c074565deb9c97485f51d4d74e40612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192083470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ee9bc4061ae057ad9a252dd67dd5a8ce7e58ba14becc7b87dfbb80bf812008`
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
# Tue, 04 Aug 2020 09:45:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:0919fec4e424098a16af1cfc29104b97cabaace0158514dd3e83a7d414135fa8`  
		Last Modified: Tue, 04 Aug 2020 09:48:14 GMT  
		Size: 132.0 MB (131959651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:e800281dce4b7d7f2b3119415ba23f5394d7252b1ef13f057cc31f0f70623aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:18384bd31a4d16c228a893267a7943b7aea1f263f75ed23cd9a139e5cd844b1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224729287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda9bfba7e60c3f947af76aa7f409fcb0ba0016af425a2c9469882c4cf09f2c`
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
# Tue, 04 Aug 2020 23:58:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:68ccfe204fbb0bc2d09a50ebeab14fc143f44a9a8fbf474784b0bb3b83f805a6`  
		Last Modified: Wed, 05 Aug 2020 00:00:24 GMT  
		Size: 130.3 MB (130288603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:d5258fbf327874144369bc85a96a28cd39d33424b6721ada7f59ffa3b12e9c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180581617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a0822afb7cdfadc889e7fa04c9808837d5277985bc6043a9e513e98ae44064`
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
# Thu, 10 Sep 2020 01:43:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:f0368391f22557528107e48ee0648f39d4efea0f944ff643e51ca88009b6eae6`  
		Last Modified: Thu, 10 Sep 2020 01:46:26 GMT  
		Size: 129.0 MB (128959139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:3c632c3e00c8c62f363191e51091a7e9b525708b7890d77f85b7004ea09cc98e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176481517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86817144f3250f1c4c03c5600aaef40dcf246bbf4464ec1f75fbe6dfa6f6b71`
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
# Thu, 10 Sep 2020 02:54:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:3c23bcd60f3ff4176c55bb33924aefcc999afddebde501b2c64d3d4964182b87`  
		Last Modified: Thu, 10 Sep 2020 02:57:00 GMT  
		Size: 127.8 MB (127796253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bd010af8be4554608415cca985d302543632b1f1823ac237bb40fa13bcd96124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203293612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ff1067bbf444ef4ff004624b28184195c00cb52b63828fcf4a3958029b1358`
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
# Tue, 04 Aug 2020 17:43:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ee22b804b8cafe31276889c5e678c467b171259147a4fdef109eea92fd6f4bf7`  
		Last Modified: Tue, 04 Aug 2020 17:47:01 GMT  
		Size: 145.4 MB (145438657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
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
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:62912aaadfc996b2e153f528812ceb6a2c074565deb9c97485f51d4d74e40612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192083470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ee9bc4061ae057ad9a252dd67dd5a8ce7e58ba14becc7b87dfbb80bf812008`
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
# Tue, 04 Aug 2020 09:45:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:0919fec4e424098a16af1cfc29104b97cabaace0158514dd3e83a7d414135fa8`  
		Last Modified: Tue, 04 Aug 2020 09:48:14 GMT  
		Size: 132.0 MB (131959651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:e800281dce4b7d7f2b3119415ba23f5394d7252b1ef13f057cc31f0f70623aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:18384bd31a4d16c228a893267a7943b7aea1f263f75ed23cd9a139e5cd844b1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224729287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda9bfba7e60c3f947af76aa7f409fcb0ba0016af425a2c9469882c4cf09f2c`
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
# Tue, 04 Aug 2020 23:58:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:68ccfe204fbb0bc2d09a50ebeab14fc143f44a9a8fbf474784b0bb3b83f805a6`  
		Last Modified: Wed, 05 Aug 2020 00:00:24 GMT  
		Size: 130.3 MB (130288603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:d5258fbf327874144369bc85a96a28cd39d33424b6721ada7f59ffa3b12e9c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180581617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a0822afb7cdfadc889e7fa04c9808837d5277985bc6043a9e513e98ae44064`
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
# Thu, 10 Sep 2020 01:43:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:f0368391f22557528107e48ee0648f39d4efea0f944ff643e51ca88009b6eae6`  
		Last Modified: Thu, 10 Sep 2020 01:46:26 GMT  
		Size: 129.0 MB (128959139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:3c632c3e00c8c62f363191e51091a7e9b525708b7890d77f85b7004ea09cc98e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176481517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86817144f3250f1c4c03c5600aaef40dcf246bbf4464ec1f75fbe6dfa6f6b71`
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
# Thu, 10 Sep 2020 02:54:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:3c23bcd60f3ff4176c55bb33924aefcc999afddebde501b2c64d3d4964182b87`  
		Last Modified: Thu, 10 Sep 2020 02:57:00 GMT  
		Size: 127.8 MB (127796253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bd010af8be4554608415cca985d302543632b1f1823ac237bb40fa13bcd96124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203293612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ff1067bbf444ef4ff004624b28184195c00cb52b63828fcf4a3958029b1358`
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
# Tue, 04 Aug 2020 17:43:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ee22b804b8cafe31276889c5e678c467b171259147a4fdef109eea92fd6f4bf7`  
		Last Modified: Tue, 04 Aug 2020 17:47:01 GMT  
		Size: 145.4 MB (145438657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
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
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:62912aaadfc996b2e153f528812ceb6a2c074565deb9c97485f51d4d74e40612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192083470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ee9bc4061ae057ad9a252dd67dd5a8ce7e58ba14becc7b87dfbb80bf812008`
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
# Tue, 04 Aug 2020 09:45:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:0919fec4e424098a16af1cfc29104b97cabaace0158514dd3e83a7d414135fa8`  
		Last Modified: Tue, 04 Aug 2020 09:48:14 GMT  
		Size: 132.0 MB (131959651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

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

### `mono:6.10.0.104-slim` - linux; amd64

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

### `mono:6.10.0.104-slim` - linux; arm variant v5

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

### `mono:6.10.0.104-slim` - linux; arm variant v7

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

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

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

### `mono:6.10.0.104-slim` - linux; 386

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

### `mono:6.10.0.104-slim` - linux; ppc64le

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

## `mono:6.10.0-slim`

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

### `mono:6.10.0-slim` - linux; amd64

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

### `mono:6.10.0-slim` - linux; arm variant v5

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

### `mono:6.10.0-slim` - linux; arm variant v7

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

### `mono:6.10.0-slim` - linux; arm64 variant v8

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

### `mono:6.10.0-slim` - linux; 386

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

### `mono:6.10.0-slim` - linux; ppc64le

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

## `mono:6.10-slim`

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

### `mono:6.10-slim` - linux; amd64

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

### `mono:6.10-slim` - linux; arm variant v5

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

### `mono:6.10-slim` - linux; arm variant v7

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

### `mono:6.10-slim` - linux; arm64 variant v8

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

### `mono:6.10-slim` - linux; 386

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

### `mono:6.10-slim` - linux; ppc64le

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

## `mono:6.8`

```console
$ docker pull mono@sha256:533193b26b795b7b5e01c0deed15e6ffcfa56ed2d5f9de23dd77714a15ec2454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8` - linux; amd64

```console
$ docker pull mono@sha256:0e2a9bfe028000a7242f8a6347e70d772547dc535df0de6710879b0f325514b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240618156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4113fea10f7865d408fd89b82554d8afbd4376df661d90e77d622ffcf507a1bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:43:40 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 23:43:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 23:52:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117f11b67da002da576a9762a0b578f5f21bc08c4e889e3b9a178814da2f08f`  
		Last Modified: Tue, 04 Aug 2020 23:58:49 GMT  
		Size: 255.9 KB (255915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ced73c25324c37ecab874524e1769ba866fc024dd15213579244c6a3ee3c7c`  
		Last Modified: Tue, 04 Aug 2020 23:59:03 GMT  
		Size: 67.1 MB (67084264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c571404027a01e77f471a77be715950669a9bdf59adcd9760d1bc9fb1545bab0`  
		Last Modified: Tue, 04 Aug 2020 23:59:57 GMT  
		Size: 146.2 MB (146185856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:316f066dc1abadfd3cae0cd9e051a4a9d8d86c21ecef4382acee987952314e1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179922558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd4ad8b4ba81d15dc13f4b69ab1b782124f3c08f7d95d18c632d2f413bf34cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:33:46 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 01:34:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:35:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 01:39:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e539909c49f82aff613ba2f8ae5a4b006b6005548b402d52901a3812fef3474`  
		Last Modified: Thu, 10 Sep 2020 01:43:59 GMT  
		Size: 256.0 KB (256032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90670588f8748f305d23a0846407e8f125e42d139026bc1d28d7e781519215df`  
		Last Modified: Thu, 10 Sep 2020 01:44:08 GMT  
		Size: 26.5 MB (26542632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656a03eda7954b3e931ad5ea9e2830868448700f8776adcb4238a046700f4f`  
		Last Modified: Thu, 10 Sep 2020 01:45:25 GMT  
		Size: 128.3 MB (128287920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:6934ae1eb80980883cbfe201fe995aa78cd1449b49af82735b52e30ca88a8f63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175798927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e5aaccfc67dcb88ac55ec1ed3068b37801411bfcbf99e7dd50c1f9e95b4f92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:43:02 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:43:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:44:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:50:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132272fbfc84f00c2b12ffa3e790ec573e8d4108e79b3218892a9956297e5a4`  
		Last Modified: Thu, 10 Sep 2020 02:54:39 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d37dbedc88ce7ba6bcb43906098a63dda65957e2cf8971ab3e12dc00ebc6c0`  
		Last Modified: Thu, 10 Sep 2020 02:54:48 GMT  
		Size: 25.7 MB (25726406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12830a36fdcbecff977db11d08416ae0fd37ced19cb94fbfb44091ae18eba96c`  
		Last Modified: Thu, 10 Sep 2020 02:56:09 GMT  
		Size: 127.1 MB (127116693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ee203e6697c8c2853f5274aba5a8ab2d36896b34b5a624fb82c4f5ca86c8c4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202437043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5067583861bc3255f61548abdd7331fefa7a2243db167523ac113470fc28e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:36:19 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 17:36:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:37:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 17:41:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5c5db189d99583a1ab3fc84f5dfe6f03a8189c3e830c8a99eb4114b0bec4c`  
		Last Modified: Tue, 04 Aug 2020 17:44:21 GMT  
		Size: 255.9 KB (255943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e42721b098c45fb576e589dea336cb548ac4cf8487af5d55577e4cfa35270`  
		Last Modified: Tue, 04 Aug 2020 17:44:31 GMT  
		Size: 31.7 MB (31694691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be8d22992da66196be7289b2498ddea6f00bb874f08753482052eb6ec18907`  
		Last Modified: Tue, 04 Aug 2020 17:45:58 GMT  
		Size: 144.6 MB (144637108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:0c38cc7c1f3753e0ccf036502e97fe356961431f342cd5616d3bb0e174bd7be8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249227694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c9b17ca8f0b950231189ae43c79238a8279d76221f31a2478dd7563e7bc684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:40:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6598ae0ae4aad9c2f4d2778c76e02ccff85f7b4ae078a9180e107b2a56e165`  
		Last Modified: Thu, 10 Sep 2020 02:45:39 GMT  
		Size: 150.1 MB (150115422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; ppc64le

```console
$ docker pull mono@sha256:83d4d6c993a052113b02cd80bcb154f79fb7ae0d59011b84094eb67893c467bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191346564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3a05aa14d22384d84bb9771edfa36e0563a926805031356e4be414da288dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:26:31 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 09:27:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:28:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 09:39:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026c875a0a82fa3f068bb859492d057de0c69e50636092b4d846ae58211fcc9b`  
		Last Modified: Tue, 04 Aug 2020 09:46:17 GMT  
		Size: 256.1 KB (256084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1fcb481278f1916c49752ade88c194f559a788eaaca8782531548dc14e809c`  
		Last Modified: Tue, 04 Aug 2020 09:46:25 GMT  
		Size: 29.3 MB (29330738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3507e1d1526e8bd590c225ac7256843161d2b2152811e45c822cf63dd1d67c5a`  
		Last Modified: Tue, 04 Aug 2020 09:47:28 GMT  
		Size: 131.2 MB (131241898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0`

```console
$ docker pull mono@sha256:533193b26b795b7b5e01c0deed15e6ffcfa56ed2d5f9de23dd77714a15ec2454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0` - linux; amd64

```console
$ docker pull mono@sha256:0e2a9bfe028000a7242f8a6347e70d772547dc535df0de6710879b0f325514b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240618156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4113fea10f7865d408fd89b82554d8afbd4376df661d90e77d622ffcf507a1bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:43:40 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 23:43:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 23:52:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117f11b67da002da576a9762a0b578f5f21bc08c4e889e3b9a178814da2f08f`  
		Last Modified: Tue, 04 Aug 2020 23:58:49 GMT  
		Size: 255.9 KB (255915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ced73c25324c37ecab874524e1769ba866fc024dd15213579244c6a3ee3c7c`  
		Last Modified: Tue, 04 Aug 2020 23:59:03 GMT  
		Size: 67.1 MB (67084264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c571404027a01e77f471a77be715950669a9bdf59adcd9760d1bc9fb1545bab0`  
		Last Modified: Tue, 04 Aug 2020 23:59:57 GMT  
		Size: 146.2 MB (146185856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:316f066dc1abadfd3cae0cd9e051a4a9d8d86c21ecef4382acee987952314e1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179922558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd4ad8b4ba81d15dc13f4b69ab1b782124f3c08f7d95d18c632d2f413bf34cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:33:46 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 01:34:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:35:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 01:39:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e539909c49f82aff613ba2f8ae5a4b006b6005548b402d52901a3812fef3474`  
		Last Modified: Thu, 10 Sep 2020 01:43:59 GMT  
		Size: 256.0 KB (256032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90670588f8748f305d23a0846407e8f125e42d139026bc1d28d7e781519215df`  
		Last Modified: Thu, 10 Sep 2020 01:44:08 GMT  
		Size: 26.5 MB (26542632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656a03eda7954b3e931ad5ea9e2830868448700f8776adcb4238a046700f4f`  
		Last Modified: Thu, 10 Sep 2020 01:45:25 GMT  
		Size: 128.3 MB (128287920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:6934ae1eb80980883cbfe201fe995aa78cd1449b49af82735b52e30ca88a8f63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175798927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e5aaccfc67dcb88ac55ec1ed3068b37801411bfcbf99e7dd50c1f9e95b4f92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:43:02 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:43:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:44:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:50:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132272fbfc84f00c2b12ffa3e790ec573e8d4108e79b3218892a9956297e5a4`  
		Last Modified: Thu, 10 Sep 2020 02:54:39 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d37dbedc88ce7ba6bcb43906098a63dda65957e2cf8971ab3e12dc00ebc6c0`  
		Last Modified: Thu, 10 Sep 2020 02:54:48 GMT  
		Size: 25.7 MB (25726406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12830a36fdcbecff977db11d08416ae0fd37ced19cb94fbfb44091ae18eba96c`  
		Last Modified: Thu, 10 Sep 2020 02:56:09 GMT  
		Size: 127.1 MB (127116693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ee203e6697c8c2853f5274aba5a8ab2d36896b34b5a624fb82c4f5ca86c8c4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202437043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5067583861bc3255f61548abdd7331fefa7a2243db167523ac113470fc28e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:36:19 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 17:36:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:37:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 17:41:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5c5db189d99583a1ab3fc84f5dfe6f03a8189c3e830c8a99eb4114b0bec4c`  
		Last Modified: Tue, 04 Aug 2020 17:44:21 GMT  
		Size: 255.9 KB (255943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e42721b098c45fb576e589dea336cb548ac4cf8487af5d55577e4cfa35270`  
		Last Modified: Tue, 04 Aug 2020 17:44:31 GMT  
		Size: 31.7 MB (31694691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be8d22992da66196be7289b2498ddea6f00bb874f08753482052eb6ec18907`  
		Last Modified: Tue, 04 Aug 2020 17:45:58 GMT  
		Size: 144.6 MB (144637108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:0c38cc7c1f3753e0ccf036502e97fe356961431f342cd5616d3bb0e174bd7be8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249227694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c9b17ca8f0b950231189ae43c79238a8279d76221f31a2478dd7563e7bc684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:40:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6598ae0ae4aad9c2f4d2778c76e02ccff85f7b4ae078a9180e107b2a56e165`  
		Last Modified: Thu, 10 Sep 2020 02:45:39 GMT  
		Size: 150.1 MB (150115422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; ppc64le

```console
$ docker pull mono@sha256:83d4d6c993a052113b02cd80bcb154f79fb7ae0d59011b84094eb67893c467bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191346564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3a05aa14d22384d84bb9771edfa36e0563a926805031356e4be414da288dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:26:31 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 09:27:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:28:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 09:39:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026c875a0a82fa3f068bb859492d057de0c69e50636092b4d846ae58211fcc9b`  
		Last Modified: Tue, 04 Aug 2020 09:46:17 GMT  
		Size: 256.1 KB (256084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1fcb481278f1916c49752ade88c194f559a788eaaca8782531548dc14e809c`  
		Last Modified: Tue, 04 Aug 2020 09:46:25 GMT  
		Size: 29.3 MB (29330738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3507e1d1526e8bd590c225ac7256843161d2b2152811e45c822cf63dd1d67c5a`  
		Last Modified: Tue, 04 Aug 2020 09:47:28 GMT  
		Size: 131.2 MB (131241898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.123`

```console
$ docker pull mono@sha256:533193b26b795b7b5e01c0deed15e6ffcfa56ed2d5f9de23dd77714a15ec2454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.123` - linux; amd64

```console
$ docker pull mono@sha256:0e2a9bfe028000a7242f8a6347e70d772547dc535df0de6710879b0f325514b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240618156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4113fea10f7865d408fd89b82554d8afbd4376df661d90e77d622ffcf507a1bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:43:40 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 23:43:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 23:52:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117f11b67da002da576a9762a0b578f5f21bc08c4e889e3b9a178814da2f08f`  
		Last Modified: Tue, 04 Aug 2020 23:58:49 GMT  
		Size: 255.9 KB (255915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ced73c25324c37ecab874524e1769ba866fc024dd15213579244c6a3ee3c7c`  
		Last Modified: Tue, 04 Aug 2020 23:59:03 GMT  
		Size: 67.1 MB (67084264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c571404027a01e77f471a77be715950669a9bdf59adcd9760d1bc9fb1545bab0`  
		Last Modified: Tue, 04 Aug 2020 23:59:57 GMT  
		Size: 146.2 MB (146185856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; arm variant v5

```console
$ docker pull mono@sha256:316f066dc1abadfd3cae0cd9e051a4a9d8d86c21ecef4382acee987952314e1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179922558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd4ad8b4ba81d15dc13f4b69ab1b782124f3c08f7d95d18c632d2f413bf34cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:33:46 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 01:34:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:35:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 01:39:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e539909c49f82aff613ba2f8ae5a4b006b6005548b402d52901a3812fef3474`  
		Last Modified: Thu, 10 Sep 2020 01:43:59 GMT  
		Size: 256.0 KB (256032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90670588f8748f305d23a0846407e8f125e42d139026bc1d28d7e781519215df`  
		Last Modified: Thu, 10 Sep 2020 01:44:08 GMT  
		Size: 26.5 MB (26542632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656a03eda7954b3e931ad5ea9e2830868448700f8776adcb4238a046700f4f`  
		Last Modified: Thu, 10 Sep 2020 01:45:25 GMT  
		Size: 128.3 MB (128287920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; arm variant v7

```console
$ docker pull mono@sha256:6934ae1eb80980883cbfe201fe995aa78cd1449b49af82735b52e30ca88a8f63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175798927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e5aaccfc67dcb88ac55ec1ed3068b37801411bfcbf99e7dd50c1f9e95b4f92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:43:02 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:43:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:44:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:50:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132272fbfc84f00c2b12ffa3e790ec573e8d4108e79b3218892a9956297e5a4`  
		Last Modified: Thu, 10 Sep 2020 02:54:39 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d37dbedc88ce7ba6bcb43906098a63dda65957e2cf8971ab3e12dc00ebc6c0`  
		Last Modified: Thu, 10 Sep 2020 02:54:48 GMT  
		Size: 25.7 MB (25726406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12830a36fdcbecff977db11d08416ae0fd37ced19cb94fbfb44091ae18eba96c`  
		Last Modified: Thu, 10 Sep 2020 02:56:09 GMT  
		Size: 127.1 MB (127116693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ee203e6697c8c2853f5274aba5a8ab2d36896b34b5a624fb82c4f5ca86c8c4c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202437043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5067583861bc3255f61548abdd7331fefa7a2243db167523ac113470fc28e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:36:19 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 17:36:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:37:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 17:41:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5c5db189d99583a1ab3fc84f5dfe6f03a8189c3e830c8a99eb4114b0bec4c`  
		Last Modified: Tue, 04 Aug 2020 17:44:21 GMT  
		Size: 255.9 KB (255943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e42721b098c45fb576e589dea336cb548ac4cf8487af5d55577e4cfa35270`  
		Last Modified: Tue, 04 Aug 2020 17:44:31 GMT  
		Size: 31.7 MB (31694691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be8d22992da66196be7289b2498ddea6f00bb874f08753482052eb6ec18907`  
		Last Modified: Tue, 04 Aug 2020 17:45:58 GMT  
		Size: 144.6 MB (144637108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; 386

```console
$ docker pull mono@sha256:0c38cc7c1f3753e0ccf036502e97fe356961431f342cd5616d3bb0e174bd7be8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249227694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c9b17ca8f0b950231189ae43c79238a8279d76221f31a2478dd7563e7bc684`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 10 Sep 2020 02:40:54 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6598ae0ae4aad9c2f4d2778c76e02ccff85f7b4ae078a9180e107b2a56e165`  
		Last Modified: Thu, 10 Sep 2020 02:45:39 GMT  
		Size: 150.1 MB (150115422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123` - linux; ppc64le

```console
$ docker pull mono@sha256:83d4d6c993a052113b02cd80bcb154f79fb7ae0d59011b84094eb67893c467bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191346564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c3a05aa14d22384d84bb9771edfa36e0563a926805031356e4be414da288dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:26:31 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 09:27:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:28:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 04 Aug 2020 09:39:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026c875a0a82fa3f068bb859492d057de0c69e50636092b4d846ae58211fcc9b`  
		Last Modified: Tue, 04 Aug 2020 09:46:17 GMT  
		Size: 256.1 KB (256084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1fcb481278f1916c49752ade88c194f559a788eaaca8782531548dc14e809c`  
		Last Modified: Tue, 04 Aug 2020 09:46:25 GMT  
		Size: 29.3 MB (29330738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3507e1d1526e8bd590c225ac7256843161d2b2152811e45c822cf63dd1d67c5a`  
		Last Modified: Tue, 04 Aug 2020 09:47:28 GMT  
		Size: 131.2 MB (131241898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.123-slim`

```console
$ docker pull mono@sha256:65c1c3dc331ba2bf20de49f5e842b7b9832e58ec1cd47c2445ebbabce53887af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.123-slim` - linux; amd64

```console
$ docker pull mono@sha256:d81708f27a892ef8902b81f02585a70a4016030406d046c8c60658ccdcd4c82a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1467b20f51203a0a93b7767f5cb66ffa01f31e4dcad3150ea535aa1b6fdadc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:43:40 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 23:43:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117f11b67da002da576a9762a0b578f5f21bc08c4e889e3b9a178814da2f08f`  
		Last Modified: Tue, 04 Aug 2020 23:58:49 GMT  
		Size: 255.9 KB (255915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ced73c25324c37ecab874524e1769ba866fc024dd15213579244c6a3ee3c7c`  
		Last Modified: Tue, 04 Aug 2020 23:59:03 GMT  
		Size: 67.1 MB (67084264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:3186e80658b5de1c651a8c08fe4bf4c2e3201bc110a34654217fd1f94c8b9aed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041243db87bd28fff0ccd6614e6fd7895e32e3ecd99ea7f58ac6961bac2bcaa3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:33:46 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 01:34:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:35:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e539909c49f82aff613ba2f8ae5a4b006b6005548b402d52901a3812fef3474`  
		Last Modified: Thu, 10 Sep 2020 01:43:59 GMT  
		Size: 256.0 KB (256032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90670588f8748f305d23a0846407e8f125e42d139026bc1d28d7e781519215df`  
		Last Modified: Thu, 10 Sep 2020 01:44:08 GMT  
		Size: 26.5 MB (26542632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:884e87555c0a9f0e3047bea88ec31451027b27ce4ad69f8b8016360fde48ff03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef51a81a0faef66947adec249cc7b73697002401c8f6f75f9aa881a883e4417b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:43:02 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:43:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:44:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132272fbfc84f00c2b12ffa3e790ec573e8d4108e79b3218892a9956297e5a4`  
		Last Modified: Thu, 10 Sep 2020 02:54:39 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d37dbedc88ce7ba6bcb43906098a63dda65957e2cf8971ab3e12dc00ebc6c0`  
		Last Modified: Thu, 10 Sep 2020 02:54:48 GMT  
		Size: 25.7 MB (25726406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:40f78bb7b3b0e090622f6254fa9323628bbde8fd25244395ddd345091d8575ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57799935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57182a485ee10c02c94698cf3b00837486de71458a026716c906a98fd5c5014`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:36:19 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 17:36:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:37:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5c5db189d99583a1ab3fc84f5dfe6f03a8189c3e830c8a99eb4114b0bec4c`  
		Last Modified: Tue, 04 Aug 2020 17:44:21 GMT  
		Size: 255.9 KB (255943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e42721b098c45fb576e589dea336cb548ac4cf8487af5d55577e4cfa35270`  
		Last Modified: Tue, 04 Aug 2020 17:44:31 GMT  
		Size: 31.7 MB (31694691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; 386

```console
$ docker pull mono@sha256:d1ba26182ea9eeeec138e323c54257bf1651fba14495922974e132989a3c6e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701dfe0fd831da557161245b218185627513738fd6d2731b2d82aecfe2d1068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.123-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a0b8a6ce9486df53d247fdc2998795d4258dd0c7168a1a1b6acc335bd117b324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60104666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdfa3dffcd9091d55042027337b4f8772d3acf8b1b8e8997d6b22b32f89f40e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:26:31 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 09:27:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:28:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026c875a0a82fa3f068bb859492d057de0c69e50636092b4d846ae58211fcc9b`  
		Last Modified: Tue, 04 Aug 2020 09:46:17 GMT  
		Size: 256.1 KB (256084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1fcb481278f1916c49752ade88c194f559a788eaaca8782531548dc14e809c`  
		Last Modified: Tue, 04 Aug 2020 09:46:25 GMT  
		Size: 29.3 MB (29330738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:65c1c3dc331ba2bf20de49f5e842b7b9832e58ec1cd47c2445ebbabce53887af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:d81708f27a892ef8902b81f02585a70a4016030406d046c8c60658ccdcd4c82a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1467b20f51203a0a93b7767f5cb66ffa01f31e4dcad3150ea535aa1b6fdadc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:43:40 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 23:43:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117f11b67da002da576a9762a0b578f5f21bc08c4e889e3b9a178814da2f08f`  
		Last Modified: Tue, 04 Aug 2020 23:58:49 GMT  
		Size: 255.9 KB (255915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ced73c25324c37ecab874524e1769ba866fc024dd15213579244c6a3ee3c7c`  
		Last Modified: Tue, 04 Aug 2020 23:59:03 GMT  
		Size: 67.1 MB (67084264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:3186e80658b5de1c651a8c08fe4bf4c2e3201bc110a34654217fd1f94c8b9aed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041243db87bd28fff0ccd6614e6fd7895e32e3ecd99ea7f58ac6961bac2bcaa3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:33:46 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 01:34:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:35:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e539909c49f82aff613ba2f8ae5a4b006b6005548b402d52901a3812fef3474`  
		Last Modified: Thu, 10 Sep 2020 01:43:59 GMT  
		Size: 256.0 KB (256032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90670588f8748f305d23a0846407e8f125e42d139026bc1d28d7e781519215df`  
		Last Modified: Thu, 10 Sep 2020 01:44:08 GMT  
		Size: 26.5 MB (26542632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:884e87555c0a9f0e3047bea88ec31451027b27ce4ad69f8b8016360fde48ff03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef51a81a0faef66947adec249cc7b73697002401c8f6f75f9aa881a883e4417b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:43:02 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:43:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:44:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132272fbfc84f00c2b12ffa3e790ec573e8d4108e79b3218892a9956297e5a4`  
		Last Modified: Thu, 10 Sep 2020 02:54:39 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d37dbedc88ce7ba6bcb43906098a63dda65957e2cf8971ab3e12dc00ebc6c0`  
		Last Modified: Thu, 10 Sep 2020 02:54:48 GMT  
		Size: 25.7 MB (25726406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:40f78bb7b3b0e090622f6254fa9323628bbde8fd25244395ddd345091d8575ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57799935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57182a485ee10c02c94698cf3b00837486de71458a026716c906a98fd5c5014`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:36:19 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 17:36:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:37:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5c5db189d99583a1ab3fc84f5dfe6f03a8189c3e830c8a99eb4114b0bec4c`  
		Last Modified: Tue, 04 Aug 2020 17:44:21 GMT  
		Size: 255.9 KB (255943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e42721b098c45fb576e589dea336cb548ac4cf8487af5d55577e4cfa35270`  
		Last Modified: Tue, 04 Aug 2020 17:44:31 GMT  
		Size: 31.7 MB (31694691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:d1ba26182ea9eeeec138e323c54257bf1651fba14495922974e132989a3c6e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701dfe0fd831da557161245b218185627513738fd6d2731b2d82aecfe2d1068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a0b8a6ce9486df53d247fdc2998795d4258dd0c7168a1a1b6acc335bd117b324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60104666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdfa3dffcd9091d55042027337b4f8772d3acf8b1b8e8997d6b22b32f89f40e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:26:31 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 09:27:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:28:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026c875a0a82fa3f068bb859492d057de0c69e50636092b4d846ae58211fcc9b`  
		Last Modified: Tue, 04 Aug 2020 09:46:17 GMT  
		Size: 256.1 KB (256084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1fcb481278f1916c49752ade88c194f559a788eaaca8782531548dc14e809c`  
		Last Modified: Tue, 04 Aug 2020 09:46:25 GMT  
		Size: 29.3 MB (29330738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:65c1c3dc331ba2bf20de49f5e842b7b9832e58ec1cd47c2445ebbabce53887af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8-slim` - linux; amd64

```console
$ docker pull mono@sha256:d81708f27a892ef8902b81f02585a70a4016030406d046c8c60658ccdcd4c82a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94432300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1467b20f51203a0a93b7767f5cb66ffa01f31e4dcad3150ea535aa1b6fdadc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:43:40 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 23:43:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 23:44:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117f11b67da002da576a9762a0b578f5f21bc08c4e889e3b9a178814da2f08f`  
		Last Modified: Tue, 04 Aug 2020 23:58:49 GMT  
		Size: 255.9 KB (255915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ced73c25324c37ecab874524e1769ba866fc024dd15213579244c6a3ee3c7c`  
		Last Modified: Tue, 04 Aug 2020 23:59:03 GMT  
		Size: 67.1 MB (67084264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:3186e80658b5de1c651a8c08fe4bf4c2e3201bc110a34654217fd1f94c8b9aed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041243db87bd28fff0ccd6614e6fd7895e32e3ecd99ea7f58ac6961bac2bcaa3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:53:49 GMT
ADD file:34835d84d87e3ee1178aa150793d75a4d4a7a28c013ca3495dbcca2b570270bf in / 
# Wed, 09 Sep 2020 23:53:53 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:33:46 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 01:34:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 01:35:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0a51b5143468e1b44dafa16fea3541e28e369071f6837337ee95e37f0ad81d99`  
		Last Modified: Thu, 10 Sep 2020 00:02:48 GMT  
		Size: 24.8 MB (24835974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e539909c49f82aff613ba2f8ae5a4b006b6005548b402d52901a3812fef3474`  
		Last Modified: Thu, 10 Sep 2020 01:43:59 GMT  
		Size: 256.0 KB (256032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90670588f8748f305d23a0846407e8f125e42d139026bc1d28d7e781519215df`  
		Last Modified: Thu, 10 Sep 2020 01:44:08 GMT  
		Size: 26.5 MB (26542632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:884e87555c0a9f0e3047bea88ec31451027b27ce4ad69f8b8016360fde48ff03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48682234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef51a81a0faef66947adec249cc7b73697002401c8f6f75f9aa881a883e4417b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:08:04 GMT
ADD file:5ec0d2c3043ae64cb72698b0f6fe7387884f4195df962466215ce534d2208327 in / 
# Thu, 10 Sep 2020 00:08:06 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:43:02 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:43:31 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:44:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a7c65856610cb24c46ede2ffe313cbf933c44fa20ba213835af953646f3eb1ed`  
		Last Modified: Thu, 10 Sep 2020 00:17:52 GMT  
		Size: 22.7 MB (22699896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132272fbfc84f00c2b12ffa3e790ec573e8d4108e79b3218892a9956297e5a4`  
		Last Modified: Thu, 10 Sep 2020 02:54:39 GMT  
		Size: 255.9 KB (255932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d37dbedc88ce7ba6bcb43906098a63dda65957e2cf8971ab3e12dc00ebc6c0`  
		Last Modified: Thu, 10 Sep 2020 02:54:48 GMT  
		Size: 25.7 MB (25726406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:40f78bb7b3b0e090622f6254fa9323628bbde8fd25244395ddd345091d8575ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57799935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57182a485ee10c02c94698cf3b00837486de71458a026716c906a98fd5c5014`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 17:36:19 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 17:36:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 17:37:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5c5db189d99583a1ab3fc84f5dfe6f03a8189c3e830c8a99eb4114b0bec4c`  
		Last Modified: Tue, 04 Aug 2020 17:44:21 GMT  
		Size: 255.9 KB (255943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e42721b098c45fb576e589dea336cb548ac4cf8487af5d55577e4cfa35270`  
		Last Modified: Tue, 04 Aug 2020 17:44:31 GMT  
		Size: 31.7 MB (31694691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:d1ba26182ea9eeeec138e323c54257bf1651fba14495922974e132989a3c6e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b701dfe0fd831da557161245b218185627513738fd6d2731b2d82aecfe2d1068`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:40:19 GMT
ADD file:08dc20c9cd727ebf02cac6e4b287c3009274682174aee9222494491cd6c671b8 in / 
# Wed, 09 Sep 2020 23:40:19 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 02:35:58 GMT
ENV MONO_VERSION=6.8.0.123
# Thu, 10 Sep 2020 02:36:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 10 Sep 2020 02:36:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:31e6582dbd9f9a84903d46339df0c393a63d2cbfb001b06b3204653cceafcc61`  
		Last Modified: Wed, 09 Sep 2020 23:46:30 GMT  
		Size: 27.8 MB (27750334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad82c343652f6abb0aa2c6b4c58d68ba7bb6d70f0a52f9674b18a54d41bdabc`  
		Last Modified: Thu, 10 Sep 2020 02:43:37 GMT  
		Size: 255.8 KB (255778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4a52d2efb3aede424ea811ba691119d849c54bd5efda04c9f6c0cfaf84f4dd`  
		Last Modified: Thu, 10 Sep 2020 02:44:08 GMT  
		Size: 71.1 MB (71106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a0b8a6ce9486df53d247fdc2998795d4258dd0c7168a1a1b6acc335bd117b324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60104666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdfa3dffcd9091d55042027337b4f8772d3acf8b1b8e8997d6b22b32f89f40e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:26:31 GMT
ENV MONO_VERSION=6.8.0.123
# Tue, 04 Aug 2020 09:27:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 04 Aug 2020 09:28:57 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026c875a0a82fa3f068bb859492d057de0c69e50636092b4d846ae58211fcc9b`  
		Last Modified: Tue, 04 Aug 2020 09:46:17 GMT  
		Size: 256.1 KB (256084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1fcb481278f1916c49752ade88c194f559a788eaaca8782531548dc14e809c`  
		Last Modified: Tue, 04 Aug 2020 09:46:25 GMT  
		Size: 29.3 MB (29330738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `mono:latest`

```console
$ docker pull mono@sha256:e800281dce4b7d7f2b3119415ba23f5394d7252b1ef13f057cc31f0f70623aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:18384bd31a4d16c228a893267a7943b7aea1f263f75ed23cd9a139e5cd844b1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224729287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecda9bfba7e60c3f947af76aa7f409fcb0ba0016af425a2c9469882c4cf09f2c`
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
# Tue, 04 Aug 2020 23:58:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:68ccfe204fbb0bc2d09a50ebeab14fc143f44a9a8fbf474784b0bb3b83f805a6`  
		Last Modified: Wed, 05 Aug 2020 00:00:24 GMT  
		Size: 130.3 MB (130288603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:d5258fbf327874144369bc85a96a28cd39d33424b6721ada7f59ffa3b12e9c15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180581617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a0822afb7cdfadc889e7fa04c9808837d5277985bc6043a9e513e98ae44064`
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
# Thu, 10 Sep 2020 01:43:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:f0368391f22557528107e48ee0648f39d4efea0f944ff643e51ca88009b6eae6`  
		Last Modified: Thu, 10 Sep 2020 01:46:26 GMT  
		Size: 129.0 MB (128959139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:3c632c3e00c8c62f363191e51091a7e9b525708b7890d77f85b7004ea09cc98e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176481517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86817144f3250f1c4c03c5600aaef40dcf246bbf4464ec1f75fbe6dfa6f6b71`
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
# Thu, 10 Sep 2020 02:54:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:3c23bcd60f3ff4176c55bb33924aefcc999afddebde501b2c64d3d4964182b87`  
		Last Modified: Thu, 10 Sep 2020 02:57:00 GMT  
		Size: 127.8 MB (127796253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bd010af8be4554608415cca985d302543632b1f1823ac237bb40fa13bcd96124
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203293612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ff1067bbf444ef4ff004624b28184195c00cb52b63828fcf4a3958029b1358`
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
# Tue, 04 Aug 2020 17:43:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ee22b804b8cafe31276889c5e678c467b171259147a4fdef109eea92fd6f4bf7`  
		Last Modified: Tue, 04 Aug 2020 17:47:01 GMT  
		Size: 145.4 MB (145438657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:d111852f67f667bb664ca166bcaf57863be573e5f9abcf640261a13ce768af9f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670b9156ca83df138822e88a059b2ef4b85870178733601534fdb68cc075916`
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
# Thu, 10 Sep 2020 02:43:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:977fb5b989bb54968bfa64f742226d8805f4ec1552243874881f524b81fb29ae`  
		Last Modified: Thu, 10 Sep 2020 02:46:21 GMT  
		Size: 131.4 MB (131392179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:62912aaadfc996b2e153f528812ceb6a2c074565deb9c97485f51d4d74e40612
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192083470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ee9bc4061ae057ad9a252dd67dd5a8ce7e58ba14becc7b87dfbb80bf812008`
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
# Tue, 04 Aug 2020 09:45:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:0919fec4e424098a16af1cfc29104b97cabaace0158514dd3e83a7d414135fa8`  
		Last Modified: Tue, 04 Aug 2020 09:48:14 GMT  
		Size: 132.0 MB (131959651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

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

### `mono:slim` - linux; amd64

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

### `mono:slim` - linux; arm variant v5

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

### `mono:slim` - linux; arm variant v7

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

### `mono:slim` - linux; arm64 variant v8

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

### `mono:slim` - linux; 386

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

### `mono:slim` - linux; ppc64le

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
