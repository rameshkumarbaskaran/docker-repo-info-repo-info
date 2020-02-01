<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:5`](#mono5)
-	[`mono:5.20`](#mono520)
-	[`mono:5.20.1`](#mono5201)
-	[`mono:5.20.1.34`](#mono520134)
-	[`mono:5.20.1.34-slim`](#mono520134-slim)
-	[`mono:5.20.1-slim`](#mono5201-slim)
-	[`mono:5.20-slim`](#mono520-slim)
-	[`mono:5-slim`](#mono5-slim)
-	[`mono:6`](#mono6)
-	[`mono:6.6`](#mono66)
-	[`mono:6.6.0`](#mono660)
-	[`mono:6.6.0.161`](#mono660161)
-	[`mono:6.6.0.161-slim`](#mono660161-slim)
-	[`mono:6.6.0-slim`](#mono660-slim)
-	[`mono:6.6-slim`](#mono66-slim)
-	[`mono:6.8`](#mono68)
-	[`mono:6.8.0`](#mono680)
-	[`mono:6.8.0.96`](#mono68096)
-	[`mono:6.8.0.96-slim`](#mono68096-slim)
-	[`mono:6.8.0-slim`](#mono680-slim)
-	[`mono:6.8-slim`](#mono68-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:5`

```console
$ docker pull mono@sha256:29757647015b61caa2b335b2ffd1175256fdc467aedf73954b6517d443aee8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v5

```console
$ docker pull mono@sha256:55d0b080083478b3a5ef1d8a48f256b1e66b01ca751d91ed352ed49d702bb0c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90041d1c9f6abe67cd6020bbe946d836069825393f322006c895c74680f748f2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:23:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55504adbc2f81231b585edccf72bbcdbd2b48de43a22e8761d8b0bf8119674c`  
		Last Modified: Sat, 01 Feb 2020 18:27:36 GMT  
		Size: 125.2 MB (125240193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea93051fc182619236da49b4f8af1fe2ced078139afbb0b9828fe6d8ddce2a66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae25a953f1102bc295958da0ee5d66c3967a954d74185373dc0cc996fefd03e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:50:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc1b9fb79e6753ea4fae8558019fb0a5eb7ca081db778816494f72a406c701`  
		Last Modified: Sat, 01 Feb 2020 17:54:25 GMT  
		Size: 123.9 MB (123886389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e5b76a4e8f2339717c7ab0a574146e72597f3757dc25ad8daaca174fa79c2d10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187815739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62b02d970d77662d628cd3de1ec8ca0d054de849c8223a2195eb41eb1027051`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:26:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dd22c4ebf5e3dc676bafae61334358c5d901357c869b2003396b7d2025449b`  
		Last Modified: Sat, 01 Feb 2020 20:30:57 GMT  
		Size: 139.0 MB (139029542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; ppc64le

```console
$ docker pull mono@sha256:e2d6bff0737f5c17c470fe744a0d1b6dcdb92f835188fb32cf3a9a50ee2229ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173306474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b6caa1c889a7c2b754a0f669f6aa77e5c9768bd81d952ef99fe5b902ed789`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:19:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c3dd79cb595ab1e91cde00ee6c88fe6152836b6bab6e58f871cf1eb5f28404`  
		Last Modified: Sat, 01 Feb 2020 18:23:27 GMT  
		Size: 125.6 MB (125621908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20`

```console
$ docker pull mono@sha256:29757647015b61caa2b335b2ffd1175256fdc467aedf73954b6517d443aee8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v5

```console
$ docker pull mono@sha256:55d0b080083478b3a5ef1d8a48f256b1e66b01ca751d91ed352ed49d702bb0c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90041d1c9f6abe67cd6020bbe946d836069825393f322006c895c74680f748f2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:23:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55504adbc2f81231b585edccf72bbcdbd2b48de43a22e8761d8b0bf8119674c`  
		Last Modified: Sat, 01 Feb 2020 18:27:36 GMT  
		Size: 125.2 MB (125240193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea93051fc182619236da49b4f8af1fe2ced078139afbb0b9828fe6d8ddce2a66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae25a953f1102bc295958da0ee5d66c3967a954d74185373dc0cc996fefd03e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:50:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc1b9fb79e6753ea4fae8558019fb0a5eb7ca081db778816494f72a406c701`  
		Last Modified: Sat, 01 Feb 2020 17:54:25 GMT  
		Size: 123.9 MB (123886389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e5b76a4e8f2339717c7ab0a574146e72597f3757dc25ad8daaca174fa79c2d10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187815739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62b02d970d77662d628cd3de1ec8ca0d054de849c8223a2195eb41eb1027051`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:26:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dd22c4ebf5e3dc676bafae61334358c5d901357c869b2003396b7d2025449b`  
		Last Modified: Sat, 01 Feb 2020 20:30:57 GMT  
		Size: 139.0 MB (139029542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; ppc64le

```console
$ docker pull mono@sha256:e2d6bff0737f5c17c470fe744a0d1b6dcdb92f835188fb32cf3a9a50ee2229ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173306474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b6caa1c889a7c2b754a0f669f6aa77e5c9768bd81d952ef99fe5b902ed789`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:19:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c3dd79cb595ab1e91cde00ee6c88fe6152836b6bab6e58f871cf1eb5f28404`  
		Last Modified: Sat, 01 Feb 2020 18:23:27 GMT  
		Size: 125.6 MB (125621908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1`

```console
$ docker pull mono@sha256:29757647015b61caa2b335b2ffd1175256fdc467aedf73954b6517d443aee8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v5

```console
$ docker pull mono@sha256:55d0b080083478b3a5ef1d8a48f256b1e66b01ca751d91ed352ed49d702bb0c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90041d1c9f6abe67cd6020bbe946d836069825393f322006c895c74680f748f2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:23:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55504adbc2f81231b585edccf72bbcdbd2b48de43a22e8761d8b0bf8119674c`  
		Last Modified: Sat, 01 Feb 2020 18:27:36 GMT  
		Size: 125.2 MB (125240193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea93051fc182619236da49b4f8af1fe2ced078139afbb0b9828fe6d8ddce2a66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae25a953f1102bc295958da0ee5d66c3967a954d74185373dc0cc996fefd03e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:50:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc1b9fb79e6753ea4fae8558019fb0a5eb7ca081db778816494f72a406c701`  
		Last Modified: Sat, 01 Feb 2020 17:54:25 GMT  
		Size: 123.9 MB (123886389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e5b76a4e8f2339717c7ab0a574146e72597f3757dc25ad8daaca174fa79c2d10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187815739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62b02d970d77662d628cd3de1ec8ca0d054de849c8223a2195eb41eb1027051`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:26:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dd22c4ebf5e3dc676bafae61334358c5d901357c869b2003396b7d2025449b`  
		Last Modified: Sat, 01 Feb 2020 20:30:57 GMT  
		Size: 139.0 MB (139029542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; ppc64le

```console
$ docker pull mono@sha256:e2d6bff0737f5c17c470fe744a0d1b6dcdb92f835188fb32cf3a9a50ee2229ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173306474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b6caa1c889a7c2b754a0f669f6aa77e5c9768bd81d952ef99fe5b902ed789`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:19:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c3dd79cb595ab1e91cde00ee6c88fe6152836b6bab6e58f871cf1eb5f28404`  
		Last Modified: Sat, 01 Feb 2020 18:23:27 GMT  
		Size: 125.6 MB (125621908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34`

```console
$ docker pull mono@sha256:29757647015b61caa2b335b2ffd1175256fdc467aedf73954b6517d443aee8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1.34` - linux; amd64

```console
$ docker pull mono@sha256:5c3479e37ebaba3938b41d85e43aa685b34b38c7d39f65838ccc250a77a1bdfe
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843d1b62c0468f21ddbfb2ead8f14088f88b3483c3d7c5bbc29fcb42f3a8e8f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:47:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239a7387a2c6ed35e9e5467be5fcd6f83491d432b82e02ec511057d4c8575205`  
		Last Modified: Sat, 28 Dec 2019 13:50:58 GMT  
		Size: 140.0 MB (139993444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v5

```console
$ docker pull mono@sha256:55d0b080083478b3a5ef1d8a48f256b1e66b01ca751d91ed352ed49d702bb0c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170952922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90041d1c9f6abe67cd6020bbe946d836069825393f322006c895c74680f748f2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:23:11 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55504adbc2f81231b585edccf72bbcdbd2b48de43a22e8761d8b0bf8119674c`  
		Last Modified: Sat, 01 Feb 2020 18:27:36 GMT  
		Size: 125.2 MB (125240193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v7

```console
$ docker pull mono@sha256:ea93051fc182619236da49b4f8af1fe2ced078139afbb0b9828fe6d8ddce2a66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167004002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae25a953f1102bc295958da0ee5d66c3967a954d74185373dc0cc996fefd03e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:50:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fc1b9fb79e6753ea4fae8558019fb0a5eb7ca081db778816494f72a406c701`  
		Last Modified: Sat, 01 Feb 2020 17:54:25 GMT  
		Size: 123.9 MB (123886389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e5b76a4e8f2339717c7ab0a574146e72597f3757dc25ad8daaca174fa79c2d10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187815739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62b02d970d77662d628cd3de1ec8ca0d054de849c8223a2195eb41eb1027051`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:26:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dd22c4ebf5e3dc676bafae61334358c5d901357c869b2003396b7d2025449b`  
		Last Modified: Sat, 01 Feb 2020 20:30:57 GMT  
		Size: 139.0 MB (139029542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; 386

```console
$ docker pull mono@sha256:f7dc31da4a9c0214be8de4be179c3447a71b7b3de432db0a73f592aa388349e8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227783487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbff081eeb3cc7d2fbd105c967757897aedc5e0aa95508184be517694b48419`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 09:03:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724b594c451feb85210631e54662992230c04f5e689387accacb9bf2825c06ed`  
		Last Modified: Sat, 28 Dec 2019 09:07:08 GMT  
		Size: 145.8 MB (145835090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; ppc64le

```console
$ docker pull mono@sha256:e2d6bff0737f5c17c470fe744a0d1b6dcdb92f835188fb32cf3a9a50ee2229ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173306474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b6caa1c889a7c2b754a0f669f6aa77e5c9768bd81d952ef99fe5b902ed789`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:19:36 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c3dd79cb595ab1e91cde00ee6c88fe6152836b6bab6e58f871cf1eb5f28404`  
		Last Modified: Sat, 01 Feb 2020 18:23:27 GMT  
		Size: 125.6 MB (125621908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34-slim`

```console
$ docker pull mono@sha256:415ccdff72bf644d46b8e73b646440369ad5488428fdde8ba139995ca5f3c8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1.34-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9f6125399657e1d2bb14980aa34d4b96fffbc3cc54165bd9d4105e38d7ff1d3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f465c7a2b9a5c9c9e156836692808760376465d0d03a379623fde3350a5783`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fff7c4d8d7c15ccab3e89b190223c86788f2b561cb2c146e558d729ccee5b832
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cd4368baddfad8bd1933c9a8a5433d1cd3933ae92f8a2a8e9be3195ed8fbe0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ba7cfedc08ba3234b18153b29f183c466a5d0e9459967792d88c7ad1429e6aee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab559878f0ad28c78a584db9031692e20712c6514db0a0ccfe220f794e4175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a27010df02a34de75867490b0d3d3a9d135b2cb8ca625933fb043122ded65b40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8677aa71c7c75538622679ecc649f68827874795c0e1493b2c6de62d88e980d6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1-slim`

```console
$ docker pull mono@sha256:415ccdff72bf644d46b8e73b646440369ad5488428fdde8ba139995ca5f3c8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20.1-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9f6125399657e1d2bb14980aa34d4b96fffbc3cc54165bd9d4105e38d7ff1d3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f465c7a2b9a5c9c9e156836692808760376465d0d03a379623fde3350a5783`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fff7c4d8d7c15ccab3e89b190223c86788f2b561cb2c146e558d729ccee5b832
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cd4368baddfad8bd1933c9a8a5433d1cd3933ae92f8a2a8e9be3195ed8fbe0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ba7cfedc08ba3234b18153b29f183c466a5d0e9459967792d88c7ad1429e6aee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab559878f0ad28c78a584db9031692e20712c6514db0a0ccfe220f794e4175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a27010df02a34de75867490b0d3d3a9d135b2cb8ca625933fb043122ded65b40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8677aa71c7c75538622679ecc649f68827874795c0e1493b2c6de62d88e980d6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20-slim`

```console
$ docker pull mono@sha256:415ccdff72bf644d46b8e73b646440369ad5488428fdde8ba139995ca5f3c8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5.20-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9f6125399657e1d2bb14980aa34d4b96fffbc3cc54165bd9d4105e38d7ff1d3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f465c7a2b9a5c9c9e156836692808760376465d0d03a379623fde3350a5783`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fff7c4d8d7c15ccab3e89b190223c86788f2b561cb2c146e558d729ccee5b832
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cd4368baddfad8bd1933c9a8a5433d1cd3933ae92f8a2a8e9be3195ed8fbe0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ba7cfedc08ba3234b18153b29f183c466a5d0e9459967792d88c7ad1429e6aee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab559878f0ad28c78a584db9031692e20712c6514db0a0ccfe220f794e4175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a27010df02a34de75867490b0d3d3a9d135b2cb8ca625933fb043122ded65b40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8677aa71c7c75538622679ecc649f68827874795c0e1493b2c6de62d88e980d6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5-slim`

```console
$ docker pull mono@sha256:415ccdff72bf644d46b8e73b646440369ad5488428fdde8ba139995ca5f3c8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:5-slim` - linux; amd64

```console
$ docker pull mono@sha256:cdacbba352e15efb4a84f8b75ec4e96c43ae5dcd8d2f2a76b5fb53100b32214e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78290482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1fc6fc66317cf629fd0743dff6784c1fad2e8e88cd9a07be738bc8a6ccfef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:16:12 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 13:16:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:17:03 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8529aa2b8c8794ada5de4f9745d3c774968df5014c707878957d1a32ac17603`  
		Last Modified: Sat, 28 Dec 2019 13:48:56 GMT  
		Size: 244.5 KB (244484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ee02007ec21f650fb90f3cac4c917ac5b5a84240a1092ff9be02b256bad72`  
		Last Modified: Sat, 28 Dec 2019 13:49:08 GMT  
		Size: 55.5 MB (55521389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9f6125399657e1d2bb14980aa34d4b96fffbc3cc54165bd9d4105e38d7ff1d3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f465c7a2b9a5c9c9e156836692808760376465d0d03a379623fde3350a5783`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:10:40 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 18:11:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:11:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b59e4ac75a76130ec77125ecd7e156e1758cf1ca1ecefa48715f72e037912f9`  
		Last Modified: Sat, 01 Feb 2020 18:24:44 GMT  
		Size: 244.6 KB (244558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f483767bed8e05367eec7297d9314b0c7316e78d81774bd3a5d028acc97472`  
		Last Modified: Sat, 01 Feb 2020 18:24:52 GMT  
		Size: 24.3 MB (24265330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fff7c4d8d7c15ccab3e89b190223c86788f2b561cb2c146e558d729ccee5b832
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43117613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cd4368baddfad8bd1933c9a8a5433d1cd3933ae92f8a2a8e9be3195ed8fbe0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:40:31 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:40:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:41:42 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cebfcb62e01658c02913a00f0cdc6c1e50ee21463a83f71715121d9a7ce83`  
		Last Modified: Sat, 01 Feb 2020 17:51:28 GMT  
		Size: 244.6 KB (244554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c315381cbfb94ff565682dbba2567c5fd9907625ce53eeafe545737234520b0`  
		Last Modified: Sat, 01 Feb 2020 17:51:36 GMT  
		Size: 23.6 MB (23561435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ba7cfedc08ba3234b18153b29f183c466a5d0e9459967792d88c7ad1429e6aee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ab559878f0ad28c78a584db9031692e20712c6514db0a0ccfe220f794e4175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:18:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 20:18:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:19:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece150351e6e2066cd7dfc59d9ed87904db44f72175a66316145097699d1ff0`  
		Last Modified: Sat, 01 Feb 2020 20:28:08 GMT  
		Size: 244.4 KB (244395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e547d270466c12baf3078ab3140164e9ccffb59d83844a9dfb1c328938835b`  
		Last Modified: Sat, 01 Feb 2020 20:28:17 GMT  
		Size: 28.2 MB (28155951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; 386

```console
$ docker pull mono@sha256:96288130247b476a2e36fe48056efd7645d8ff9772e13178024ae4529801ea1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81948397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf00a5e27af46784e6f08920565478037a23309428ca7975d58b5a5814f8ba`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:55:21 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 28 Dec 2019 08:55:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:56:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b6f7471907c646ec285955dc4cf7094149b0ad93ea3e95125c4ef5f5d1171`  
		Last Modified: Sat, 28 Dec 2019 09:04:39 GMT  
		Size: 244.5 KB (244474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1c87cf35f42f1f93ef3f7676dee0b1b3f1ca6657c6afa49443d888dbc3360d`  
		Last Modified: Sat, 28 Dec 2019 09:04:53 GMT  
		Size: 58.6 MB (58551781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:a27010df02a34de75867490b0d3d3a9d135b2cb8ca625933fb043122ded65b40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47684566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8677aa71c7c75538622679ecc649f68827874795c0e1493b2c6de62d88e980d6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:50 GMT
ENV MONO_VERSION=5.20.1.34
# Sat, 01 Feb 2020 17:54:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:56:09 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d69bdb77fd9f07bc8f2f09cf69c3a5071e8f99fb707b263176e096d5c3bd32`  
		Last Modified: Sat, 01 Feb 2020 18:21:09 GMT  
		Size: 244.5 KB (244487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf181d637d24519cc9783943d3a9e43ad1b9295f066e6f82b405b534dca764cd`  
		Last Modified: Sat, 01 Feb 2020 18:21:16 GMT  
		Size: 24.6 MB (24639320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6`

```console
$ docker pull mono@sha256:e1f9d68577e94e2fcc34111781f51f3d6c7466ef970455479842f2eb871dd93e
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
$ docker pull mono@sha256:7948ca5193732f4ab443b242d9a284b5b377a1d4d32fabd2b9f0494dec6963b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235148673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5184391de3f6b76346daeeeb23f79f43011decc5ce6bc572f425291dc49ba6e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 21:31:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037709db234c6aa291803f4776a7569eb1f02aedd2781ac9b4308fa0a8548b42`  
		Last Modified: Thu, 16 Jan 2020 21:32:44 GMT  
		Size: 147.8 MB (147794425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:54bab175861028052f3094b5367979ce25edac68d35c174b4eac2d24cd9869d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176708017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed7f9f6e5ac53c325cbdbd5fc43c3fb82a4c78095e7cacd6db5036b4e6ec56f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:15:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c9e8408fb0f096a5defc8aa833384120bacdba2536b97ca0f98907a161c34c`  
		Last Modified: Sat, 01 Feb 2020 18:25:47 GMT  
		Size: 129.9 MB (129891684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:e8c3b4a96526f7b14b093f31777805e730008e0495125e99a3836a13003592f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172715546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbcf3978da4b10aa490eb3fff91f5171301abbc16e854bd73eb6f771d811c10`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:44:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fe839bf8f56a8d913f3b1e7bf6f7c2715aa9ed6923464ff61b10dd88c684d`  
		Last Modified: Sat, 01 Feb 2020 17:52:30 GMT  
		Size: 128.6 MB (128555278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5a472f7dad952809cb4a149b9b530f3378d40b1ce37706fd0cc295058e6bed9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194763168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74814fa60075a22b4fbc4c7d8f14d375f0199a86f70528b1adc5619decabc3e1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:21:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e95cf65e4cd19670ee250e0b6c1aafdb06745cfcf49ebe5e4276f42d5523f39`  
		Last Modified: Sat, 01 Feb 2020 20:29:10 GMT  
		Size: 144.7 MB (144712847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:dde073bd368f9a6c2892ca2e68f30d65dfbd7d4829989b163e6ab490a643410d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243518701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e307147ebfcf6ceef152bd8d45d910e6111eb1d1a97e4fa72ec9b799b9c6a5f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 20:41:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ebfa3d96f84743b6cd1c1dd57bd7b194744cfb740d7f4a9530b7c38ad344fa`  
		Last Modified: Thu, 16 Jan 2020 20:43:07 GMT  
		Size: 151.5 MB (151491580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:b4b29c1e014ef943c2791de20ce1cb2148e4cd101cc64462822205324eaacdc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179009804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9230b1fc8c21cab858e44af5b866fac6e7043b5fcc11f6f5e2d42d0a7dc2fe5b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:01:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a999d3b52ef279123d4422cba8b16762fec7d01740d75db5b67270cc454a674`  
		Last Modified: Sat, 01 Feb 2020 18:21:59 GMT  
		Size: 130.2 MB (130189242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6`

```console
$ docker pull mono@sha256:8b5971e04c3846afb7989a0fa5055712b439a0cd0e8b6ff51cf280c93f8edf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v5

```console
$ docker pull mono@sha256:dd37300f013c7f84d808b986860b89a47f0eec24cc5b72575ea9363358fd9bef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176512231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02506462e430a2a35ef500d2f670e2d300e56f006b496b04d7344381a57e46bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:09:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 18:09:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:18:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de4d5738afbab2019627443d31b31fc1f13d0ec419eb70f3f6d712a37a4dd2`  
		Last Modified: Sat, 01 Feb 2020 18:24:08 GMT  
		Size: 244.5 KB (244542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3840c17199885c49b50f80d19cc7de06c15e8ea3615bfa6edaf32947034d1`  
		Last Modified: Sat, 01 Feb 2020 18:24:36 GMT  
		Size: 25.4 MB (25416901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d82a57adbb19613503b3b0df62fcf30151585038dc6040cf69fc94730d98f0f`  
		Last Modified: Sat, 01 Feb 2020 18:26:41 GMT  
		Size: 129.6 MB (129647947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v7

```console
$ docker pull mono@sha256:74f041cd83554fb9d20dd885b39fe026e00d6b63ab0078ef338b5e201af4a9d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172519907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5e3242986561772e8f04817de1051784fa500dcbd4389ecc4a153629fc0411`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:39:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:40:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:47:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c609c4edaf2ba1f45ee900c31b6d90c8492283b5784d72ec8585b4e96eab8d`  
		Last Modified: Sat, 01 Feb 2020 17:51:13 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4d47f8be45dd1afd33f4243185ff8f1577bc6c8902d985307328050b0fe94`  
		Last Modified: Sat, 01 Feb 2020 17:51:21 GMT  
		Size: 24.6 MB (24648308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67b87821ce06f915961a00c2434992f0698125dbdb6221de7ae939b19c9b898`  
		Last Modified: Sat, 01 Feb 2020 17:53:29 GMT  
		Size: 128.3 MB (128315434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:362b85fa9906fc15bc96617bdafc80ea456bb3c446657350fa12dc5828799403
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194405864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41197640265d2b9ce7306c046265cc398e03ed38e9376731cfed3dda2709a853`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:17:05 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 20:17:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:18:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:24:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0988f395f0e7fd7ea2a03ffd1117a3461de43b8b348e30ce1a2b75797818b52`  
		Last Modified: Sat, 01 Feb 2020 20:27:51 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb7d26f25aba05048c8334fbdc1776e38116a8918c440af906bfa1be63917d`  
		Last Modified: Sat, 01 Feb 2020 20:28:01 GMT  
		Size: 29.4 MB (29434159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4707232c9c4090f76eb094f751275cb9a1376cd46c76ea8907a83f6e1b47fe77`  
		Last Modified: Sat, 01 Feb 2020 20:30:06 GMT  
		Size: 144.3 MB (144341470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; ppc64le

```console
$ docker pull mono@sha256:c17e981d2e196b9960dc81557c5c73601bfd6171c0920f2ca2c1f985606933d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178814834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3cc94c26ade4a890a7313d21c33a9ded78c83ac544c7953d1b3b8eea59b56`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:51:37 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:52:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:53:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:08:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fb63edcfd00f44052e41e704d58b6099c321c67ca624343e158e511375226`  
		Last Modified: Sat, 01 Feb 2020 18:20:49 GMT  
		Size: 244.5 KB (244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a7f7c7057a3b7ef0bd1529ff61859426bf9bda79aaff74de7c2a3f4ad1f609`  
		Last Modified: Sat, 01 Feb 2020 18:20:57 GMT  
		Size: 25.8 MB (25828597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d02bbc2775b08c913b8dc79cdfbbeed41b9e7abeff7d9a059026e0c6b60b858`  
		Last Modified: Sat, 01 Feb 2020 18:22:45 GMT  
		Size: 129.9 MB (129940949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0`

```console
$ docker pull mono@sha256:8b5971e04c3846afb7989a0fa5055712b439a0cd0e8b6ff51cf280c93f8edf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:dd37300f013c7f84d808b986860b89a47f0eec24cc5b72575ea9363358fd9bef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176512231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02506462e430a2a35ef500d2f670e2d300e56f006b496b04d7344381a57e46bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:09:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 18:09:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:18:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de4d5738afbab2019627443d31b31fc1f13d0ec419eb70f3f6d712a37a4dd2`  
		Last Modified: Sat, 01 Feb 2020 18:24:08 GMT  
		Size: 244.5 KB (244542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3840c17199885c49b50f80d19cc7de06c15e8ea3615bfa6edaf32947034d1`  
		Last Modified: Sat, 01 Feb 2020 18:24:36 GMT  
		Size: 25.4 MB (25416901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d82a57adbb19613503b3b0df62fcf30151585038dc6040cf69fc94730d98f0f`  
		Last Modified: Sat, 01 Feb 2020 18:26:41 GMT  
		Size: 129.6 MB (129647947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:74f041cd83554fb9d20dd885b39fe026e00d6b63ab0078ef338b5e201af4a9d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172519907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5e3242986561772e8f04817de1051784fa500dcbd4389ecc4a153629fc0411`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:39:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:40:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:47:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c609c4edaf2ba1f45ee900c31b6d90c8492283b5784d72ec8585b4e96eab8d`  
		Last Modified: Sat, 01 Feb 2020 17:51:13 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4d47f8be45dd1afd33f4243185ff8f1577bc6c8902d985307328050b0fe94`  
		Last Modified: Sat, 01 Feb 2020 17:51:21 GMT  
		Size: 24.6 MB (24648308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67b87821ce06f915961a00c2434992f0698125dbdb6221de7ae939b19c9b898`  
		Last Modified: Sat, 01 Feb 2020 17:53:29 GMT  
		Size: 128.3 MB (128315434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:362b85fa9906fc15bc96617bdafc80ea456bb3c446657350fa12dc5828799403
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194405864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41197640265d2b9ce7306c046265cc398e03ed38e9376731cfed3dda2709a853`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:17:05 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 20:17:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:18:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:24:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0988f395f0e7fd7ea2a03ffd1117a3461de43b8b348e30ce1a2b75797818b52`  
		Last Modified: Sat, 01 Feb 2020 20:27:51 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb7d26f25aba05048c8334fbdc1776e38116a8918c440af906bfa1be63917d`  
		Last Modified: Sat, 01 Feb 2020 20:28:01 GMT  
		Size: 29.4 MB (29434159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4707232c9c4090f76eb094f751275cb9a1376cd46c76ea8907a83f6e1b47fe77`  
		Last Modified: Sat, 01 Feb 2020 20:30:06 GMT  
		Size: 144.3 MB (144341470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; ppc64le

```console
$ docker pull mono@sha256:c17e981d2e196b9960dc81557c5c73601bfd6171c0920f2ca2c1f985606933d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178814834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3cc94c26ade4a890a7313d21c33a9ded78c83ac544c7953d1b3b8eea59b56`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:51:37 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:52:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:53:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:08:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fb63edcfd00f44052e41e704d58b6099c321c67ca624343e158e511375226`  
		Last Modified: Sat, 01 Feb 2020 18:20:49 GMT  
		Size: 244.5 KB (244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a7f7c7057a3b7ef0bd1529ff61859426bf9bda79aaff74de7c2a3f4ad1f609`  
		Last Modified: Sat, 01 Feb 2020 18:20:57 GMT  
		Size: 25.8 MB (25828597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d02bbc2775b08c913b8dc79cdfbbeed41b9e7abeff7d9a059026e0c6b60b858`  
		Last Modified: Sat, 01 Feb 2020 18:22:45 GMT  
		Size: 129.9 MB (129940949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161`

```console
$ docker pull mono@sha256:8b5971e04c3846afb7989a0fa5055712b439a0cd0e8b6ff51cf280c93f8edf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0.161` - linux; amd64

```console
$ docker pull mono@sha256:3f3ad551a8789a79e3b59c836a659dc748626b0c18543cc9d32ecc1f3d01ee32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233195367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ed216b8ba57507781ef13d31102febe0415d37333dd05d96e05f92ad9e9ca3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 13:27:55 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e6e2e990789fcd233754f316f68b3dcf7fcc8affcb267f1770e6abecd0a4df`  
		Last Modified: Sat, 28 Dec 2019 13:49:41 GMT  
		Size: 147.5 MB (147452344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v5

```console
$ docker pull mono@sha256:dd37300f013c7f84d808b986860b89a47f0eec24cc5b72575ea9363358fd9bef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176512231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02506462e430a2a35ef500d2f670e2d300e56f006b496b04d7344381a57e46bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:09:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 18:09:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:18:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de4d5738afbab2019627443d31b31fc1f13d0ec419eb70f3f6d712a37a4dd2`  
		Last Modified: Sat, 01 Feb 2020 18:24:08 GMT  
		Size: 244.5 KB (244542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3840c17199885c49b50f80d19cc7de06c15e8ea3615bfa6edaf32947034d1`  
		Last Modified: Sat, 01 Feb 2020 18:24:36 GMT  
		Size: 25.4 MB (25416901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d82a57adbb19613503b3b0df62fcf30151585038dc6040cf69fc94730d98f0f`  
		Last Modified: Sat, 01 Feb 2020 18:26:41 GMT  
		Size: 129.6 MB (129647947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v7

```console
$ docker pull mono@sha256:74f041cd83554fb9d20dd885b39fe026e00d6b63ab0078ef338b5e201af4a9d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172519907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5e3242986561772e8f04817de1051784fa500dcbd4389ecc4a153629fc0411`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:39:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:40:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:47:30 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c609c4edaf2ba1f45ee900c31b6d90c8492283b5784d72ec8585b4e96eab8d`  
		Last Modified: Sat, 01 Feb 2020 17:51:13 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4d47f8be45dd1afd33f4243185ff8f1577bc6c8902d985307328050b0fe94`  
		Last Modified: Sat, 01 Feb 2020 17:51:21 GMT  
		Size: 24.6 MB (24648308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67b87821ce06f915961a00c2434992f0698125dbdb6221de7ae939b19c9b898`  
		Last Modified: Sat, 01 Feb 2020 17:53:29 GMT  
		Size: 128.3 MB (128315434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:362b85fa9906fc15bc96617bdafc80ea456bb3c446657350fa12dc5828799403
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194405864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41197640265d2b9ce7306c046265cc398e03ed38e9376731cfed3dda2709a853`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:17:05 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 20:17:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:18:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:24:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0988f395f0e7fd7ea2a03ffd1117a3461de43b8b348e30ce1a2b75797818b52`  
		Last Modified: Sat, 01 Feb 2020 20:27:51 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb7d26f25aba05048c8334fbdc1776e38116a8918c440af906bfa1be63917d`  
		Last Modified: Sat, 01 Feb 2020 20:28:01 GMT  
		Size: 29.4 MB (29434159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4707232c9c4090f76eb094f751275cb9a1376cd46c76ea8907a83f6e1b47fe77`  
		Last Modified: Sat, 01 Feb 2020 20:30:06 GMT  
		Size: 144.3 MB (144341470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; 386

```console
$ docker pull mono@sha256:113663c398fb93fe981888f95186bb46d53ceb70ec40b9dd5d2062147bcf30cb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c3139144abd4f519d829e1787e239be574822453c53467c29462efab37ff42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 28 Dec 2019 08:58:35 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126a79dc65a7868221d13b2fe454087df416e1ea28ef3fb313d2abba6692268`  
		Last Modified: Sat, 28 Dec 2019 09:05:37 GMT  
		Size: 151.3 MB (151294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; ppc64le

```console
$ docker pull mono@sha256:c17e981d2e196b9960dc81557c5c73601bfd6171c0920f2ca2c1f985606933d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178814834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb3cc94c26ade4a890a7313d21c33a9ded78c83ac544c7953d1b3b8eea59b56`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:51:37 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:52:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:53:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:08:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fb63edcfd00f44052e41e704d58b6099c321c67ca624343e158e511375226`  
		Last Modified: Sat, 01 Feb 2020 18:20:49 GMT  
		Size: 244.5 KB (244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a7f7c7057a3b7ef0bd1529ff61859426bf9bda79aaff74de7c2a3f4ad1f609`  
		Last Modified: Sat, 01 Feb 2020 18:20:57 GMT  
		Size: 25.8 MB (25828597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d02bbc2775b08c913b8dc79cdfbbeed41b9e7abeff7d9a059026e0c6b60b858`  
		Last Modified: Sat, 01 Feb 2020 18:22:45 GMT  
		Size: 129.9 MB (129940949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161-slim`

```console
$ docker pull mono@sha256:bc7216e9761370da1ed28c081c30e7f053fd98e26c262d9e5360757a503ff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0.161-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9677fc74545aa4b77ef2aaaa2cfd5e4898d573f846184d22d43347eb2f78c82c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46864284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be774a1c1b53d6ae225e614aca6845c54fb96349fd48b6d35880ef565bdbfa13`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:09:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 18:09:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de4d5738afbab2019627443d31b31fc1f13d0ec419eb70f3f6d712a37a4dd2`  
		Last Modified: Sat, 01 Feb 2020 18:24:08 GMT  
		Size: 244.5 KB (244542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3840c17199885c49b50f80d19cc7de06c15e8ea3615bfa6edaf32947034d1`  
		Last Modified: Sat, 01 Feb 2020 18:24:36 GMT  
		Size: 25.4 MB (25416901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:5af8b7089c2effefe710ae76f19e535cc3e08ac5a86f5d63c110ae0976cb1fdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518ffaad28657ebac0bd672391d563d4691681fc37a5c0723f0d177c3222290`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:39:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:40:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c609c4edaf2ba1f45ee900c31b6d90c8492283b5784d72ec8585b4e96eab8d`  
		Last Modified: Sat, 01 Feb 2020 17:51:13 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4d47f8be45dd1afd33f4243185ff8f1577bc6c8902d985307328050b0fe94`  
		Last Modified: Sat, 01 Feb 2020 17:51:21 GMT  
		Size: 24.6 MB (24648308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9d8d4a3be8d67d8710503aa610e75ea427aedbdb591512bf124379fcfeb31c10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47070b12214cff7cb0310d224188727031fa2ba43711ff8f81c3cb6afe40cc44`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:17:05 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 20:17:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:18:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0988f395f0e7fd7ea2a03ffd1117a3461de43b8b348e30ce1a2b75797818b52`  
		Last Modified: Sat, 01 Feb 2020 20:27:51 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb7d26f25aba05048c8334fbdc1776e38116a8918c440af906bfa1be63917d`  
		Last Modified: Sat, 01 Feb 2020 20:28:01 GMT  
		Size: 29.4 MB (29434159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:05f080cd3ca797903ac7d607dfc316a3fe7ea0392c74041f3962184dfd4d3904
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48873885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5eae0b029508a57b25a5d5a028c98809b15aba19d10d349cb67567a7d714d6a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:51:37 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:52:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:53:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fb63edcfd00f44052e41e704d58b6099c321c67ca624343e158e511375226`  
		Last Modified: Sat, 01 Feb 2020 18:20:49 GMT  
		Size: 244.5 KB (244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a7f7c7057a3b7ef0bd1529ff61859426bf9bda79aaff74de7c2a3f4ad1f609`  
		Last Modified: Sat, 01 Feb 2020 18:20:57 GMT  
		Size: 25.8 MB (25828597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0-slim`

```console
$ docker pull mono@sha256:bc7216e9761370da1ed28c081c30e7f053fd98e26c262d9e5360757a503ff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9677fc74545aa4b77ef2aaaa2cfd5e4898d573f846184d22d43347eb2f78c82c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46864284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be774a1c1b53d6ae225e614aca6845c54fb96349fd48b6d35880ef565bdbfa13`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:09:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 18:09:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de4d5738afbab2019627443d31b31fc1f13d0ec419eb70f3f6d712a37a4dd2`  
		Last Modified: Sat, 01 Feb 2020 18:24:08 GMT  
		Size: 244.5 KB (244542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3840c17199885c49b50f80d19cc7de06c15e8ea3615bfa6edaf32947034d1`  
		Last Modified: Sat, 01 Feb 2020 18:24:36 GMT  
		Size: 25.4 MB (25416901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:5af8b7089c2effefe710ae76f19e535cc3e08ac5a86f5d63c110ae0976cb1fdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518ffaad28657ebac0bd672391d563d4691681fc37a5c0723f0d177c3222290`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:39:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:40:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c609c4edaf2ba1f45ee900c31b6d90c8492283b5784d72ec8585b4e96eab8d`  
		Last Modified: Sat, 01 Feb 2020 17:51:13 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4d47f8be45dd1afd33f4243185ff8f1577bc6c8902d985307328050b0fe94`  
		Last Modified: Sat, 01 Feb 2020 17:51:21 GMT  
		Size: 24.6 MB (24648308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9d8d4a3be8d67d8710503aa610e75ea427aedbdb591512bf124379fcfeb31c10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47070b12214cff7cb0310d224188727031fa2ba43711ff8f81c3cb6afe40cc44`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:17:05 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 20:17:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:18:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0988f395f0e7fd7ea2a03ffd1117a3461de43b8b348e30ce1a2b75797818b52`  
		Last Modified: Sat, 01 Feb 2020 20:27:51 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb7d26f25aba05048c8334fbdc1776e38116a8918c440af906bfa1be63917d`  
		Last Modified: Sat, 01 Feb 2020 20:28:01 GMT  
		Size: 29.4 MB (29434159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:05f080cd3ca797903ac7d607dfc316a3fe7ea0392c74041f3962184dfd4d3904
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48873885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5eae0b029508a57b25a5d5a028c98809b15aba19d10d349cb67567a7d714d6a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:51:37 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:52:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:53:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fb63edcfd00f44052e41e704d58b6099c321c67ca624343e158e511375226`  
		Last Modified: Sat, 01 Feb 2020 18:20:49 GMT  
		Size: 244.5 KB (244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a7f7c7057a3b7ef0bd1529ff61859426bf9bda79aaff74de7c2a3f4ad1f609`  
		Last Modified: Sat, 01 Feb 2020 18:20:57 GMT  
		Size: 25.8 MB (25828597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6-slim`

```console
$ docker pull mono@sha256:bc7216e9761370da1ed28c081c30e7f053fd98e26c262d9e5360757a503ff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.6-slim` - linux; amd64

```console
$ docker pull mono@sha256:dbf079afc972cbf36017055c5dfa8b63e8495e68ed7a12782ff4e3b632100af0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85743023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13361f8aea3337ed6ca565868d63ed73db5104f6c26dfa91ce41d1ce1e5082`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 13:14:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 13:14:25 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 13:15:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e78f3e714bb9645ac8b6e172f033253467b1312e6dd4889da24aeee207e091`  
		Last Modified: Sat, 28 Dec 2019 13:48:14 GMT  
		Size: 244.5 KB (244485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64c5ff00a44477231f8da775a76ef1611f6e7879ef3116862f0e13f16e5575f`  
		Last Modified: Sat, 28 Dec 2019 13:48:30 GMT  
		Size: 63.0 MB (62973929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:9677fc74545aa4b77ef2aaaa2cfd5e4898d573f846184d22d43347eb2f78c82c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46864284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be774a1c1b53d6ae225e614aca6845c54fb96349fd48b6d35880ef565bdbfa13`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:09:10 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 18:09:34 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de4d5738afbab2019627443d31b31fc1f13d0ec419eb70f3f6d712a37a4dd2`  
		Last Modified: Sat, 01 Feb 2020 18:24:08 GMT  
		Size: 244.5 KB (244542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3840c17199885c49b50f80d19cc7de06c15e8ea3615bfa6edaf32947034d1`  
		Last Modified: Sat, 01 Feb 2020 18:24:36 GMT  
		Size: 25.4 MB (25416901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:5af8b7089c2effefe710ae76f19e535cc3e08ac5a86f5d63c110ae0976cb1fdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44204473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518ffaad28657ebac0bd672391d563d4691681fc37a5c0723f0d177c3222290`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:39:15 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:39:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:40:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c609c4edaf2ba1f45ee900c31b6d90c8492283b5784d72ec8585b4e96eab8d`  
		Last Modified: Sat, 01 Feb 2020 17:51:13 GMT  
		Size: 244.5 KB (244541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4d47f8be45dd1afd33f4243185ff8f1577bc6c8902d985307328050b0fe94`  
		Last Modified: Sat, 01 Feb 2020 17:51:21 GMT  
		Size: 24.6 MB (24648308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:9d8d4a3be8d67d8710503aa610e75ea427aedbdb591512bf124379fcfeb31c10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50064394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47070b12214cff7cb0310d224188727031fa2ba43711ff8f81c3cb6afe40cc44`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:17:05 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 20:17:24 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:18:04 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0988f395f0e7fd7ea2a03ffd1117a3461de43b8b348e30ce1a2b75797818b52`  
		Last Modified: Sat, 01 Feb 2020 20:27:51 GMT  
		Size: 244.4 KB (244384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb7d26f25aba05048c8334fbdc1776e38116a8918c440af906bfa1be63917d`  
		Last Modified: Sat, 01 Feb 2020 20:28:01 GMT  
		Size: 29.4 MB (29434159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; 386

```console
$ docker pull mono@sha256:1470434632f62ac60985681302e025a1a93fb7c696224fa2f5fbafb8f168bf7e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90146392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872c3284610e489106962651891765f6a5b3a1418c06cda514d1db86209162e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:53:34 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 28 Dec 2019 08:53:44 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 28 Dec 2019 08:54:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b4fc901f01e72498a390f3e82b1885f694d21c0c86b2c5b722170744653ee`  
		Last Modified: Sat, 28 Dec 2019 09:03:51 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef8b692587284955aed9af38c783ccb1813e5f21a78f50075e3a462a575820e`  
		Last Modified: Sat, 28 Dec 2019 09:04:10 GMT  
		Size: 66.7 MB (66749769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:05f080cd3ca797903ac7d607dfc316a3fe7ea0392c74041f3962184dfd4d3904
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48873885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5eae0b029508a57b25a5d5a028c98809b15aba19d10d349cb67567a7d714d6a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:51:37 GMT
ENV MONO_VERSION=6.6.0.161
# Sat, 01 Feb 2020 17:52:30 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:53:40 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fb63edcfd00f44052e41e704d58b6099c321c67ca624343e158e511375226`  
		Last Modified: Sat, 01 Feb 2020 18:20:49 GMT  
		Size: 244.5 KB (244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a7f7c7057a3b7ef0bd1529ff61859426bf9bda79aaff74de7c2a3f4ad1f609`  
		Last Modified: Sat, 01 Feb 2020 18:20:57 GMT  
		Size: 25.8 MB (25828597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:e1f9d68577e94e2fcc34111781f51f3d6c7466ef970455479842f2eb871dd93e
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
$ docker pull mono@sha256:7948ca5193732f4ab443b242d9a284b5b377a1d4d32fabd2b9f0494dec6963b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235148673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5184391de3f6b76346daeeeb23f79f43011decc5ce6bc572f425291dc49ba6e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 21:31:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037709db234c6aa291803f4776a7569eb1f02aedd2781ac9b4308fa0a8548b42`  
		Last Modified: Thu, 16 Jan 2020 21:32:44 GMT  
		Size: 147.8 MB (147794425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:54bab175861028052f3094b5367979ce25edac68d35c174b4eac2d24cd9869d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176708017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed7f9f6e5ac53c325cbdbd5fc43c3fb82a4c78095e7cacd6db5036b4e6ec56f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:15:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c9e8408fb0f096a5defc8aa833384120bacdba2536b97ca0f98907a161c34c`  
		Last Modified: Sat, 01 Feb 2020 18:25:47 GMT  
		Size: 129.9 MB (129891684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:e8c3b4a96526f7b14b093f31777805e730008e0495125e99a3836a13003592f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172715546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbcf3978da4b10aa490eb3fff91f5171301abbc16e854bd73eb6f771d811c10`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:44:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fe839bf8f56a8d913f3b1e7bf6f7c2715aa9ed6923464ff61b10dd88c684d`  
		Last Modified: Sat, 01 Feb 2020 17:52:30 GMT  
		Size: 128.6 MB (128555278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5a472f7dad952809cb4a149b9b530f3378d40b1ce37706fd0cc295058e6bed9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194763168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74814fa60075a22b4fbc4c7d8f14d375f0199a86f70528b1adc5619decabc3e1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:21:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e95cf65e4cd19670ee250e0b6c1aafdb06745cfcf49ebe5e4276f42d5523f39`  
		Last Modified: Sat, 01 Feb 2020 20:29:10 GMT  
		Size: 144.7 MB (144712847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:dde073bd368f9a6c2892ca2e68f30d65dfbd7d4829989b163e6ab490a643410d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243518701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e307147ebfcf6ceef152bd8d45d910e6111eb1d1a97e4fa72ec9b799b9c6a5f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 20:41:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ebfa3d96f84743b6cd1c1dd57bd7b194744cfb740d7f4a9530b7c38ad344fa`  
		Last Modified: Thu, 16 Jan 2020 20:43:07 GMT  
		Size: 151.5 MB (151491580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; ppc64le

```console
$ docker pull mono@sha256:b4b29c1e014ef943c2791de20ce1cb2148e4cd101cc64462822205324eaacdc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179009804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9230b1fc8c21cab858e44af5b866fac6e7043b5fcc11f6f5e2d42d0a7dc2fe5b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:01:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a999d3b52ef279123d4422cba8b16762fec7d01740d75db5b67270cc454a674`  
		Last Modified: Sat, 01 Feb 2020 18:21:59 GMT  
		Size: 130.2 MB (130189242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0`

```console
$ docker pull mono@sha256:e1f9d68577e94e2fcc34111781f51f3d6c7466ef970455479842f2eb871dd93e
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
$ docker pull mono@sha256:7948ca5193732f4ab443b242d9a284b5b377a1d4d32fabd2b9f0494dec6963b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235148673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5184391de3f6b76346daeeeb23f79f43011decc5ce6bc572f425291dc49ba6e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 21:31:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037709db234c6aa291803f4776a7569eb1f02aedd2781ac9b4308fa0a8548b42`  
		Last Modified: Thu, 16 Jan 2020 21:32:44 GMT  
		Size: 147.8 MB (147794425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:54bab175861028052f3094b5367979ce25edac68d35c174b4eac2d24cd9869d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176708017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed7f9f6e5ac53c325cbdbd5fc43c3fb82a4c78095e7cacd6db5036b4e6ec56f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:15:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c9e8408fb0f096a5defc8aa833384120bacdba2536b97ca0f98907a161c34c`  
		Last Modified: Sat, 01 Feb 2020 18:25:47 GMT  
		Size: 129.9 MB (129891684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:e8c3b4a96526f7b14b093f31777805e730008e0495125e99a3836a13003592f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172715546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbcf3978da4b10aa490eb3fff91f5171301abbc16e854bd73eb6f771d811c10`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:44:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fe839bf8f56a8d913f3b1e7bf6f7c2715aa9ed6923464ff61b10dd88c684d`  
		Last Modified: Sat, 01 Feb 2020 17:52:30 GMT  
		Size: 128.6 MB (128555278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5a472f7dad952809cb4a149b9b530f3378d40b1ce37706fd0cc295058e6bed9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194763168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74814fa60075a22b4fbc4c7d8f14d375f0199a86f70528b1adc5619decabc3e1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:21:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e95cf65e4cd19670ee250e0b6c1aafdb06745cfcf49ebe5e4276f42d5523f39`  
		Last Modified: Sat, 01 Feb 2020 20:29:10 GMT  
		Size: 144.7 MB (144712847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:dde073bd368f9a6c2892ca2e68f30d65dfbd7d4829989b163e6ab490a643410d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243518701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e307147ebfcf6ceef152bd8d45d910e6111eb1d1a97e4fa72ec9b799b9c6a5f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 20:41:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ebfa3d96f84743b6cd1c1dd57bd7b194744cfb740d7f4a9530b7c38ad344fa`  
		Last Modified: Thu, 16 Jan 2020 20:43:07 GMT  
		Size: 151.5 MB (151491580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; ppc64le

```console
$ docker pull mono@sha256:b4b29c1e014ef943c2791de20ce1cb2148e4cd101cc64462822205324eaacdc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179009804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9230b1fc8c21cab858e44af5b866fac6e7043b5fcc11f6f5e2d42d0a7dc2fe5b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:01:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a999d3b52ef279123d4422cba8b16762fec7d01740d75db5b67270cc454a674`  
		Last Modified: Sat, 01 Feb 2020 18:21:59 GMT  
		Size: 130.2 MB (130189242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.96`

```console
$ docker pull mono@sha256:e1f9d68577e94e2fcc34111781f51f3d6c7466ef970455479842f2eb871dd93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.96` - linux; amd64

```console
$ docker pull mono@sha256:7948ca5193732f4ab443b242d9a284b5b377a1d4d32fabd2b9f0494dec6963b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235148673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5184391de3f6b76346daeeeb23f79f43011decc5ce6bc572f425291dc49ba6e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 21:31:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037709db234c6aa291803f4776a7569eb1f02aedd2781ac9b4308fa0a8548b42`  
		Last Modified: Thu, 16 Jan 2020 21:32:44 GMT  
		Size: 147.8 MB (147794425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v5

```console
$ docker pull mono@sha256:54bab175861028052f3094b5367979ce25edac68d35c174b4eac2d24cd9869d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176708017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed7f9f6e5ac53c325cbdbd5fc43c3fb82a4c78095e7cacd6db5036b4e6ec56f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:15:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c9e8408fb0f096a5defc8aa833384120bacdba2536b97ca0f98907a161c34c`  
		Last Modified: Sat, 01 Feb 2020 18:25:47 GMT  
		Size: 129.9 MB (129891684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v7

```console
$ docker pull mono@sha256:e8c3b4a96526f7b14b093f31777805e730008e0495125e99a3836a13003592f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172715546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbcf3978da4b10aa490eb3fff91f5171301abbc16e854bd73eb6f771d811c10`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:44:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fe839bf8f56a8d913f3b1e7bf6f7c2715aa9ed6923464ff61b10dd88c684d`  
		Last Modified: Sat, 01 Feb 2020 17:52:30 GMT  
		Size: 128.6 MB (128555278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5a472f7dad952809cb4a149b9b530f3378d40b1ce37706fd0cc295058e6bed9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194763168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74814fa60075a22b4fbc4c7d8f14d375f0199a86f70528b1adc5619decabc3e1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:21:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e95cf65e4cd19670ee250e0b6c1aafdb06745cfcf49ebe5e4276f42d5523f39`  
		Last Modified: Sat, 01 Feb 2020 20:29:10 GMT  
		Size: 144.7 MB (144712847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; 386

```console
$ docker pull mono@sha256:dde073bd368f9a6c2892ca2e68f30d65dfbd7d4829989b163e6ab490a643410d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243518701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e307147ebfcf6ceef152bd8d45d910e6111eb1d1a97e4fa72ec9b799b9c6a5f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 20:41:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ebfa3d96f84743b6cd1c1dd57bd7b194744cfb740d7f4a9530b7c38ad344fa`  
		Last Modified: Thu, 16 Jan 2020 20:43:07 GMT  
		Size: 151.5 MB (151491580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; ppc64le

```console
$ docker pull mono@sha256:b4b29c1e014ef943c2791de20ce1cb2148e4cd101cc64462822205324eaacdc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179009804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9230b1fc8c21cab858e44af5b866fac6e7043b5fcc11f6f5e2d42d0a7dc2fe5b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:01:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a999d3b52ef279123d4422cba8b16762fec7d01740d75db5b67270cc454a674`  
		Last Modified: Sat, 01 Feb 2020 18:21:59 GMT  
		Size: 130.2 MB (130189242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.96-slim`

```console
$ docker pull mono@sha256:30ac8a3cd467ac0a02e3826f6659ca54d6d3fc3bd2623b976f0c00cafaeb3d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.8.0.96-slim` - linux; amd64

```console
$ docker pull mono@sha256:39aee858c84f60df113b186a6e9bb4741f8c291c3c44fb26f5f99548b3c8a9ce
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87354248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df205cc8792ae1d6c87a5b00ca176ff298624c67664624caeb149fe1c2752a3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2ebd775ca9adaf68e26f8c4c02f3d305388e259b5f1d4c021496f610bb0a3dfd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46816333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d800624a24de28eee73a1504ef77b3abf297ae19043eb2c0835f6708f901e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bad8e36b6e300784c212d4b98a79fcb25f11ced030338af8f6210cfa3c426f2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44160268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9158a4ba2c685e8b310f7a8293372583001de5a734c89692e2634c1c472ba46c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:765e0d192801e6bacd6752334d46724cf04e272bb75849b8bc862101e786727b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50050321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3accaf0621ee6c69ec500f6fed2ff611c18b54583bb122b3871315929226273`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; 386

```console
$ docker pull mono@sha256:5b50c5f68fb5a4604d744d6262d0ab80278d35e016024c6d894d5691f676dc2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92027121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c766847de03011bb0074648caf4c22771d9d59fa076abed42f333577a7a43f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89f17280ec4e1cba97f6d2401270a8ce20f8bd59a0ada224598a5bc01895cc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48820562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f9ae29abb2156fa6aa858573cab8a419900ca43eb5f4737279fa0e2c80ed2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:30ac8a3cd467ac0a02e3826f6659ca54d6d3fc3bd2623b976f0c00cafaeb3d72
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
$ docker pull mono@sha256:39aee858c84f60df113b186a6e9bb4741f8c291c3c44fb26f5f99548b3c8a9ce
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87354248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df205cc8792ae1d6c87a5b00ca176ff298624c67664624caeb149fe1c2752a3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2ebd775ca9adaf68e26f8c4c02f3d305388e259b5f1d4c021496f610bb0a3dfd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46816333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d800624a24de28eee73a1504ef77b3abf297ae19043eb2c0835f6708f901e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bad8e36b6e300784c212d4b98a79fcb25f11ced030338af8f6210cfa3c426f2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44160268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9158a4ba2c685e8b310f7a8293372583001de5a734c89692e2634c1c472ba46c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:765e0d192801e6bacd6752334d46724cf04e272bb75849b8bc862101e786727b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50050321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3accaf0621ee6c69ec500f6fed2ff611c18b54583bb122b3871315929226273`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:5b50c5f68fb5a4604d744d6262d0ab80278d35e016024c6d894d5691f676dc2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92027121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c766847de03011bb0074648caf4c22771d9d59fa076abed42f333577a7a43f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89f17280ec4e1cba97f6d2401270a8ce20f8bd59a0ada224598a5bc01895cc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48820562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f9ae29abb2156fa6aa858573cab8a419900ca43eb5f4737279fa0e2c80ed2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:30ac8a3cd467ac0a02e3826f6659ca54d6d3fc3bd2623b976f0c00cafaeb3d72
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
$ docker pull mono@sha256:39aee858c84f60df113b186a6e9bb4741f8c291c3c44fb26f5f99548b3c8a9ce
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87354248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df205cc8792ae1d6c87a5b00ca176ff298624c67664624caeb149fe1c2752a3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2ebd775ca9adaf68e26f8c4c02f3d305388e259b5f1d4c021496f610bb0a3dfd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46816333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d800624a24de28eee73a1504ef77b3abf297ae19043eb2c0835f6708f901e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bad8e36b6e300784c212d4b98a79fcb25f11ced030338af8f6210cfa3c426f2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44160268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9158a4ba2c685e8b310f7a8293372583001de5a734c89692e2634c1c472ba46c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:765e0d192801e6bacd6752334d46724cf04e272bb75849b8bc862101e786727b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50050321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3accaf0621ee6c69ec500f6fed2ff611c18b54583bb122b3871315929226273`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:5b50c5f68fb5a4604d744d6262d0ab80278d35e016024c6d894d5691f676dc2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92027121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c766847de03011bb0074648caf4c22771d9d59fa076abed42f333577a7a43f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89f17280ec4e1cba97f6d2401270a8ce20f8bd59a0ada224598a5bc01895cc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48820562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f9ae29abb2156fa6aa858573cab8a419900ca43eb5f4737279fa0e2c80ed2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:30ac8a3cd467ac0a02e3826f6659ca54d6d3fc3bd2623b976f0c00cafaeb3d72
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
$ docker pull mono@sha256:39aee858c84f60df113b186a6e9bb4741f8c291c3c44fb26f5f99548b3c8a9ce
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87354248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df205cc8792ae1d6c87a5b00ca176ff298624c67664624caeb149fe1c2752a3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2ebd775ca9adaf68e26f8c4c02f3d305388e259b5f1d4c021496f610bb0a3dfd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46816333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d800624a24de28eee73a1504ef77b3abf297ae19043eb2c0835f6708f901e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bad8e36b6e300784c212d4b98a79fcb25f11ced030338af8f6210cfa3c426f2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44160268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9158a4ba2c685e8b310f7a8293372583001de5a734c89692e2634c1c472ba46c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:765e0d192801e6bacd6752334d46724cf04e272bb75849b8bc862101e786727b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50050321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3accaf0621ee6c69ec500f6fed2ff611c18b54583bb122b3871315929226273`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:5b50c5f68fb5a4604d744d6262d0ab80278d35e016024c6d894d5691f676dc2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92027121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c766847de03011bb0074648caf4c22771d9d59fa076abed42f333577a7a43f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89f17280ec4e1cba97f6d2401270a8ce20f8bd59a0ada224598a5bc01895cc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48820562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f9ae29abb2156fa6aa858573cab8a419900ca43eb5f4737279fa0e2c80ed2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:e1f9d68577e94e2fcc34111781f51f3d6c7466ef970455479842f2eb871dd93e
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
$ docker pull mono@sha256:7948ca5193732f4ab443b242d9a284b5b377a1d4d32fabd2b9f0494dec6963b1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235148673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5184391de3f6b76346daeeeb23f79f43011decc5ce6bc572f425291dc49ba6e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 21:31:24 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037709db234c6aa291803f4776a7569eb1f02aedd2781ac9b4308fa0a8548b42`  
		Last Modified: Thu, 16 Jan 2020 21:32:44 GMT  
		Size: 147.8 MB (147794425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:54bab175861028052f3094b5367979ce25edac68d35c174b4eac2d24cd9869d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176708017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed7f9f6e5ac53c325cbdbd5fc43c3fb82a4c78095e7cacd6db5036b4e6ec56f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:15:12 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c9e8408fb0f096a5defc8aa833384120bacdba2536b97ca0f98907a161c34c`  
		Last Modified: Sat, 01 Feb 2020 18:25:47 GMT  
		Size: 129.9 MB (129891684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:e8c3b4a96526f7b14b093f31777805e730008e0495125e99a3836a13003592f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172715546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbcf3978da4b10aa490eb3fff91f5171301abbc16e854bd73eb6f771d811c10`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 17:44:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fe839bf8f56a8d913f3b1e7bf6f7c2715aa9ed6923464ff61b10dd88c684d`  
		Last Modified: Sat, 01 Feb 2020 17:52:30 GMT  
		Size: 128.6 MB (128555278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:5a472f7dad952809cb4a149b9b530f3378d40b1ce37706fd0cc295058e6bed9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194763168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74814fa60075a22b4fbc4c7d8f14d375f0199a86f70528b1adc5619decabc3e1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 20:21:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e95cf65e4cd19670ee250e0b6c1aafdb06745cfcf49ebe5e4276f42d5523f39`  
		Last Modified: Sat, 01 Feb 2020 20:29:10 GMT  
		Size: 144.7 MB (144712847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:dde073bd368f9a6c2892ca2e68f30d65dfbd7d4829989b163e6ab490a643410d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243518701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e307147ebfcf6ceef152bd8d45d910e6111eb1d1a97e4fa72ec9b799b9c6a5f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 16 Jan 2020 20:41:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ebfa3d96f84743b6cd1c1dd57bd7b194744cfb740d7f4a9530b7c38ad344fa`  
		Last Modified: Thu, 16 Jan 2020 20:43:07 GMT  
		Size: 151.5 MB (151491580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:b4b29c1e014ef943c2791de20ce1cb2148e4cd101cc64462822205324eaacdc5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179009804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9230b1fc8c21cab858e44af5b866fac6e7043b5fcc11f6f5e2d42d0a7dc2fe5b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Sat, 01 Feb 2020 18:01:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a999d3b52ef279123d4422cba8b16762fec7d01740d75db5b67270cc454a674`  
		Last Modified: Sat, 01 Feb 2020 18:21:59 GMT  
		Size: 130.2 MB (130189242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:30ac8a3cd467ac0a02e3826f6659ca54d6d3fc3bd2623b976f0c00cafaeb3d72
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
$ docker pull mono@sha256:39aee858c84f60df113b186a6e9bb4741f8c291c3c44fb26f5f99548b3c8a9ce
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87354248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df205cc8792ae1d6c87a5b00ca176ff298624c67664624caeb149fe1c2752a3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 21:22:42 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 21:22:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 21:23:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f1b80ee1bacf85e58bce19d99a6bc74b02f0777c3157dd361923df2f2f0e85`  
		Last Modified: Thu, 16 Jan 2020 21:31:52 GMT  
		Size: 244.5 KB (244481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c50129323d22c4aacfd3788f3cb571c52a0310fb6ba01e8807854b702c1644`  
		Last Modified: Thu, 16 Jan 2020 21:32:05 GMT  
		Size: 64.6 MB (64585158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2ebd775ca9adaf68e26f8c4c02f3d305388e259b5f1d4c021496f610bb0a3dfd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46816333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d800624a24de28eee73a1504ef77b3abf297ae19043eb2c0835f6708f901e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:53:57 GMT
ADD file:f0d179649cbf50028b5ecd832961cc332fb524c2f12fda6c8060c3c258208be6 in / 
# Sat, 01 Feb 2020 16:53:59 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:07:40 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 18:08:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 18:08:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:03886a8604d1b5423798ee97917dcb9de4cfdfbb7c435a7988d5c5e69a78e3b7`  
		Last Modified: Sat, 01 Feb 2020 17:01:03 GMT  
		Size: 21.2 MB (21202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956558813159fe712b991be4406aa3455301f7056c7cad3b9f964b396719889e`  
		Last Modified: Sat, 01 Feb 2020 18:23:47 GMT  
		Size: 244.5 KB (244549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcdd43b4c26f7cbae8d5ede3a17e3c99e5563390705e618682b7acda3efee7a`  
		Last Modified: Sat, 01 Feb 2020 18:23:56 GMT  
		Size: 25.4 MB (25368943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:bad8e36b6e300784c212d4b98a79fcb25f11ced030338af8f6210cfa3c426f2a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44160268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9158a4ba2c685e8b310f7a8293372583001de5a734c89692e2634c1c472ba46c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:38:00 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:38:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:39:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc9e95ca45f76f014694d99f355328e846b8b4965d8db8f448dbe07e279708`  
		Last Modified: Sat, 01 Feb 2020 17:50:50 GMT  
		Size: 244.5 KB (244528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb2bc6acff2c1d40bf6368e050ae759a24d86945fb9e6d51a8b52b58e95361`  
		Last Modified: Sat, 01 Feb 2020 17:50:59 GMT  
		Size: 24.6 MB (24604116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:765e0d192801e6bacd6752334d46724cf04e272bb75849b8bc862101e786727b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50050321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3accaf0621ee6c69ec500f6fed2ff611c18b54583bb122b3871315929226273`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:15:50 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 20:16:08 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 20:16:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f8fea4be7da1a44e0b664b6c28baee42f9c3d7aa7e1964a5c0cee8227936`  
		Last Modified: Sat, 01 Feb 2020 20:27:34 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60561a2c178b1b043bdcd15600acb0b469348e7c4fd6985e07a9dacf8164d2ab`  
		Last Modified: Sat, 01 Feb 2020 20:27:42 GMT  
		Size: 29.4 MB (29420090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:5b50c5f68fb5a4604d744d6262d0ab80278d35e016024c6d894d5691f676dc2f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92027121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c766847de03011bb0074648caf4c22771d9d59fa076abed42f333577a7a43f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Thu, 16 Jan 2020 20:38:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 16 Jan 2020 20:38:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 16 Jan 2020 20:39:20 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad3a63e1808da2e29053cff1fa8d22a2124d4f5109b28f76ae642481e4e42e`  
		Last Modified: Thu, 16 Jan 2020 20:42:06 GMT  
		Size: 244.5 KB (244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5269ebfb77642ca2643fee81b4723150468d2607e1db73cf44cf94aa7571e`  
		Last Modified: Thu, 16 Jan 2020 20:42:23 GMT  
		Size: 68.6 MB (68630517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89f17280ec4e1cba97f6d2401270a8ce20f8bd59a0ada224598a5bc01895cc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48820562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f9ae29abb2156fa6aa858573cab8a419900ca43eb5f4737279fa0e2c80ed2b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:8840e8b11ab671d52cc308dfcd68117cbff88d7e5e18e0628683d75699a7c131 in / 
# Sat, 01 Feb 2020 17:20:49 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:48:56 GMT
ENV MONO_VERSION=6.8.0.96
# Sat, 01 Feb 2020 17:50:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 01 Feb 2020 17:51:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4b12198d119cc40a2102fa8f986f1f3bc6f22967a421939f96b52470129050b9`  
		Last Modified: Sat, 01 Feb 2020 17:31:15 GMT  
		Size: 22.8 MB (22800759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dced62fef2ecb11062175a9bb4d40edc62d01b24904c13c8cc0d02fd207473a`  
		Last Modified: Sat, 01 Feb 2020 18:20:26 GMT  
		Size: 244.6 KB (244574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5582014ea26abafc9395ec9f22199a2fdb6597e721a0463fbd21ef11296fa8`  
		Last Modified: Sat, 01 Feb 2020 18:20:32 GMT  
		Size: 25.8 MB (25775229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
