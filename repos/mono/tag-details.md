<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.12`](#mono612)
-	[`mono:6.12-slim`](#mono612-slim)
-	[`mono:6.12.0`](#mono6120)
-	[`mono:6.12.0-slim`](#mono6120-slim)
-	[`mono:6.12.0.107`](#mono6120107)
-	[`mono:6.12.0.107-slim`](#mono6120107-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:eba426636d9d8bf4707eb23fb8570fe5df717a3d20e74627724471da6c3f2f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6` - linux; amd64

```console
$ docker pull mono@sha256:b280392f8c7f9275fde3ea5acc7cf50a83aa87b4d735a9edbcf059cea8fe2dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235971366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1c92835c596dbede0a89460938b2732275d1e045f16abc3a00826b58746908`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:08:32 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec491672336af147d576206fb63447992542dd48c7f0321a7f9bb96526eda`  
		Last Modified: Tue, 28 Sep 2021 08:15:40 GMT  
		Size: 141.4 MB (141441237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:e92e435f06ed1101d11121ab632d14a3ba7d56c5afe00f31996822d8a84db182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775f04ace0147c935056d6c88cf20cf65a9d6a157c52619aff14e69d1920e793`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:10:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6e330faf4ca8e7f4ce5c061f98b25fe3d923ac271cf40485b6d87e3c82d66`  
		Last Modified: Tue, 28 Sep 2021 09:19:16 GMT  
		Size: 140.1 MB (140100783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8caa05c6c17efef1d9372556b5c1de6e74af56539ece5e422538dd8e9aec469
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187688584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf330eb64ec91dda2b4fac41f619ce1ed0772e5cf21bc3dfa45b524799b1239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:19:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb794efb0e6d60270e7db2fb146156adde39ff777c2a080b43cfd1cf22ac08`  
		Last Modified: Fri, 03 Sep 2021 07:26:31 GMT  
		Size: 138.9 MB (138948728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:84e3de223d8a4325ac4f30bf7b857ac411b518e0b9c1feb4386a5fab192edb42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214538053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201aac86326d3de1163f088401b0215a95979f2017689a88f9effdf593c41ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:57:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84ff9adb8612f8b5f3c3f0898d61502bf043f588f5d6cfdd1b9e8e3963cb0ba`  
		Last Modified: Tue, 28 Sep 2021 05:01:11 GMT  
		Size: 156.6 MB (156597146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:6d9ae76a1db4e1bce4613ec15c92a5ff6e56045b5afbb247ce9e8e489e008523
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241755205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088da9c051198fd9c1f2e8d34859c0e111f5a3b0a0872047f58ed3772b4d2ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:31:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd055cd7ecdd8a30a3cf1e588940b2ed7647ec3e65bfe5ae8fe80d09610fff`  
		Last Modified: Tue, 28 Sep 2021 08:35:23 GMT  
		Size: 142.5 MB (142547720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:c93670820c2ad6a8e447f286863c431ad3e6cbc9f1bb805e53d084db08b6dd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203420660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e97c533f5387bb3a62c323592c25608829cd80abd3692b0c6f823c5e71087`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:36:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988aaa676e755a5cd43176983ac0d18a325a38dfed9f09fcce1f1d08044f399`  
		Last Modified: Fri, 03 Sep 2021 08:46:47 GMT  
		Size: 143.3 MB (143250656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:01fd569d63b3682f126390f4153cef90542ea814534148924fca55760c82bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6-slim` - linux; amd64

```console
$ docker pull mono@sha256:b95b956802e20e811d7679e23c19da5ca2176c5f626f19ae66e5b1c90ec32c4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60e409339ab63005aa179be654058616053a358d1570b3cdcdcb75c304657c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f2b607801869b17dcfecca774af452732463bbb1bb54f50180d4d0670117c673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b13fc4e4777077d271e70defb931bda269b7f856a68e164c74a0fbac4a8a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2c2cfd1988c13d32f9b0ad2ceb4d88421a5b877b3f5f86dc99f4dfc6a936c1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59e8321cabd2c937293ef6752fba1bbca466979018d57651dd08e3404ac03e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f3721cf677ee4fe6eeb9c757e7e0bf0faebbfdfe5942c6f515b0cf1e45372425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f450d60fb7b5103dad6aa7b14ae87b78da88df0a7cf341bed22d676b455e95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:17a92d3b707ead6f1ffd7fbfbb386bda7f46f888c07036ee5fe3e79fefb5e97a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99207485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2b71ab8631041a02064dc75c2eddce521e452f50114c2967392a3418944855`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:246b89a98ed402f68e362e5071d08884b53e4a6e66a0594ba58a2f7fcb27764a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e719554a822c0a6e8d0da2a4d9711f875e416cb9993bc0e3adf300c33d822`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:c0342df2c97ebdd7499a8cf15482a3c9863b5bcd13c93e43e03a4ffda5024a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10` - linux; amd64

```console
$ docker pull mono@sha256:5c98a1f94c8a213cade5040b7e74186060cc27008d24b2908fd6d44c8bf92ad6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224847627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807ee4cfa136949c749566cb4dc47f289d750aa7fe8001da54d996bb922a85f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:00:48 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:00:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:01:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:13:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4cb61092b6ef750b6ba82a3bf819fdad8d962d768f6b71ecfd9b3f8ec56aab`  
		Last Modified: Tue, 28 Sep 2021 08:14:57 GMT  
		Size: 256.0 KB (256046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8274a0ef20c3568cfcbc2f33681a8c630dad3b25a0c74d127848eb93f08014`  
		Last Modified: Tue, 28 Sep 2021 08:15:08 GMT  
		Size: 67.1 MB (67148271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d12c5127b2c2e335097b62d2083a629f8f744e436c45ba289c77f5f540fb1`  
		Last Modified: Tue, 28 Sep 2021 08:16:19 GMT  
		Size: 130.3 MB (130297316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:ab609e1b64b6c6ed6112d16adba1b76824e9a04a731baf6fac1ab01a1c0e7c0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180673448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3a7768d6e4aee0c8546af0668cce90a3eeb0652765330312211e7303f1c572`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:12 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 09:04:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:06:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:14:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07be636d58f4cfe8ab60e7a92e212e66f3fe6f15aa2adb9b5326b1f6ea4b0e`  
		Last Modified: Tue, 28 Sep 2021 09:17:02 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffd2d254da31dc4ca4f416844b04226404acd24ecd47b65fc98eec339a9ef6`  
		Last Modified: Tue, 28 Sep 2021 09:17:22 GMT  
		Size: 26.6 MB (26573991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb03448e3957b34f5ea5d42f5925dccc10cd9fecf3b0e5e4e485d0ce4c501147`  
		Last Modified: Tue, 28 Sep 2021 09:21:10 GMT  
		Size: 129.0 MB (128964413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:6329e7833c88016b7ba7b007fc4c1e9698a8d3a8cbf26704c406320ae121184d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176594479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffb757bd919c0535ec760492937c91f4d99d7d48f5ef7510dd4fe45aa4d654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:14:52 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 07:15:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:15:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab9ab5a244291947250c1513d8e0bdd263f76fd88eeb06b4e9bbcc4b629026`  
		Last Modified: Fri, 03 Sep 2021 07:24:20 GMT  
		Size: 255.9 KB (255936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad508abbc934de30932bda7340b7b17e103fa8a1aceac95a82b0582d9a1bec0`  
		Last Modified: Fri, 03 Sep 2021 07:24:38 GMT  
		Size: 25.8 MB (25776669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7c6062075b54536bb118e5b97796f7524367ec70ea583b5dcc9fda196647a4`  
		Last Modified: Fri, 03 Sep 2021 07:28:24 GMT  
		Size: 127.8 MB (127815723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4f144b39c4960a888091560fc0a67c89dd8ffa197ed042b0657b7c7374d00424
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203430536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e124ee3b535f0fe0a9f3be5709b206526689edfb9e03cd78ba249437acaaeaad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:54:13 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 04:54:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9585ab1883b35ade9823353ee2f0b74df2e57d4a03326e2a1bd2d473df0a32`  
		Last Modified: Tue, 28 Sep 2021 05:00:25 GMT  
		Size: 255.9 KB (255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a15546042e0a737c53f6f021a6b3a71ffafc03e2ff1bb645880f9a0a2cd355`  
		Last Modified: Tue, 28 Sep 2021 05:00:31 GMT  
		Size: 31.8 MB (31791240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b8aed687e9e9e005827683e1de285fcf9108775ae8221a9e294838380e9687`  
		Last Modified: Tue, 28 Sep 2021 05:01:57 GMT  
		Size: 145.5 MB (145468350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:3a59a832b25f27b64f4f65e6b24bec72e48cf03a0ebe41f4aba091895bafccf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230645338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6bdde6672f1fe64cbf8f671dfe943c1fc07be48a7cf911468371bbb2c7fffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:29:17 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:29:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:30:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:33:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2aa3cc438586bbe8ff38983ddcd7a6c2c7ff0bfd88ec787db08d42942b9376`  
		Last Modified: Tue, 28 Sep 2021 08:34:22 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e12a248df404d430824291be12af8a7e6e91e7a43cfd7c05f808023d2697c`  
		Last Modified: Tue, 28 Sep 2021 08:34:36 GMT  
		Size: 71.2 MB (71178935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dbcccc4432f7c6fc1e0c5f66a4a24de09777610b77bde73fdbdd223621955b`  
		Last Modified: Tue, 28 Sep 2021 08:36:12 GMT  
		Size: 131.4 MB (131412817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:b4842b4068a2ee0baf90019e3c22ff7c2da3f3ca520a28c420a08627d5bf8ded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192204761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4f0c6100f7b4cf5274e658782327f9ca511b326c74f0ce9151973fa8c6ec85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:26:56 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 08:27:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:29:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:44:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ed5deac1f433a0ffa69afd3fb3c6df5dc1d3a7f6172b99903d967fc8fa52a`  
		Last Modified: Fri, 03 Sep 2021 08:46:00 GMT  
		Size: 256.1 KB (256078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670314a6ebec2a6b5ddadba5cc428d8f5432bdee858ca166f9738839659404d`  
		Last Modified: Fri, 03 Sep 2021 08:46:06 GMT  
		Size: 29.4 MB (29392983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e41e15cff899fcb27f4fe03234f23a4f205c7feebf788248a028253b1c0f7e`  
		Last Modified: Fri, 03 Sep 2021 08:47:33 GMT  
		Size: 132.0 MB (132002025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:867bc43c5ce0937b7e49e5d80a50a311848d8d09274d467045ad60ca7c9861d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10-slim` - linux; amd64

```console
$ docker pull mono@sha256:90fa447053efbb634bbf621f700395faeed20e14869d9f10496d052faad8e7d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94550311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb2bcc5264f14b2fc9e2aba7da2b42b022dbad0ac85ec0a773793a1dcdad92d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:00:48 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:00:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:01:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4cb61092b6ef750b6ba82a3bf819fdad8d962d768f6b71ecfd9b3f8ec56aab`  
		Last Modified: Tue, 28 Sep 2021 08:14:57 GMT  
		Size: 256.0 KB (256046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8274a0ef20c3568cfcbc2f33681a8c630dad3b25a0c74d127848eb93f08014`  
		Last Modified: Tue, 28 Sep 2021 08:15:08 GMT  
		Size: 67.1 MB (67148271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e527e64e3878014d47561c76dd3aea63cbe08efb0cc96eaf9427b903dda9622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9659f2a40bc39d4c1612221e08a36119ff32c1842dbeadb3d33e52d9402809d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:12 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 09:04:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:06:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07be636d58f4cfe8ab60e7a92e212e66f3fe6f15aa2adb9b5326b1f6ea4b0e`  
		Last Modified: Tue, 28 Sep 2021 09:17:02 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffd2d254da31dc4ca4f416844b04226404acd24ecd47b65fc98eec339a9ef6`  
		Last Modified: Tue, 28 Sep 2021 09:17:22 GMT  
		Size: 26.6 MB (26573991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ca4352df1def840bac8a4e9b78605d210279ce99813d9e439dcc1b6c4e754530
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48778756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ecf1571b4640d4df6400b36e43df3d4e535b012148c41a6edcf4660a535128`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:14:52 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 07:15:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:15:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab9ab5a244291947250c1513d8e0bdd263f76fd88eeb06b4e9bbcc4b629026`  
		Last Modified: Fri, 03 Sep 2021 07:24:20 GMT  
		Size: 255.9 KB (255936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad508abbc934de30932bda7340b7b17e103fa8a1aceac95a82b0582d9a1bec0`  
		Last Modified: Fri, 03 Sep 2021 07:24:38 GMT  
		Size: 25.8 MB (25776669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0a94e563853e20024671dfb8def8e196a5458cd68d26a1dcacbad6b6e51217ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57962186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d2529d96c6b6b49160179a0e968b65775f1beadc85e11c26ab11b89363a23e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:54:13 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 04:54:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9585ab1883b35ade9823353ee2f0b74df2e57d4a03326e2a1bd2d473df0a32`  
		Last Modified: Tue, 28 Sep 2021 05:00:25 GMT  
		Size: 255.9 KB (255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a15546042e0a737c53f6f021a6b3a71ffafc03e2ff1bb645880f9a0a2cd355`  
		Last Modified: Tue, 28 Sep 2021 05:00:31 GMT  
		Size: 31.8 MB (31791240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:e95496be54b6a50958dd8173c4e7db3b8cdef775cb9da4057e34b7bef1a44f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99232521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7796700f66ff57bf87bcf9333851f6d7fc8429694d44fef5641b22f600ee35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:29:17 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:29:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:30:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2aa3cc438586bbe8ff38983ddcd7a6c2c7ff0bfd88ec787db08d42942b9376`  
		Last Modified: Tue, 28 Sep 2021 08:34:22 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e12a248df404d430824291be12af8a7e6e91e7a43cfd7c05f808023d2697c`  
		Last Modified: Tue, 28 Sep 2021 08:34:36 GMT  
		Size: 71.2 MB (71178935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:efc9781052bffc1bf83b0dfa96e14c62c28f0e74bcc4d46f656240fd480d9415
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609adaed25545dbf1ceeaf098d8928b21f5f7dc334da4a72f797c799b22faa6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:26:56 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 08:27:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:29:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ed5deac1f433a0ffa69afd3fb3c6df5dc1d3a7f6172b99903d967fc8fa52a`  
		Last Modified: Fri, 03 Sep 2021 08:46:00 GMT  
		Size: 256.1 KB (256078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670314a6ebec2a6b5ddadba5cc428d8f5432bdee858ca166f9738839659404d`  
		Last Modified: Fri, 03 Sep 2021 08:46:06 GMT  
		Size: 29.4 MB (29392983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:c0342df2c97ebdd7499a8cf15482a3c9863b5bcd13c93e43e03a4ffda5024a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0` - linux; amd64

```console
$ docker pull mono@sha256:5c98a1f94c8a213cade5040b7e74186060cc27008d24b2908fd6d44c8bf92ad6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224847627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807ee4cfa136949c749566cb4dc47f289d750aa7fe8001da54d996bb922a85f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:00:48 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:00:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:01:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:13:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4cb61092b6ef750b6ba82a3bf819fdad8d962d768f6b71ecfd9b3f8ec56aab`  
		Last Modified: Tue, 28 Sep 2021 08:14:57 GMT  
		Size: 256.0 KB (256046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8274a0ef20c3568cfcbc2f33681a8c630dad3b25a0c74d127848eb93f08014`  
		Last Modified: Tue, 28 Sep 2021 08:15:08 GMT  
		Size: 67.1 MB (67148271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d12c5127b2c2e335097b62d2083a629f8f744e436c45ba289c77f5f540fb1`  
		Last Modified: Tue, 28 Sep 2021 08:16:19 GMT  
		Size: 130.3 MB (130297316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:ab609e1b64b6c6ed6112d16adba1b76824e9a04a731baf6fac1ab01a1c0e7c0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180673448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3a7768d6e4aee0c8546af0668cce90a3eeb0652765330312211e7303f1c572`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:12 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 09:04:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:06:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:14:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07be636d58f4cfe8ab60e7a92e212e66f3fe6f15aa2adb9b5326b1f6ea4b0e`  
		Last Modified: Tue, 28 Sep 2021 09:17:02 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffd2d254da31dc4ca4f416844b04226404acd24ecd47b65fc98eec339a9ef6`  
		Last Modified: Tue, 28 Sep 2021 09:17:22 GMT  
		Size: 26.6 MB (26573991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb03448e3957b34f5ea5d42f5925dccc10cd9fecf3b0e5e4e485d0ce4c501147`  
		Last Modified: Tue, 28 Sep 2021 09:21:10 GMT  
		Size: 129.0 MB (128964413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:6329e7833c88016b7ba7b007fc4c1e9698a8d3a8cbf26704c406320ae121184d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176594479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffb757bd919c0535ec760492937c91f4d99d7d48f5ef7510dd4fe45aa4d654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:14:52 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 07:15:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:15:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab9ab5a244291947250c1513d8e0bdd263f76fd88eeb06b4e9bbcc4b629026`  
		Last Modified: Fri, 03 Sep 2021 07:24:20 GMT  
		Size: 255.9 KB (255936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad508abbc934de30932bda7340b7b17e103fa8a1aceac95a82b0582d9a1bec0`  
		Last Modified: Fri, 03 Sep 2021 07:24:38 GMT  
		Size: 25.8 MB (25776669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7c6062075b54536bb118e5b97796f7524367ec70ea583b5dcc9fda196647a4`  
		Last Modified: Fri, 03 Sep 2021 07:28:24 GMT  
		Size: 127.8 MB (127815723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4f144b39c4960a888091560fc0a67c89dd8ffa197ed042b0657b7c7374d00424
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203430536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e124ee3b535f0fe0a9f3be5709b206526689edfb9e03cd78ba249437acaaeaad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:54:13 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 04:54:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9585ab1883b35ade9823353ee2f0b74df2e57d4a03326e2a1bd2d473df0a32`  
		Last Modified: Tue, 28 Sep 2021 05:00:25 GMT  
		Size: 255.9 KB (255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a15546042e0a737c53f6f021a6b3a71ffafc03e2ff1bb645880f9a0a2cd355`  
		Last Modified: Tue, 28 Sep 2021 05:00:31 GMT  
		Size: 31.8 MB (31791240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b8aed687e9e9e005827683e1de285fcf9108775ae8221a9e294838380e9687`  
		Last Modified: Tue, 28 Sep 2021 05:01:57 GMT  
		Size: 145.5 MB (145468350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:3a59a832b25f27b64f4f65e6b24bec72e48cf03a0ebe41f4aba091895bafccf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230645338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6bdde6672f1fe64cbf8f671dfe943c1fc07be48a7cf911468371bbb2c7fffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:29:17 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:29:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:30:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:33:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2aa3cc438586bbe8ff38983ddcd7a6c2c7ff0bfd88ec787db08d42942b9376`  
		Last Modified: Tue, 28 Sep 2021 08:34:22 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e12a248df404d430824291be12af8a7e6e91e7a43cfd7c05f808023d2697c`  
		Last Modified: Tue, 28 Sep 2021 08:34:36 GMT  
		Size: 71.2 MB (71178935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dbcccc4432f7c6fc1e0c5f66a4a24de09777610b77bde73fdbdd223621955b`  
		Last Modified: Tue, 28 Sep 2021 08:36:12 GMT  
		Size: 131.4 MB (131412817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:b4842b4068a2ee0baf90019e3c22ff7c2da3f3ca520a28c420a08627d5bf8ded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192204761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4f0c6100f7b4cf5274e658782327f9ca511b326c74f0ce9151973fa8c6ec85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:26:56 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 08:27:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:29:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:44:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ed5deac1f433a0ffa69afd3fb3c6df5dc1d3a7f6172b99903d967fc8fa52a`  
		Last Modified: Fri, 03 Sep 2021 08:46:00 GMT  
		Size: 256.1 KB (256078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670314a6ebec2a6b5ddadba5cc428d8f5432bdee858ca166f9738839659404d`  
		Last Modified: Fri, 03 Sep 2021 08:46:06 GMT  
		Size: 29.4 MB (29392983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e41e15cff899fcb27f4fe03234f23a4f205c7feebf788248a028253b1c0f7e`  
		Last Modified: Fri, 03 Sep 2021 08:47:33 GMT  
		Size: 132.0 MB (132002025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:867bc43c5ce0937b7e49e5d80a50a311848d8d09274d467045ad60ca7c9861d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:90fa447053efbb634bbf621f700395faeed20e14869d9f10496d052faad8e7d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94550311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb2bcc5264f14b2fc9e2aba7da2b42b022dbad0ac85ec0a773793a1dcdad92d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:00:48 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:00:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:01:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4cb61092b6ef750b6ba82a3bf819fdad8d962d768f6b71ecfd9b3f8ec56aab`  
		Last Modified: Tue, 28 Sep 2021 08:14:57 GMT  
		Size: 256.0 KB (256046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8274a0ef20c3568cfcbc2f33681a8c630dad3b25a0c74d127848eb93f08014`  
		Last Modified: Tue, 28 Sep 2021 08:15:08 GMT  
		Size: 67.1 MB (67148271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e527e64e3878014d47561c76dd3aea63cbe08efb0cc96eaf9427b903dda9622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9659f2a40bc39d4c1612221e08a36119ff32c1842dbeadb3d33e52d9402809d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:12 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 09:04:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:06:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07be636d58f4cfe8ab60e7a92e212e66f3fe6f15aa2adb9b5326b1f6ea4b0e`  
		Last Modified: Tue, 28 Sep 2021 09:17:02 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffd2d254da31dc4ca4f416844b04226404acd24ecd47b65fc98eec339a9ef6`  
		Last Modified: Tue, 28 Sep 2021 09:17:22 GMT  
		Size: 26.6 MB (26573991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ca4352df1def840bac8a4e9b78605d210279ce99813d9e439dcc1b6c4e754530
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48778756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ecf1571b4640d4df6400b36e43df3d4e535b012148c41a6edcf4660a535128`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:14:52 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 07:15:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:15:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab9ab5a244291947250c1513d8e0bdd263f76fd88eeb06b4e9bbcc4b629026`  
		Last Modified: Fri, 03 Sep 2021 07:24:20 GMT  
		Size: 255.9 KB (255936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad508abbc934de30932bda7340b7b17e103fa8a1aceac95a82b0582d9a1bec0`  
		Last Modified: Fri, 03 Sep 2021 07:24:38 GMT  
		Size: 25.8 MB (25776669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0a94e563853e20024671dfb8def8e196a5458cd68d26a1dcacbad6b6e51217ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57962186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d2529d96c6b6b49160179a0e968b65775f1beadc85e11c26ab11b89363a23e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:54:13 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 04:54:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9585ab1883b35ade9823353ee2f0b74df2e57d4a03326e2a1bd2d473df0a32`  
		Last Modified: Tue, 28 Sep 2021 05:00:25 GMT  
		Size: 255.9 KB (255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a15546042e0a737c53f6f021a6b3a71ffafc03e2ff1bb645880f9a0a2cd355`  
		Last Modified: Tue, 28 Sep 2021 05:00:31 GMT  
		Size: 31.8 MB (31791240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:e95496be54b6a50958dd8173c4e7db3b8cdef775cb9da4057e34b7bef1a44f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99232521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7796700f66ff57bf87bcf9333851f6d7fc8429694d44fef5641b22f600ee35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:29:17 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:29:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:30:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2aa3cc438586bbe8ff38983ddcd7a6c2c7ff0bfd88ec787db08d42942b9376`  
		Last Modified: Tue, 28 Sep 2021 08:34:22 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e12a248df404d430824291be12af8a7e6e91e7a43cfd7c05f808023d2697c`  
		Last Modified: Tue, 28 Sep 2021 08:34:36 GMT  
		Size: 71.2 MB (71178935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:efc9781052bffc1bf83b0dfa96e14c62c28f0e74bcc4d46f656240fd480d9415
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609adaed25545dbf1ceeaf098d8928b21f5f7dc334da4a72f797c799b22faa6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:26:56 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 08:27:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:29:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ed5deac1f433a0ffa69afd3fb3c6df5dc1d3a7f6172b99903d967fc8fa52a`  
		Last Modified: Fri, 03 Sep 2021 08:46:00 GMT  
		Size: 256.1 KB (256078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670314a6ebec2a6b5ddadba5cc428d8f5432bdee858ca166f9738839659404d`  
		Last Modified: Fri, 03 Sep 2021 08:46:06 GMT  
		Size: 29.4 MB (29392983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:c0342df2c97ebdd7499a8cf15482a3c9863b5bcd13c93e43e03a4ffda5024a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104` - linux; amd64

```console
$ docker pull mono@sha256:5c98a1f94c8a213cade5040b7e74186060cc27008d24b2908fd6d44c8bf92ad6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224847627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807ee4cfa136949c749566cb4dc47f289d750aa7fe8001da54d996bb922a85f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:00:48 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:00:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:01:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:13:53 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4cb61092b6ef750b6ba82a3bf819fdad8d962d768f6b71ecfd9b3f8ec56aab`  
		Last Modified: Tue, 28 Sep 2021 08:14:57 GMT  
		Size: 256.0 KB (256046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8274a0ef20c3568cfcbc2f33681a8c630dad3b25a0c74d127848eb93f08014`  
		Last Modified: Tue, 28 Sep 2021 08:15:08 GMT  
		Size: 67.1 MB (67148271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d12c5127b2c2e335097b62d2083a629f8f744e436c45ba289c77f5f540fb1`  
		Last Modified: Tue, 28 Sep 2021 08:16:19 GMT  
		Size: 130.3 MB (130297316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:ab609e1b64b6c6ed6112d16adba1b76824e9a04a731baf6fac1ab01a1c0e7c0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180673448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3a7768d6e4aee0c8546af0668cce90a3eeb0652765330312211e7303f1c572`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:12 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 09:04:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:06:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:14:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07be636d58f4cfe8ab60e7a92e212e66f3fe6f15aa2adb9b5326b1f6ea4b0e`  
		Last Modified: Tue, 28 Sep 2021 09:17:02 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffd2d254da31dc4ca4f416844b04226404acd24ecd47b65fc98eec339a9ef6`  
		Last Modified: Tue, 28 Sep 2021 09:17:22 GMT  
		Size: 26.6 MB (26573991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb03448e3957b34f5ea5d42f5925dccc10cd9fecf3b0e5e4e485d0ce4c501147`  
		Last Modified: Tue, 28 Sep 2021 09:21:10 GMT  
		Size: 129.0 MB (128964413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:6329e7833c88016b7ba7b007fc4c1e9698a8d3a8cbf26704c406320ae121184d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176594479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffb757bd919c0535ec760492937c91f4d99d7d48f5ef7510dd4fe45aa4d654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:14:52 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 07:15:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:15:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:22:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab9ab5a244291947250c1513d8e0bdd263f76fd88eeb06b4e9bbcc4b629026`  
		Last Modified: Fri, 03 Sep 2021 07:24:20 GMT  
		Size: 255.9 KB (255936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad508abbc934de30932bda7340b7b17e103fa8a1aceac95a82b0582d9a1bec0`  
		Last Modified: Fri, 03 Sep 2021 07:24:38 GMT  
		Size: 25.8 MB (25776669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7c6062075b54536bb118e5b97796f7524367ec70ea583b5dcc9fda196647a4`  
		Last Modified: Fri, 03 Sep 2021 07:28:24 GMT  
		Size: 127.8 MB (127815723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4f144b39c4960a888091560fc0a67c89dd8ffa197ed042b0657b7c7374d00424
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203430536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e124ee3b535f0fe0a9f3be5709b206526689edfb9e03cd78ba249437acaaeaad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:54:13 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 04:54:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:59:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9585ab1883b35ade9823353ee2f0b74df2e57d4a03326e2a1bd2d473df0a32`  
		Last Modified: Tue, 28 Sep 2021 05:00:25 GMT  
		Size: 255.9 KB (255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a15546042e0a737c53f6f021a6b3a71ffafc03e2ff1bb645880f9a0a2cd355`  
		Last Modified: Tue, 28 Sep 2021 05:00:31 GMT  
		Size: 31.8 MB (31791240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b8aed687e9e9e005827683e1de285fcf9108775ae8221a9e294838380e9687`  
		Last Modified: Tue, 28 Sep 2021 05:01:57 GMT  
		Size: 145.5 MB (145468350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:3a59a832b25f27b64f4f65e6b24bec72e48cf03a0ebe41f4aba091895bafccf7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230645338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6bdde6672f1fe64cbf8f671dfe943c1fc07be48a7cf911468371bbb2c7fffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:29:17 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:29:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:30:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:33:04 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2aa3cc438586bbe8ff38983ddcd7a6c2c7ff0bfd88ec787db08d42942b9376`  
		Last Modified: Tue, 28 Sep 2021 08:34:22 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e12a248df404d430824291be12af8a7e6e91e7a43cfd7c05f808023d2697c`  
		Last Modified: Tue, 28 Sep 2021 08:34:36 GMT  
		Size: 71.2 MB (71178935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dbcccc4432f7c6fc1e0c5f66a4a24de09777610b77bde73fdbdd223621955b`  
		Last Modified: Tue, 28 Sep 2021 08:36:12 GMT  
		Size: 131.4 MB (131412817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:b4842b4068a2ee0baf90019e3c22ff7c2da3f3ca520a28c420a08627d5bf8ded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192204761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4f0c6100f7b4cf5274e658782327f9ca511b326c74f0ce9151973fa8c6ec85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:26:56 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 08:27:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:29:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:44:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ed5deac1f433a0ffa69afd3fb3c6df5dc1d3a7f6172b99903d967fc8fa52a`  
		Last Modified: Fri, 03 Sep 2021 08:46:00 GMT  
		Size: 256.1 KB (256078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670314a6ebec2a6b5ddadba5cc428d8f5432bdee858ca166f9738839659404d`  
		Last Modified: Fri, 03 Sep 2021 08:46:06 GMT  
		Size: 29.4 MB (29392983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e41e15cff899fcb27f4fe03234f23a4f205c7feebf788248a028253b1c0f7e`  
		Last Modified: Fri, 03 Sep 2021 08:47:33 GMT  
		Size: 132.0 MB (132002025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:867bc43c5ce0937b7e49e5d80a50a311848d8d09274d467045ad60ca7c9861d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.10.0.104-slim` - linux; amd64

```console
$ docker pull mono@sha256:90fa447053efbb634bbf621f700395faeed20e14869d9f10496d052faad8e7d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94550311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb2bcc5264f14b2fc9e2aba7da2b42b022dbad0ac85ec0a773793a1dcdad92d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:00:48 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:00:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:01:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4cb61092b6ef750b6ba82a3bf819fdad8d962d768f6b71ecfd9b3f8ec56aab`  
		Last Modified: Tue, 28 Sep 2021 08:14:57 GMT  
		Size: 256.0 KB (256046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8274a0ef20c3568cfcbc2f33681a8c630dad3b25a0c74d127848eb93f08014`  
		Last Modified: Tue, 28 Sep 2021 08:15:08 GMT  
		Size: 67.1 MB (67148271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:e527e64e3878014d47561c76dd3aea63cbe08efb0cc96eaf9427b903dda9622d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9659f2a40bc39d4c1612221e08a36119ff32c1842dbeadb3d33e52d9402809d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:12 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 09:04:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:06:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac07be636d58f4cfe8ab60e7a92e212e66f3fe6f15aa2adb9b5326b1f6ea4b0e`  
		Last Modified: Tue, 28 Sep 2021 09:17:02 GMT  
		Size: 256.0 KB (255977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffd2d254da31dc4ca4f416844b04226404acd24ecd47b65fc98eec339a9ef6`  
		Last Modified: Tue, 28 Sep 2021 09:17:22 GMT  
		Size: 26.6 MB (26573991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:ca4352df1def840bac8a4e9b78605d210279ce99813d9e439dcc1b6c4e754530
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48778756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ecf1571b4640d4df6400b36e43df3d4e535b012148c41a6edcf4660a535128`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:14:52 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 07:15:09 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:15:59 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab9ab5a244291947250c1513d8e0bdd263f76fd88eeb06b4e9bbcc4b629026`  
		Last Modified: Fri, 03 Sep 2021 07:24:20 GMT  
		Size: 255.9 KB (255936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad508abbc934de30932bda7340b7b17e103fa8a1aceac95a82b0582d9a1bec0`  
		Last Modified: Fri, 03 Sep 2021 07:24:38 GMT  
		Size: 25.8 MB (25776669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0a94e563853e20024671dfb8def8e196a5458cd68d26a1dcacbad6b6e51217ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57962186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d2529d96c6b6b49160179a0e968b65775f1beadc85e11c26ab11b89363a23e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:54:13 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 04:54:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9585ab1883b35ade9823353ee2f0b74df2e57d4a03326e2a1bd2d473df0a32`  
		Last Modified: Tue, 28 Sep 2021 05:00:25 GMT  
		Size: 255.9 KB (255907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a15546042e0a737c53f6f021a6b3a71ffafc03e2ff1bb645880f9a0a2cd355`  
		Last Modified: Tue, 28 Sep 2021 05:00:31 GMT  
		Size: 31.8 MB (31791240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:e95496be54b6a50958dd8173c4e7db3b8cdef775cb9da4057e34b7bef1a44f47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99232521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7796700f66ff57bf87bcf9333851f6d7fc8429694d44fef5641b22f600ee35`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:29:17 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 28 Sep 2021 08:29:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:30:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2aa3cc438586bbe8ff38983ddcd7a6c2c7ff0bfd88ec787db08d42942b9376`  
		Last Modified: Tue, 28 Sep 2021 08:34:22 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9e12a248df404d430824291be12af8a7e6e91e7a43cfd7c05f808023d2697c`  
		Last Modified: Tue, 28 Sep 2021 08:34:36 GMT  
		Size: 71.2 MB (71178935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:efc9781052bffc1bf83b0dfa96e14c62c28f0e74bcc4d46f656240fd480d9415
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609adaed25545dbf1ceeaf098d8928b21f5f7dc334da4a72f797c799b22faa6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:26:56 GMT
ENV MONO_VERSION=6.10.0.104
# Fri, 03 Sep 2021 08:27:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:29:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ed5deac1f433a0ffa69afd3fb3c6df5dc1d3a7f6172b99903d967fc8fa52a`  
		Last Modified: Fri, 03 Sep 2021 08:46:00 GMT  
		Size: 256.1 KB (256078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670314a6ebec2a6b5ddadba5cc428d8f5432bdee858ca166f9738839659404d`  
		Last Modified: Fri, 03 Sep 2021 08:46:06 GMT  
		Size: 29.4 MB (29392983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:eba426636d9d8bf4707eb23fb8570fe5df717a3d20e74627724471da6c3f2f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:b280392f8c7f9275fde3ea5acc7cf50a83aa87b4d735a9edbcf059cea8fe2dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235971366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1c92835c596dbede0a89460938b2732275d1e045f16abc3a00826b58746908`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:08:32 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec491672336af147d576206fb63447992542dd48c7f0321a7f9bb96526eda`  
		Last Modified: Tue, 28 Sep 2021 08:15:40 GMT  
		Size: 141.4 MB (141441237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:e92e435f06ed1101d11121ab632d14a3ba7d56c5afe00f31996822d8a84db182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775f04ace0147c935056d6c88cf20cf65a9d6a157c52619aff14e69d1920e793`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:10:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6e330faf4ca8e7f4ce5c061f98b25fe3d923ac271cf40485b6d87e3c82d66`  
		Last Modified: Tue, 28 Sep 2021 09:19:16 GMT  
		Size: 140.1 MB (140100783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8caa05c6c17efef1d9372556b5c1de6e74af56539ece5e422538dd8e9aec469
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187688584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf330eb64ec91dda2b4fac41f619ce1ed0772e5cf21bc3dfa45b524799b1239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:19:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb794efb0e6d60270e7db2fb146156adde39ff777c2a080b43cfd1cf22ac08`  
		Last Modified: Fri, 03 Sep 2021 07:26:31 GMT  
		Size: 138.9 MB (138948728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:84e3de223d8a4325ac4f30bf7b857ac411b518e0b9c1feb4386a5fab192edb42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214538053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201aac86326d3de1163f088401b0215a95979f2017689a88f9effdf593c41ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:57:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84ff9adb8612f8b5f3c3f0898d61502bf043f588f5d6cfdd1b9e8e3963cb0ba`  
		Last Modified: Tue, 28 Sep 2021 05:01:11 GMT  
		Size: 156.6 MB (156597146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:6d9ae76a1db4e1bce4613ec15c92a5ff6e56045b5afbb247ce9e8e489e008523
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241755205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088da9c051198fd9c1f2e8d34859c0e111f5a3b0a0872047f58ed3772b4d2ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:31:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd055cd7ecdd8a30a3cf1e588940b2ed7647ec3e65bfe5ae8fe80d09610fff`  
		Last Modified: Tue, 28 Sep 2021 08:35:23 GMT  
		Size: 142.5 MB (142547720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:c93670820c2ad6a8e447f286863c431ad3e6cbc9f1bb805e53d084db08b6dd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203420660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e97c533f5387bb3a62c323592c25608829cd80abd3692b0c6f823c5e71087`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:36:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988aaa676e755a5cd43176983ac0d18a325a38dfed9f09fcce1f1d08044f399`  
		Last Modified: Fri, 03 Sep 2021 08:46:47 GMT  
		Size: 143.3 MB (143250656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:01fd569d63b3682f126390f4153cef90542ea814534148924fca55760c82bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:b95b956802e20e811d7679e23c19da5ca2176c5f626f19ae66e5b1c90ec32c4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60e409339ab63005aa179be654058616053a358d1570b3cdcdcb75c304657c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f2b607801869b17dcfecca774af452732463bbb1bb54f50180d4d0670117c673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b13fc4e4777077d271e70defb931bda269b7f856a68e164c74a0fbac4a8a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2c2cfd1988c13d32f9b0ad2ceb4d88421a5b877b3f5f86dc99f4dfc6a936c1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59e8321cabd2c937293ef6752fba1bbca466979018d57651dd08e3404ac03e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f3721cf677ee4fe6eeb9c757e7e0bf0faebbfdfe5942c6f515b0cf1e45372425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f450d60fb7b5103dad6aa7b14ae87b78da88df0a7cf341bed22d676b455e95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:17a92d3b707ead6f1ffd7fbfbb386bda7f46f888c07036ee5fe3e79fefb5e97a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99207485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2b71ab8631041a02064dc75c2eddce521e452f50114c2967392a3418944855`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:246b89a98ed402f68e362e5071d08884b53e4a6e66a0594ba58a2f7fcb27764a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e719554a822c0a6e8d0da2a4d9711f875e416cb9993bc0e3adf300c33d822`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:eba426636d9d8bf4707eb23fb8570fe5df717a3d20e74627724471da6c3f2f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:b280392f8c7f9275fde3ea5acc7cf50a83aa87b4d735a9edbcf059cea8fe2dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235971366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1c92835c596dbede0a89460938b2732275d1e045f16abc3a00826b58746908`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:08:32 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec491672336af147d576206fb63447992542dd48c7f0321a7f9bb96526eda`  
		Last Modified: Tue, 28 Sep 2021 08:15:40 GMT  
		Size: 141.4 MB (141441237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:e92e435f06ed1101d11121ab632d14a3ba7d56c5afe00f31996822d8a84db182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775f04ace0147c935056d6c88cf20cf65a9d6a157c52619aff14e69d1920e793`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:10:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6e330faf4ca8e7f4ce5c061f98b25fe3d923ac271cf40485b6d87e3c82d66`  
		Last Modified: Tue, 28 Sep 2021 09:19:16 GMT  
		Size: 140.1 MB (140100783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8caa05c6c17efef1d9372556b5c1de6e74af56539ece5e422538dd8e9aec469
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187688584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf330eb64ec91dda2b4fac41f619ce1ed0772e5cf21bc3dfa45b524799b1239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:19:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb794efb0e6d60270e7db2fb146156adde39ff777c2a080b43cfd1cf22ac08`  
		Last Modified: Fri, 03 Sep 2021 07:26:31 GMT  
		Size: 138.9 MB (138948728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:84e3de223d8a4325ac4f30bf7b857ac411b518e0b9c1feb4386a5fab192edb42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214538053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201aac86326d3de1163f088401b0215a95979f2017689a88f9effdf593c41ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:57:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84ff9adb8612f8b5f3c3f0898d61502bf043f588f5d6cfdd1b9e8e3963cb0ba`  
		Last Modified: Tue, 28 Sep 2021 05:01:11 GMT  
		Size: 156.6 MB (156597146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:6d9ae76a1db4e1bce4613ec15c92a5ff6e56045b5afbb247ce9e8e489e008523
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241755205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088da9c051198fd9c1f2e8d34859c0e111f5a3b0a0872047f58ed3772b4d2ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:31:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd055cd7ecdd8a30a3cf1e588940b2ed7647ec3e65bfe5ae8fe80d09610fff`  
		Last Modified: Tue, 28 Sep 2021 08:35:23 GMT  
		Size: 142.5 MB (142547720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:c93670820c2ad6a8e447f286863c431ad3e6cbc9f1bb805e53d084db08b6dd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203420660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e97c533f5387bb3a62c323592c25608829cd80abd3692b0c6f823c5e71087`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:36:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988aaa676e755a5cd43176983ac0d18a325a38dfed9f09fcce1f1d08044f399`  
		Last Modified: Fri, 03 Sep 2021 08:46:47 GMT  
		Size: 143.3 MB (143250656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:01fd569d63b3682f126390f4153cef90542ea814534148924fca55760c82bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:b95b956802e20e811d7679e23c19da5ca2176c5f626f19ae66e5b1c90ec32c4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60e409339ab63005aa179be654058616053a358d1570b3cdcdcb75c304657c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f2b607801869b17dcfecca774af452732463bbb1bb54f50180d4d0670117c673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b13fc4e4777077d271e70defb931bda269b7f856a68e164c74a0fbac4a8a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2c2cfd1988c13d32f9b0ad2ceb4d88421a5b877b3f5f86dc99f4dfc6a936c1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59e8321cabd2c937293ef6752fba1bbca466979018d57651dd08e3404ac03e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f3721cf677ee4fe6eeb9c757e7e0bf0faebbfdfe5942c6f515b0cf1e45372425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f450d60fb7b5103dad6aa7b14ae87b78da88df0a7cf341bed22d676b455e95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:17a92d3b707ead6f1ffd7fbfbb386bda7f46f888c07036ee5fe3e79fefb5e97a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99207485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2b71ab8631041a02064dc75c2eddce521e452f50114c2967392a3418944855`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:246b89a98ed402f68e362e5071d08884b53e4a6e66a0594ba58a2f7fcb27764a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e719554a822c0a6e8d0da2a4d9711f875e416cb9993bc0e3adf300c33d822`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107`

```console
$ docker pull mono@sha256:eba426636d9d8bf4707eb23fb8570fe5df717a3d20e74627724471da6c3f2f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107` - linux; amd64

```console
$ docker pull mono@sha256:b280392f8c7f9275fde3ea5acc7cf50a83aa87b4d735a9edbcf059cea8fe2dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235971366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1c92835c596dbede0a89460938b2732275d1e045f16abc3a00826b58746908`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:08:32 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec491672336af147d576206fb63447992542dd48c7f0321a7f9bb96526eda`  
		Last Modified: Tue, 28 Sep 2021 08:15:40 GMT  
		Size: 141.4 MB (141441237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v5

```console
$ docker pull mono@sha256:e92e435f06ed1101d11121ab632d14a3ba7d56c5afe00f31996822d8a84db182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775f04ace0147c935056d6c88cf20cf65a9d6a157c52619aff14e69d1920e793`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:10:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6e330faf4ca8e7f4ce5c061f98b25fe3d923ac271cf40485b6d87e3c82d66`  
		Last Modified: Tue, 28 Sep 2021 09:19:16 GMT  
		Size: 140.1 MB (140100783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8caa05c6c17efef1d9372556b5c1de6e74af56539ece5e422538dd8e9aec469
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187688584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf330eb64ec91dda2b4fac41f619ce1ed0772e5cf21bc3dfa45b524799b1239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:19:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb794efb0e6d60270e7db2fb146156adde39ff777c2a080b43cfd1cf22ac08`  
		Last Modified: Fri, 03 Sep 2021 07:26:31 GMT  
		Size: 138.9 MB (138948728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:84e3de223d8a4325ac4f30bf7b857ac411b518e0b9c1feb4386a5fab192edb42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214538053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201aac86326d3de1163f088401b0215a95979f2017689a88f9effdf593c41ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:57:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84ff9adb8612f8b5f3c3f0898d61502bf043f588f5d6cfdd1b9e8e3963cb0ba`  
		Last Modified: Tue, 28 Sep 2021 05:01:11 GMT  
		Size: 156.6 MB (156597146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; 386

```console
$ docker pull mono@sha256:6d9ae76a1db4e1bce4613ec15c92a5ff6e56045b5afbb247ce9e8e489e008523
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241755205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088da9c051198fd9c1f2e8d34859c0e111f5a3b0a0872047f58ed3772b4d2ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:31:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd055cd7ecdd8a30a3cf1e588940b2ed7647ec3e65bfe5ae8fe80d09610fff`  
		Last Modified: Tue, 28 Sep 2021 08:35:23 GMT  
		Size: 142.5 MB (142547720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; ppc64le

```console
$ docker pull mono@sha256:c93670820c2ad6a8e447f286863c431ad3e6cbc9f1bb805e53d084db08b6dd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203420660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e97c533f5387bb3a62c323592c25608829cd80abd3692b0c6f823c5e71087`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:36:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988aaa676e755a5cd43176983ac0d18a325a38dfed9f09fcce1f1d08044f399`  
		Last Modified: Fri, 03 Sep 2021 08:46:47 GMT  
		Size: 143.3 MB (143250656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107-slim`

```console
$ docker pull mono@sha256:01fd569d63b3682f126390f4153cef90542ea814534148924fca55760c82bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107-slim` - linux; amd64

```console
$ docker pull mono@sha256:b95b956802e20e811d7679e23c19da5ca2176c5f626f19ae66e5b1c90ec32c4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60e409339ab63005aa179be654058616053a358d1570b3cdcdcb75c304657c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f2b607801869b17dcfecca774af452732463bbb1bb54f50180d4d0670117c673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b13fc4e4777077d271e70defb931bda269b7f856a68e164c74a0fbac4a8a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2c2cfd1988c13d32f9b0ad2ceb4d88421a5b877b3f5f86dc99f4dfc6a936c1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59e8321cabd2c937293ef6752fba1bbca466979018d57651dd08e3404ac03e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f3721cf677ee4fe6eeb9c757e7e0bf0faebbfdfe5942c6f515b0cf1e45372425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f450d60fb7b5103dad6aa7b14ae87b78da88df0a7cf341bed22d676b455e95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; 386

```console
$ docker pull mono@sha256:17a92d3b707ead6f1ffd7fbfbb386bda7f46f888c07036ee5fe3e79fefb5e97a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99207485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2b71ab8631041a02064dc75c2eddce521e452f50114c2967392a3418944855`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:246b89a98ed402f68e362e5071d08884b53e4a6e66a0594ba58a2f7fcb27764a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e719554a822c0a6e8d0da2a4d9711f875e416cb9993bc0e3adf300c33d822`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:eba426636d9d8bf4707eb23fb8570fe5df717a3d20e74627724471da6c3f2f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:b280392f8c7f9275fde3ea5acc7cf50a83aa87b4d735a9edbcf059cea8fe2dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235971366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1c92835c596dbede0a89460938b2732275d1e045f16abc3a00826b58746908`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:08:32 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ec491672336af147d576206fb63447992542dd48c7f0321a7f9bb96526eda`  
		Last Modified: Tue, 28 Sep 2021 08:15:40 GMT  
		Size: 141.4 MB (141441237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:e92e435f06ed1101d11121ab632d14a3ba7d56c5afe00f31996822d8a84db182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775f04ace0147c935056d6c88cf20cf65a9d6a157c52619aff14e69d1920e793`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 09:10:13 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6e330faf4ca8e7f4ce5c061f98b25fe3d923ac271cf40485b6d87e3c82d66`  
		Last Modified: Tue, 28 Sep 2021 09:19:16 GMT  
		Size: 140.1 MB (140100783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:c8caa05c6c17efef1d9372556b5c1de6e74af56539ece5e422538dd8e9aec469
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187688584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf330eb64ec91dda2b4fac41f619ce1ed0772e5cf21bc3dfa45b524799b1239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 07:19:05 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fb794efb0e6d60270e7db2fb146156adde39ff777c2a080b43cfd1cf22ac08`  
		Last Modified: Fri, 03 Sep 2021 07:26:31 GMT  
		Size: 138.9 MB (138948728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:84e3de223d8a4325ac4f30bf7b857ac411b518e0b9c1feb4386a5fab192edb42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214538053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201aac86326d3de1163f088401b0215a95979f2017689a88f9effdf593c41ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 04:57:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84ff9adb8612f8b5f3c3f0898d61502bf043f588f5d6cfdd1b9e8e3963cb0ba`  
		Last Modified: Tue, 28 Sep 2021 05:01:11 GMT  
		Size: 156.6 MB (156597146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:6d9ae76a1db4e1bce4613ec15c92a5ff6e56045b5afbb247ce9e8e489e008523
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241755205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1088da9c051198fd9c1f2e8d34859c0e111f5a3b0a0872047f58ed3772b4d2ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 28 Sep 2021 08:31:34 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afd055cd7ecdd8a30a3cf1e588940b2ed7647ec3e65bfe5ae8fe80d09610fff`  
		Last Modified: Tue, 28 Sep 2021 08:35:23 GMT  
		Size: 142.5 MB (142547720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:c93670820c2ad6a8e447f286863c431ad3e6cbc9f1bb805e53d084db08b6dd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203420660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334e97c533f5387bb3a62c323592c25608829cd80abd3692b0c6f823c5e71087`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Fri, 03 Sep 2021 08:36:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988aaa676e755a5cd43176983ac0d18a325a38dfed9f09fcce1f1d08044f399`  
		Last Modified: Fri, 03 Sep 2021 08:46:47 GMT  
		Size: 143.3 MB (143250656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:01fd569d63b3682f126390f4153cef90542ea814534148924fca55760c82bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:b95b956802e20e811d7679e23c19da5ca2176c5f626f19ae66e5b1c90ec32c4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60e409339ab63005aa179be654058616053a358d1570b3cdcdcb75c304657c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:59:06 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 07:59:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:00:39 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea8795680905be9f91cdc74f10ed87ceb69cec1c77c6ae0518dcd1aa1e3347`  
		Last Modified: Tue, 28 Sep 2021 08:14:27 GMT  
		Size: 256.0 KB (256040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d9dfc5f833638009d440a829ddcbed8e30689e1e2387a25d1bd2faa39eec2`  
		Last Modified: Tue, 28 Sep 2021 08:14:40 GMT  
		Size: 67.1 MB (67128095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:f2b607801869b17dcfecca774af452732463bbb1bb54f50180d4d0670117c673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b13fc4e4777077d271e70defb931bda269b7f856a68e164c74a0fbac4a8a72f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:51:42 GMT
ADD file:6524935705c59a0eda67f61fe1005a28b4b388258e2d5636dd5b831333200dc8 in / 
# Tue, 28 Sep 2021 01:51:43 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:01:54 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 09:02:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 09:03:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:85d14771cf32dc23d1c8e99a9aad844b3db9d67f4781455c81749ffe43b05513`  
		Last Modified: Tue, 28 Sep 2021 02:08:05 GMT  
		Size: 24.9 MB (24879067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eeae9124c81ef776c99ace88727acbe2cafac499164230ea53dd2e44030beb`  
		Last Modified: Tue, 28 Sep 2021 09:16:19 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcb1c2ef03e8176fcb8b66f6146ec8585b86fd2b24ba7a09f8c72f0dd9f562`  
		Last Modified: Tue, 28 Sep 2021 09:16:38 GMT  
		Size: 26.6 MB (26551304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2c2cfd1988c13d32f9b0ad2ceb4d88421a5b877b3f5f86dc99f4dfc6a936c1a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59e8321cabd2c937293ef6752fba1bbca466979018d57651dd08e3404ac03e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:00:40 GMT
ADD file:4754bbccf4c59f77dd54f3888871f0635a2f9655cda53f50e63237f1580286e0 in / 
# Fri, 03 Sep 2021 01:00:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:13:29 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 07:13:48 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 07:14:37 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2215ad7863d95c38f1f794f1d5b4d6c5ca4ca7e921e4bb7218b803f7ed270675`  
		Last Modified: Fri, 03 Sep 2021 01:16:23 GMT  
		Size: 22.7 MB (22746151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa844351522fac27215e39f522d477371158e68add695f3fa0d3e3eb7a405c`  
		Last Modified: Fri, 03 Sep 2021 07:23:37 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d985c8447020bf59910488f403f842aa681c83349963f713e2552b54cc1559`  
		Last Modified: Fri, 03 Sep 2021 07:23:56 GMT  
		Size: 25.7 MB (25737754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:f3721cf677ee4fe6eeb9c757e7e0bf0faebbfdfe5942c6f515b0cf1e45372425
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f450d60fb7b5103dad6aa7b14ae87b78da88df0a7cf341bed22d676b455e95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:53:28 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 04:53:43 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 04:54:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b751b21d089e680f6da69f7b8eba65cfd34ec336fdc51580b3847b39965ef9a`  
		Last Modified: Tue, 28 Sep 2021 04:59:58 GMT  
		Size: 255.9 KB (255923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2601a6dd7d5beaad12a0519f8ba90c7df66acb8a5dc81279c35fe6162d50a4e6`  
		Last Modified: Tue, 28 Sep 2021 05:00:04 GMT  
		Size: 31.8 MB (31769945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:17a92d3b707ead6f1ffd7fbfbb386bda7f46f888c07036ee5fe3e79fefb5e97a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99207485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2b71ab8631041a02064dc75c2eddce521e452f50114c2967392a3418944855`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:49 GMT
ADD file:c090abbb3afcfebf797e06e2ac4b778acb4e97d5dca79c29d1927f43cf14b23e in / 
# Tue, 28 Sep 2021 01:40:49 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:28:04 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 28 Sep 2021 08:28:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 28 Sep 2021 08:29:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:82f7c8b98609aee82696182c03cb09ae62ceab1b17f8eec1e233a68180876d41`  
		Last Modified: Tue, 28 Sep 2021 01:50:06 GMT  
		Size: 27.8 MB (27797629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd47d582cba43c893da5c58ffe6ddd70edcb3a681a8e4a38c96d7c7945d52ca8`  
		Last Modified: Tue, 28 Sep 2021 08:33:46 GMT  
		Size: 256.0 KB (255957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92415e43d551139c225b91bbb9fb519a9852327832f035906ee21534cbf2ccef`  
		Last Modified: Tue, 28 Sep 2021 08:34:01 GMT  
		Size: 71.2 MB (71153899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:246b89a98ed402f68e362e5071d08884b53e4a6e66a0594ba58a2f7fcb27764a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4e719554a822c0a6e8d0da2a4d9711f875e416cb9993bc0e3adf300c33d822`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:24:33 GMT
ADD file:6c1662ddb92232ae8969a86a18dacab97b3b5792a1ecda49e6ac741a1a5c878c in / 
# Fri, 03 Sep 2021 01:24:41 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:23:08 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 03 Sep 2021 08:25:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 03 Sep 2021 08:26:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8258146296247df1f308a336d4abf286afae14e3375edefb87a091e80745e29f`  
		Last Modified: Fri, 03 Sep 2021 01:39:45 GMT  
		Size: 30.6 MB (30553675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fcd88e98a8c542138e173bd2d3a18fbf8dd3cda3b870b754928dabcc051ad`  
		Last Modified: Fri, 03 Sep 2021 08:45:34 GMT  
		Size: 256.1 KB (256149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0042f91bcb537d4c7e2f158954a705080702b91cc826701626dc0375b741ab`  
		Last Modified: Fri, 03 Sep 2021 08:45:40 GMT  
		Size: 29.4 MB (29360180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
