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
$ docker pull mono@sha256:d5afd60a10e63f09de082a55a8ceb9dd74d68125a807626f5e978c5758531237
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
$ docker pull mono@sha256:a6bd33eaec46ce447d3d114fa7d87c1a161ce421bcd9a615d2e3bd79c1b27179
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218273053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d615e447a74530b87923b510fdf27472388004dc17c20dc13b0efb913b52ef96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:18:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372424f3138cf973f4a1e505b9f65ee657ae72dc6d20e6a766e17371c8ba4be6`  
		Last Modified: Thu, 23 Apr 2020 02:22:31 GMT  
		Size: 140.0 MB (139994638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v5

```console
$ docker pull mono@sha256:b92fa4380bbdb5282ff11a53106859dc68ca724b4e4c16751ac2de07a3ec5589
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3485bf597d69ba7b798696916ea154c10767570f4dfa695791f54cbfcb5c4293`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:34:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88132f5a39438ff62c911032ad21b8909ed25537e3b8ef3bb1d08824305b0908`  
		Last Modified: Thu, 23 Apr 2020 02:39:14 GMT  
		Size: 125.2 MB (125241135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v7

```console
$ docker pull mono@sha256:83f148b6fa446f06d32694c7d0006346c6989a4e2ede04af3823c4cbf78a53e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3772c68cf1fb582a41974eb23929a171ce1a6b8126ceb8c2031a33ac226266fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:03:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aacf3bbf4d9b860afb4fbe44f0f8ad6475f05e85e4eb2ca9c41dfaa554ff65d`  
		Last Modified: Thu, 23 Apr 2020 03:08:26 GMT  
		Size: 123.9 MB (123888451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4d9b9182bc67137e9fa202cbf631c9a7dbd18dd4ec8a7c6b22f8fcdbb3c54da8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187801523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca84f8002627449cf69f3f0acc087bb0bf409a0d80f7891efdd48c83b919fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:09:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371f8bacc29b18ea11bd323d65f7038bd8cad3181ef8df9d884429325b2d11be`  
		Last Modified: Thu, 23 Apr 2020 04:13:28 GMT  
		Size: 139.0 MB (139029342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; ppc64le

```console
$ docker pull mono@sha256:f688dff8fc9e33895b251751347fe7597d84c2313f63514d35d0d05e4007cc02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173291141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db601143a8b2faca7a3938aae178b25f4689ff37a5ca36f081c33749ade1815b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7c2e5ca881a6d1aa59dab96e5c1eaa277da834bf2bcad8c4e395aaf41ff0a`  
		Last Modified: Thu, 23 Apr 2020 02:59:56 GMT  
		Size: 125.6 MB (125621670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20`

```console
$ docker pull mono@sha256:d5afd60a10e63f09de082a55a8ceb9dd74d68125a807626f5e978c5758531237
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
$ docker pull mono@sha256:a6bd33eaec46ce447d3d114fa7d87c1a161ce421bcd9a615d2e3bd79c1b27179
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218273053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d615e447a74530b87923b510fdf27472388004dc17c20dc13b0efb913b52ef96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:18:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372424f3138cf973f4a1e505b9f65ee657ae72dc6d20e6a766e17371c8ba4be6`  
		Last Modified: Thu, 23 Apr 2020 02:22:31 GMT  
		Size: 140.0 MB (139994638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v5

```console
$ docker pull mono@sha256:b92fa4380bbdb5282ff11a53106859dc68ca724b4e4c16751ac2de07a3ec5589
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3485bf597d69ba7b798696916ea154c10767570f4dfa695791f54cbfcb5c4293`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:34:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88132f5a39438ff62c911032ad21b8909ed25537e3b8ef3bb1d08824305b0908`  
		Last Modified: Thu, 23 Apr 2020 02:39:14 GMT  
		Size: 125.2 MB (125241135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm variant v7

```console
$ docker pull mono@sha256:83f148b6fa446f06d32694c7d0006346c6989a4e2ede04af3823c4cbf78a53e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3772c68cf1fb582a41974eb23929a171ce1a6b8126ceb8c2031a33ac226266fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:03:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aacf3bbf4d9b860afb4fbe44f0f8ad6475f05e85e4eb2ca9c41dfaa554ff65d`  
		Last Modified: Thu, 23 Apr 2020 03:08:26 GMT  
		Size: 123.9 MB (123888451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4d9b9182bc67137e9fa202cbf631c9a7dbd18dd4ec8a7c6b22f8fcdbb3c54da8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187801523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca84f8002627449cf69f3f0acc087bb0bf409a0d80f7891efdd48c83b919fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:09:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371f8bacc29b18ea11bd323d65f7038bd8cad3181ef8df9d884429325b2d11be`  
		Last Modified: Thu, 23 Apr 2020 04:13:28 GMT  
		Size: 139.0 MB (139029342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20` - linux; ppc64le

```console
$ docker pull mono@sha256:f688dff8fc9e33895b251751347fe7597d84c2313f63514d35d0d05e4007cc02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173291141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db601143a8b2faca7a3938aae178b25f4689ff37a5ca36f081c33749ade1815b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7c2e5ca881a6d1aa59dab96e5c1eaa277da834bf2bcad8c4e395aaf41ff0a`  
		Last Modified: Thu, 23 Apr 2020 02:59:56 GMT  
		Size: 125.6 MB (125621670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1`

```console
$ docker pull mono@sha256:d5afd60a10e63f09de082a55a8ceb9dd74d68125a807626f5e978c5758531237
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
$ docker pull mono@sha256:a6bd33eaec46ce447d3d114fa7d87c1a161ce421bcd9a615d2e3bd79c1b27179
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218273053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d615e447a74530b87923b510fdf27472388004dc17c20dc13b0efb913b52ef96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:18:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372424f3138cf973f4a1e505b9f65ee657ae72dc6d20e6a766e17371c8ba4be6`  
		Last Modified: Thu, 23 Apr 2020 02:22:31 GMT  
		Size: 140.0 MB (139994638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v5

```console
$ docker pull mono@sha256:b92fa4380bbdb5282ff11a53106859dc68ca724b4e4c16751ac2de07a3ec5589
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3485bf597d69ba7b798696916ea154c10767570f4dfa695791f54cbfcb5c4293`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:34:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88132f5a39438ff62c911032ad21b8909ed25537e3b8ef3bb1d08824305b0908`  
		Last Modified: Thu, 23 Apr 2020 02:39:14 GMT  
		Size: 125.2 MB (125241135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:83f148b6fa446f06d32694c7d0006346c6989a4e2ede04af3823c4cbf78a53e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3772c68cf1fb582a41974eb23929a171ce1a6b8126ceb8c2031a33ac226266fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:03:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aacf3bbf4d9b860afb4fbe44f0f8ad6475f05e85e4eb2ca9c41dfaa554ff65d`  
		Last Modified: Thu, 23 Apr 2020 03:08:26 GMT  
		Size: 123.9 MB (123888451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4d9b9182bc67137e9fa202cbf631c9a7dbd18dd4ec8a7c6b22f8fcdbb3c54da8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187801523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca84f8002627449cf69f3f0acc087bb0bf409a0d80f7891efdd48c83b919fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:09:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371f8bacc29b18ea11bd323d65f7038bd8cad3181ef8df9d884429325b2d11be`  
		Last Modified: Thu, 23 Apr 2020 04:13:28 GMT  
		Size: 139.0 MB (139029342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1` - linux; ppc64le

```console
$ docker pull mono@sha256:f688dff8fc9e33895b251751347fe7597d84c2313f63514d35d0d05e4007cc02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173291141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db601143a8b2faca7a3938aae178b25f4689ff37a5ca36f081c33749ade1815b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7c2e5ca881a6d1aa59dab96e5c1eaa277da834bf2bcad8c4e395aaf41ff0a`  
		Last Modified: Thu, 23 Apr 2020 02:59:56 GMT  
		Size: 125.6 MB (125621670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34`

```console
$ docker pull mono@sha256:d5afd60a10e63f09de082a55a8ceb9dd74d68125a807626f5e978c5758531237
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
$ docker pull mono@sha256:a6bd33eaec46ce447d3d114fa7d87c1a161ce421bcd9a615d2e3bd79c1b27179
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218273053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d615e447a74530b87923b510fdf27472388004dc17c20dc13b0efb913b52ef96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:18:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372424f3138cf973f4a1e505b9f65ee657ae72dc6d20e6a766e17371c8ba4be6`  
		Last Modified: Thu, 23 Apr 2020 02:22:31 GMT  
		Size: 140.0 MB (139994638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v5

```console
$ docker pull mono@sha256:b92fa4380bbdb5282ff11a53106859dc68ca724b4e4c16751ac2de07a3ec5589
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170941707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3485bf597d69ba7b798696916ea154c10767570f4dfa695791f54cbfcb5c4293`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:34:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88132f5a39438ff62c911032ad21b8909ed25537e3b8ef3bb1d08824305b0908`  
		Last Modified: Thu, 23 Apr 2020 02:39:14 GMT  
		Size: 125.2 MB (125241135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm variant v7

```console
$ docker pull mono@sha256:83f148b6fa446f06d32694c7d0006346c6989a4e2ede04af3823c4cbf78a53e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (166993740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3772c68cf1fb582a41974eb23929a171ce1a6b8126ceb8c2031a33ac226266fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:03:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aacf3bbf4d9b860afb4fbe44f0f8ad6475f05e85e4eb2ca9c41dfaa554ff65d`  
		Last Modified: Thu, 23 Apr 2020 03:08:26 GMT  
		Size: 123.9 MB (123888451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4d9b9182bc67137e9fa202cbf631c9a7dbd18dd4ec8a7c6b22f8fcdbb3c54da8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187801523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca84f8002627449cf69f3f0acc087bb0bf409a0d80f7891efdd48c83b919fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:09:03 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371f8bacc29b18ea11bd323d65f7038bd8cad3181ef8df9d884429325b2d11be`  
		Last Modified: Thu, 23 Apr 2020 04:13:28 GMT  
		Size: 139.0 MB (139029342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; 386

```console
$ docker pull mono@sha256:d23260f2eb55831d7a644c2090e68183c31cd94cce445d07f31ad077313cab92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227782164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917877589f53f998a6928fe9997618f6d6fe19a80de19b911e67d5d6ec383707`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:13:57 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdddfacaf4baebf50319e32e2db6159513b09a35b5034627accd2490cded313`  
		Last Modified: Thu, 23 Apr 2020 01:17:45 GMT  
		Size: 145.8 MB (145839739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34` - linux; ppc64le

```console
$ docker pull mono@sha256:f688dff8fc9e33895b251751347fe7597d84c2313f63514d35d0d05e4007cc02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173291141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db601143a8b2faca7a3938aae178b25f4689ff37a5ca36f081c33749ade1815b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:31 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7c2e5ca881a6d1aa59dab96e5c1eaa277da834bf2bcad8c4e395aaf41ff0a`  
		Last Modified: Thu, 23 Apr 2020 02:59:56 GMT  
		Size: 125.6 MB (125621670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1.34-slim`

```console
$ docker pull mono@sha256:fa6b279f88199241362549618d796dd9912969867d5a0bf2e4ea43fb7d229a0d
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
$ docker pull mono@sha256:a67c4cfdbe2cbfd691b5e0506c6d7c3f63e27f09611f7553437ee8be0c1540d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78278415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfd262ac923bb4f9148617aa8498c5ab8c4aa833de4b7c30ea774331686612e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:19a3d3b09e5eb6d420e4dd578717ed988d0cfde7119721560a7162b72ad3c45f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a61466e662903c9784bdbd99011734fc79e1c14aba9697d54035d32d9fed1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:9385888c2179401b8b7d5ba0d9aff97e9aed214a9a8b2a447293a84bdabd168d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc18ef344c27baa9245c921070cf31253a665a6062cc4e36d71dbd52d9c0b473`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:22a8b0345232c248fe0b816669e07aec116dcf92ee519608dc8d305e58d5d468
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d23318e7b6bef7171af3108d17ac10eb52a7874bfee877ddc9c76c0c9728d7a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1.34-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:46c35405cdfbd096c103acc1042707ce96618470e00f9c62be042c919f123914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0d65e296b4107c182521c07104faeddf60ad36361f7cbda2b73443b53e369c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20.1-slim`

```console
$ docker pull mono@sha256:fa6b279f88199241362549618d796dd9912969867d5a0bf2e4ea43fb7d229a0d
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
$ docker pull mono@sha256:a67c4cfdbe2cbfd691b5e0506c6d7c3f63e27f09611f7553437ee8be0c1540d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78278415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfd262ac923bb4f9148617aa8498c5ab8c4aa833de4b7c30ea774331686612e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:19a3d3b09e5eb6d420e4dd578717ed988d0cfde7119721560a7162b72ad3c45f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a61466e662903c9784bdbd99011734fc79e1c14aba9697d54035d32d9fed1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:9385888c2179401b8b7d5ba0d9aff97e9aed214a9a8b2a447293a84bdabd168d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc18ef344c27baa9245c921070cf31253a665a6062cc4e36d71dbd52d9c0b473`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:22a8b0345232c248fe0b816669e07aec116dcf92ee519608dc8d305e58d5d468
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d23318e7b6bef7171af3108d17ac10eb52a7874bfee877ddc9c76c0c9728d7a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20.1-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:46c35405cdfbd096c103acc1042707ce96618470e00f9c62be042c919f123914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0d65e296b4107c182521c07104faeddf60ad36361f7cbda2b73443b53e369c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.20-slim`

```console
$ docker pull mono@sha256:fa6b279f88199241362549618d796dd9912969867d5a0bf2e4ea43fb7d229a0d
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
$ docker pull mono@sha256:a67c4cfdbe2cbfd691b5e0506c6d7c3f63e27f09611f7553437ee8be0c1540d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78278415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfd262ac923bb4f9148617aa8498c5ab8c4aa833de4b7c30ea774331686612e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:19a3d3b09e5eb6d420e4dd578717ed988d0cfde7119721560a7162b72ad3c45f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a61466e662903c9784bdbd99011734fc79e1c14aba9697d54035d32d9fed1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:9385888c2179401b8b7d5ba0d9aff97e9aed214a9a8b2a447293a84bdabd168d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc18ef344c27baa9245c921070cf31253a665a6062cc4e36d71dbd52d9c0b473`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:22a8b0345232c248fe0b816669e07aec116dcf92ee519608dc8d305e58d5d468
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d23318e7b6bef7171af3108d17ac10eb52a7874bfee877ddc9c76c0c9728d7a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.20-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:46c35405cdfbd096c103acc1042707ce96618470e00f9c62be042c919f123914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0d65e296b4107c182521c07104faeddf60ad36361f7cbda2b73443b53e369c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5-slim`

```console
$ docker pull mono@sha256:fa6b279f88199241362549618d796dd9912969867d5a0bf2e4ea43fb7d229a0d
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
$ docker pull mono@sha256:a67c4cfdbe2cbfd691b5e0506c6d7c3f63e27f09611f7553437ee8be0c1540d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78278415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfd262ac923bb4f9148617aa8498c5ab8c4aa833de4b7c30ea774331686612e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:50:05 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:50:43 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a90fcd30243429ccde1f9410482825b3cf605a11a43283d700d5d0d2c19d`  
		Last Modified: Thu, 23 Apr 2020 02:19:53 GMT  
		Size: 244.5 KB (244486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60b582667e2deb99365fcd66c622deb3a30e7320b51aa6bed522cc774124d2`  
		Last Modified: Thu, 23 Apr 2020 02:20:08 GMT  
		Size: 55.5 MB (55520441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:19a3d3b09e5eb6d420e4dd578717ed988d0cfde7119721560a7162b72ad3c45f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45700572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a61466e662903c9784bdbd99011734fc79e1c14aba9697d54035d32d9fed1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:12:18 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:13:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:24:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8545a6480f9d5ada3bb6fd047fb63d967f20535d293f5919a1f8e7849a6861`  
		Last Modified: Thu, 23 Apr 2020 02:36:03 GMT  
		Size: 244.6 KB (244561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2270ff6022f304e7408415d101d4c6377db331ff658336956e8a47f2ea956e`  
		Last Modified: Thu, 23 Apr 2020 02:36:12 GMT  
		Size: 24.3 MB (24265165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:9385888c2179401b8b7d5ba0d9aff97e9aed214a9a8b2a447293a84bdabd168d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc18ef344c27baa9245c921070cf31253a665a6062cc4e36d71dbd52d9c0b473`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:52:43 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:53:05 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:53:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd31ab9d840645c8263c147bb25abc2cfa231de9f8b633f113c3fa3385037578`  
		Last Modified: Thu, 23 Apr 2020 03:05:03 GMT  
		Size: 244.6 KB (244595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed761a6b0ccaf8955cbc766f5c9279960c64189fb32b68804de040529f0963d`  
		Last Modified: Thu, 23 Apr 2020 03:05:12 GMT  
		Size: 23.6 MB (23562231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:22a8b0345232c248fe0b816669e07aec116dcf92ee519608dc8d305e58d5d468
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d23318e7b6bef7171af3108d17ac10eb52a7874bfee877ddc9c76c0c9728d7a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:57 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 04:00:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 04:01:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbabe46ceb0d671299103f7bcfbb1a4fcf779de2d88738f747a7b88fcdd84f4d`  
		Last Modified: Thu, 23 Apr 2020 04:10:21 GMT  
		Size: 244.4 KB (244392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72e6421be369b93138740dae6343512e7feb2f7b1ce7873198afad2df44fac`  
		Last Modified: Thu, 23 Apr 2020 04:10:28 GMT  
		Size: 28.2 MB (28157696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; 386

```console
$ docker pull mono@sha256:f298a5136fcc732fb7f7c1b06514978d91489ec0402751f79366829250420a41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81942425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471b379bc228d2d7acf3bf17250d5dc21bc3475d42956005eef5b84e23100b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:06:02 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 01:06:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:06:47 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f99a2ee486012fc5349a1f2fc838b03077a9aa47e79c414bc5af7e6be55d0ac`  
		Last Modified: Thu, 23 Apr 2020 01:15:02 GMT  
		Size: 244.5 KB (244504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3666eed20e513a6d57a046805936faf49f4e8af6f172fefa71261014ee05c479`  
		Last Modified: Thu, 23 Apr 2020 01:15:18 GMT  
		Size: 58.6 MB (58556498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:46c35405cdfbd096c103acc1042707ce96618470e00f9c62be042c919f123914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47669471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0d65e296b4107c182521c07104faeddf60ad36361f7cbda2b73443b53e369c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:36:13 GMT
ENV MONO_VERSION=5.20.1.34
# Thu, 23 Apr 2020 02:37:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:38:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb818e1907f5fd0c1afe14f17f1897068b59037a3e9b938a510b05648bd5e`  
		Last Modified: Thu, 23 Apr 2020 02:57:41 GMT  
		Size: 244.6 KB (244626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b17db901e0fb99bb4c584f681099a659c9a66b475063c2fd797590901b91d0b`  
		Last Modified: Thu, 23 Apr 2020 02:57:47 GMT  
		Size: 24.6 MB (24639440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6`

```console
$ docker pull mono@sha256:5369341c2c163d02bbd085644993ecc35d7366385ea36fd97130ceea5ed3872e
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
$ docker pull mono@sha256:2351a2ba6c2228ecac8696680f65e49607432bb7fd6c0494fd254060c48f6a02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235136555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59599093bfc20b4291b6019e7cd8bd648dab8dc3c341bc26001f807264ac44dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:59:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e83f8e35ba5681f2772165e09a403fab75e2cb54d9c6166e85301ad905d258`  
		Last Modified: Thu, 23 Apr 2020 02:20:55 GMT  
		Size: 147.8 MB (147794220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:638eb478bc2d77761637d3c38bdd315feca956bb670fe7a57de4cc35cb6c7215
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbdf0b0401ab5130c35b7db945960e55082c3ab6023657188752ec82f91cae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:27:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3f3bb75c812ff1a60644fe7dce9fbed58cd4578c80f3e37b9714f26987ed2`  
		Last Modified: Thu, 23 Apr 2020 02:37:17 GMT  
		Size: 129.9 MB (129892151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:c874c01c6f92382c5cec60d09cc395518c556217595e4c806afb22d672d3e45c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e196d31d2f638e7440ab21cfc4440afb3d32e9e49ee3ea6698a7331936ea0ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2fcd3e55989df99fa1643abe68ef9911caf777caf659f98a9672df51bab1`  
		Last Modified: Thu, 23 Apr 2020 03:06:12 GMT  
		Size: 128.6 MB (128556011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2c4a103ab7827cd92c451d3eb273403a21172601e646618353670b5bc9c11d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9689c7b697340040a0333ddb72fe3f1026947a0fd9aafd57a27eead437208c5d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:03:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e858c5d0189c31dc4dd9dfe8546a68dfb734613feaf85697642b6b0798f08`  
		Last Modified: Thu, 23 Apr 2020 04:11:28 GMT  
		Size: 144.7 MB (144712974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:c872e3bb21f26535dfc38f43e7e622be64e67b77e2c05818d04390929a2b7227
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178995140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25acb6d4e7f1006ab9ff7f6d82a649bf9ee795479e883b74dd7e66e21cb07a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f154d5f25d2332d3ea9f8ebb837c6f0156ffe8f2420773f3907230be4b2b85`  
		Last Modified: Thu, 23 Apr 2020 02:58:31 GMT  
		Size: 130.2 MB (130190019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6`

```console
$ docker pull mono@sha256:3d7933d3c9e37695a67161b053ed13a600afb6f0f3a523a5338dd7d2540400b8
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
$ docker pull mono@sha256:3ea2f2740b1f0ff78b3a90eb8ff531a9763c181158b7c329f97ea04e8d213dec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233037465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53213d4543a9b55852762487dcc6eca75d1a42efa19c79750579e082c5a2b536`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:10 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:49:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:49:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:08:52 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f7d13fbf11ea37b0afce7d19a2618fdef52ce09eeed3be5d6c2cba3ff89bc`  
		Last Modified: Thu, 23 Apr 2020 02:19:31 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4778f199830e07df7630da3469e683d4db678333a3b3d661eaadaf4866f90`  
		Last Modified: Thu, 23 Apr 2020 02:19:48 GMT  
		Size: 63.0 MB (62971564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309b0c95463c87a0e326685c37fc42adbe87d5e1da3032cd92d8e56c50c6440`  
		Last Modified: Thu, 23 Apr 2020 02:21:38 GMT  
		Size: 147.3 MB (147307935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v5

```console
$ docker pull mono@sha256:346625f2f1599311a65692b143be30807bbf79175b391ac3511ee7ef4c1f2260
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd97f5816d94cbf04f56d74d8e1491bba02e8a64282226afc81fc2980892455`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:45 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:11:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:12:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:31:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09679394a81018547ba09b984030af4f9b67cad71e45f1c68f9bff20e5cf4271`  
		Last Modified: Thu, 23 Apr 2020 02:35:43 GMT  
		Size: 244.6 KB (244576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9460908a68c0df86289e96c31e664d653d5f320efeb5a2a2d614a9344732dd`  
		Last Modified: Thu, 23 Apr 2020 02:35:52 GMT  
		Size: 25.4 MB (25415299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562de89bf9baebf1c50f3d80c43d557090a7847c2c945afd9aba052ab2483c06`  
		Last Modified: Thu, 23 Apr 2020 02:38:19 GMT  
		Size: 129.6 MB (129648926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm variant v7

```console
$ docker pull mono@sha256:fd9dca9050865f7a3e5a4a15e3c524eb91faa48e100db1bac0b09c55b0409347
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172507724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e0befeda8b8c6fbb4b10f73bc00a74ed37df8970955f737f8c0687b8c1de35`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:51:24 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:51:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:52:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:00:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092abc720fccf8c8741a6a05b645345539a17504f0b8ee8a8c61d62acac51a74`  
		Last Modified: Thu, 23 Apr 2020 03:04:43 GMT  
		Size: 244.6 KB (244606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac0d8819b7a78b917c7978fbb485db1ac5b2f3e0b87172a542b077871dba7d`  
		Last Modified: Thu, 23 Apr 2020 03:04:52 GMT  
		Size: 24.6 MB (24648603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8e1c616d172de493250a6de4c2873028491050826b134f05fab25c435d784`  
		Last Modified: Thu, 23 Apr 2020 03:07:31 GMT  
		Size: 128.3 MB (128316052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:2c173ce6282c9cde0bf8730c2cce0e4bcf18942af2b813761162bdd41d33eb60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb80b96f2cb3ffec87831cc585f2988e7087c667c9917bbd2e030870774e20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:58:38 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 03:58:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:06:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a613c1e437bd181cec840599438a9cafe1261ef24174c4d6cdc45068e521bf`  
		Last Modified: Thu, 23 Apr 2020 04:09:56 GMT  
		Size: 244.4 KB (244383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30965877704d115035d3df32eedac7ff9b25fcc6479c6abfb6dbd6f8b2cebc11`  
		Last Modified: Thu, 23 Apr 2020 04:10:07 GMT  
		Size: 29.4 MB (29438489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230e19a390f97576129e6dbffe1727c17fc580370ca59de7cf8c6d6e259c763d`  
		Last Modified: Thu, 23 Apr 2020 04:12:30 GMT  
		Size: 144.3 MB (144341467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; 386

```console
$ docker pull mono@sha256:94e58f1ce29ecb43527eb823856f0434fa0d3a0812ecc31df88f0e9d2e1c3eb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241294092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5575a49e77c965605a2abaa50aa38f2aa1668e66c41a766b116df708ca2d2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:11:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb378b781be2a120cd2fa519211a18f9a67e6bd23b8442b3ae140570f8371226`  
		Last Modified: Thu, 23 Apr 2020 01:16:57 GMT  
		Size: 151.2 MB (151160722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6` - linux; ppc64le

```console
$ docker pull mono@sha256:97fdf52452fdab1fad4756d7693629dd306191088c8a7b1c41195b0487ebd93d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178798621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c255ece3b37ada62d9b920bd4ddbd290bd463ffde67b1aaf61cf63af07c17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:33:46 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:34:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:35:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe41c226541af3bbd0797b5d3f53fa7f8979c19ce96676209666c0d5b1c2e`  
		Last Modified: Thu, 23 Apr 2020 02:57:21 GMT  
		Size: 244.5 KB (244522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25177009e07c7ce1a7798a6d0f9cad7334ba19e40d0c812a3d0c56c8c89784`  
		Last Modified: Thu, 23 Apr 2020 02:57:28 GMT  
		Size: 25.8 MB (25828002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8dce84e2a00b41e57e946d61e258b3da040ba7a16b28c2f14e230cacdf0716`  
		Last Modified: Thu, 23 Apr 2020 02:59:16 GMT  
		Size: 129.9 MB (129940692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0`

```console
$ docker pull mono@sha256:3d7933d3c9e37695a67161b053ed13a600afb6f0f3a523a5338dd7d2540400b8
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
$ docker pull mono@sha256:3ea2f2740b1f0ff78b3a90eb8ff531a9763c181158b7c329f97ea04e8d213dec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233037465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53213d4543a9b55852762487dcc6eca75d1a42efa19c79750579e082c5a2b536`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:10 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:49:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:49:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:08:52 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f7d13fbf11ea37b0afce7d19a2618fdef52ce09eeed3be5d6c2cba3ff89bc`  
		Last Modified: Thu, 23 Apr 2020 02:19:31 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4778f199830e07df7630da3469e683d4db678333a3b3d661eaadaf4866f90`  
		Last Modified: Thu, 23 Apr 2020 02:19:48 GMT  
		Size: 63.0 MB (62971564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309b0c95463c87a0e326685c37fc42adbe87d5e1da3032cd92d8e56c50c6440`  
		Last Modified: Thu, 23 Apr 2020 02:21:38 GMT  
		Size: 147.3 MB (147307935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:346625f2f1599311a65692b143be30807bbf79175b391ac3511ee7ef4c1f2260
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd97f5816d94cbf04f56d74d8e1491bba02e8a64282226afc81fc2980892455`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:45 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:11:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:12:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:31:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09679394a81018547ba09b984030af4f9b67cad71e45f1c68f9bff20e5cf4271`  
		Last Modified: Thu, 23 Apr 2020 02:35:43 GMT  
		Size: 244.6 KB (244576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9460908a68c0df86289e96c31e664d653d5f320efeb5a2a2d614a9344732dd`  
		Last Modified: Thu, 23 Apr 2020 02:35:52 GMT  
		Size: 25.4 MB (25415299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562de89bf9baebf1c50f3d80c43d557090a7847c2c945afd9aba052ab2483c06`  
		Last Modified: Thu, 23 Apr 2020 02:38:19 GMT  
		Size: 129.6 MB (129648926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:fd9dca9050865f7a3e5a4a15e3c524eb91faa48e100db1bac0b09c55b0409347
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172507724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e0befeda8b8c6fbb4b10f73bc00a74ed37df8970955f737f8c0687b8c1de35`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:51:24 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:51:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:52:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:00:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092abc720fccf8c8741a6a05b645345539a17504f0b8ee8a8c61d62acac51a74`  
		Last Modified: Thu, 23 Apr 2020 03:04:43 GMT  
		Size: 244.6 KB (244606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac0d8819b7a78b917c7978fbb485db1ac5b2f3e0b87172a542b077871dba7d`  
		Last Modified: Thu, 23 Apr 2020 03:04:52 GMT  
		Size: 24.6 MB (24648603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8e1c616d172de493250a6de4c2873028491050826b134f05fab25c435d784`  
		Last Modified: Thu, 23 Apr 2020 03:07:31 GMT  
		Size: 128.3 MB (128316052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:2c173ce6282c9cde0bf8730c2cce0e4bcf18942af2b813761162bdd41d33eb60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb80b96f2cb3ffec87831cc585f2988e7087c667c9917bbd2e030870774e20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:58:38 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 03:58:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:06:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a613c1e437bd181cec840599438a9cafe1261ef24174c4d6cdc45068e521bf`  
		Last Modified: Thu, 23 Apr 2020 04:09:56 GMT  
		Size: 244.4 KB (244383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30965877704d115035d3df32eedac7ff9b25fcc6479c6abfb6dbd6f8b2cebc11`  
		Last Modified: Thu, 23 Apr 2020 04:10:07 GMT  
		Size: 29.4 MB (29438489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230e19a390f97576129e6dbffe1727c17fc580370ca59de7cf8c6d6e259c763d`  
		Last Modified: Thu, 23 Apr 2020 04:12:30 GMT  
		Size: 144.3 MB (144341467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; 386

```console
$ docker pull mono@sha256:94e58f1ce29ecb43527eb823856f0434fa0d3a0812ecc31df88f0e9d2e1c3eb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241294092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5575a49e77c965605a2abaa50aa38f2aa1668e66c41a766b116df708ca2d2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:11:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb378b781be2a120cd2fa519211a18f9a67e6bd23b8442b3ae140570f8371226`  
		Last Modified: Thu, 23 Apr 2020 01:16:57 GMT  
		Size: 151.2 MB (151160722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0` - linux; ppc64le

```console
$ docker pull mono@sha256:97fdf52452fdab1fad4756d7693629dd306191088c8a7b1c41195b0487ebd93d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178798621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c255ece3b37ada62d9b920bd4ddbd290bd463ffde67b1aaf61cf63af07c17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:33:46 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:34:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:35:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe41c226541af3bbd0797b5d3f53fa7f8979c19ce96676209666c0d5b1c2e`  
		Last Modified: Thu, 23 Apr 2020 02:57:21 GMT  
		Size: 244.5 KB (244522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25177009e07c7ce1a7798a6d0f9cad7334ba19e40d0c812a3d0c56c8c89784`  
		Last Modified: Thu, 23 Apr 2020 02:57:28 GMT  
		Size: 25.8 MB (25828002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8dce84e2a00b41e57e946d61e258b3da040ba7a16b28c2f14e230cacdf0716`  
		Last Modified: Thu, 23 Apr 2020 02:59:16 GMT  
		Size: 129.9 MB (129940692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161`

```console
$ docker pull mono@sha256:3d7933d3c9e37695a67161b053ed13a600afb6f0f3a523a5338dd7d2540400b8
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
$ docker pull mono@sha256:3ea2f2740b1f0ff78b3a90eb8ff531a9763c181158b7c329f97ea04e8d213dec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233037465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53213d4543a9b55852762487dcc6eca75d1a42efa19c79750579e082c5a2b536`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:10 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:49:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:49:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:08:52 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f7d13fbf11ea37b0afce7d19a2618fdef52ce09eeed3be5d6c2cba3ff89bc`  
		Last Modified: Thu, 23 Apr 2020 02:19:31 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4778f199830e07df7630da3469e683d4db678333a3b3d661eaadaf4866f90`  
		Last Modified: Thu, 23 Apr 2020 02:19:48 GMT  
		Size: 63.0 MB (62971564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8309b0c95463c87a0e326685c37fc42adbe87d5e1da3032cd92d8e56c50c6440`  
		Last Modified: Thu, 23 Apr 2020 02:21:38 GMT  
		Size: 147.3 MB (147307935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v5

```console
$ docker pull mono@sha256:346625f2f1599311a65692b143be30807bbf79175b391ac3511ee7ef4c1f2260
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd97f5816d94cbf04f56d74d8e1491bba02e8a64282226afc81fc2980892455`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:45 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:11:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:12:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:31:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09679394a81018547ba09b984030af4f9b67cad71e45f1c68f9bff20e5cf4271`  
		Last Modified: Thu, 23 Apr 2020 02:35:43 GMT  
		Size: 244.6 KB (244576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9460908a68c0df86289e96c31e664d653d5f320efeb5a2a2d614a9344732dd`  
		Last Modified: Thu, 23 Apr 2020 02:35:52 GMT  
		Size: 25.4 MB (25415299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562de89bf9baebf1c50f3d80c43d557090a7847c2c945afd9aba052ab2483c06`  
		Last Modified: Thu, 23 Apr 2020 02:38:19 GMT  
		Size: 129.6 MB (129648926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm variant v7

```console
$ docker pull mono@sha256:fd9dca9050865f7a3e5a4a15e3c524eb91faa48e100db1bac0b09c55b0409347
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172507724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e0befeda8b8c6fbb4b10f73bc00a74ed37df8970955f737f8c0687b8c1de35`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:51:24 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:51:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:52:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 03:00:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092abc720fccf8c8741a6a05b645345539a17504f0b8ee8a8c61d62acac51a74`  
		Last Modified: Thu, 23 Apr 2020 03:04:43 GMT  
		Size: 244.6 KB (244606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac0d8819b7a78b917c7978fbb485db1ac5b2f3e0b87172a542b077871dba7d`  
		Last Modified: Thu, 23 Apr 2020 03:04:52 GMT  
		Size: 24.6 MB (24648603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8e1c616d172de493250a6de4c2873028491050826b134f05fab25c435d784`  
		Last Modified: Thu, 23 Apr 2020 03:07:31 GMT  
		Size: 128.3 MB (128316052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:2c173ce6282c9cde0bf8730c2cce0e4bcf18942af2b813761162bdd41d33eb60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194394432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb80b96f2cb3ffec87831cc585f2988e7087c667c9917bbd2e030870774e20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:58:38 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 03:58:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:06:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a613c1e437bd181cec840599438a9cafe1261ef24174c4d6cdc45068e521bf`  
		Last Modified: Thu, 23 Apr 2020 04:09:56 GMT  
		Size: 244.4 KB (244383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30965877704d115035d3df32eedac7ff9b25fcc6479c6abfb6dbd6f8b2cebc11`  
		Last Modified: Thu, 23 Apr 2020 04:10:07 GMT  
		Size: 29.4 MB (29438489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230e19a390f97576129e6dbffe1727c17fc580370ca59de7cf8c6d6e259c763d`  
		Last Modified: Thu, 23 Apr 2020 04:12:30 GMT  
		Size: 144.3 MB (144341467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; 386

```console
$ docker pull mono@sha256:94e58f1ce29ecb43527eb823856f0434fa0d3a0812ecc31df88f0e9d2e1c3eb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241294092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5575a49e77c965605a2abaa50aa38f2aa1668e66c41a766b116df708ca2d2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:11:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb378b781be2a120cd2fa519211a18f9a67e6bd23b8442b3ae140570f8371226`  
		Last Modified: Thu, 23 Apr 2020 01:16:57 GMT  
		Size: 151.2 MB (151160722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161` - linux; ppc64le

```console
$ docker pull mono@sha256:97fdf52452fdab1fad4756d7693629dd306191088c8a7b1c41195b0487ebd93d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178798621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c255ece3b37ada62d9b920bd4ddbd290bd463ffde67b1aaf61cf63af07c17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:33:46 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:34:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:35:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:50:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe41c226541af3bbd0797b5d3f53fa7f8979c19ce96676209666c0d5b1c2e`  
		Last Modified: Thu, 23 Apr 2020 02:57:21 GMT  
		Size: 244.5 KB (244522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25177009e07c7ce1a7798a6d0f9cad7334ba19e40d0c812a3d0c56c8c89784`  
		Last Modified: Thu, 23 Apr 2020 02:57:28 GMT  
		Size: 25.8 MB (25828002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8dce84e2a00b41e57e946d61e258b3da040ba7a16b28c2f14e230cacdf0716`  
		Last Modified: Thu, 23 Apr 2020 02:59:16 GMT  
		Size: 129.9 MB (129940692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0.161-slim`

```console
$ docker pull mono@sha256:915bc54e25778a4ed37ea8df5056108286a87dc98120026bc3b89c80c5ddb56b
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
$ docker pull mono@sha256:e03c444502022dd73573d892596a6bb4cab789a4f66a61e9ee6dffd8ff9ef1c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85729530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa672f39c92e71df557f447a2ab1ebfcf309747e3f6f883f2ccf571ac14d999`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:10 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:49:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:49:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f7d13fbf11ea37b0afce7d19a2618fdef52ce09eeed3be5d6c2cba3ff89bc`  
		Last Modified: Thu, 23 Apr 2020 02:19:31 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4778f199830e07df7630da3469e683d4db678333a3b3d661eaadaf4866f90`  
		Last Modified: Thu, 23 Apr 2020 02:19:48 GMT  
		Size: 63.0 MB (62971564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c7906036c3817541ff4c781b5e8059548a816543c14e439af57ac39f71c61f96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c649e27d8abfb6b20f45b5a41695200bb6b3c5a38580ce3d958dfc212051dd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:45 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:11:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:12:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09679394a81018547ba09b984030af4f9b67cad71e45f1c68f9bff20e5cf4271`  
		Last Modified: Thu, 23 Apr 2020 02:35:43 GMT  
		Size: 244.6 KB (244576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9460908a68c0df86289e96c31e664d653d5f320efeb5a2a2d614a9344732dd`  
		Last Modified: Thu, 23 Apr 2020 02:35:52 GMT  
		Size: 25.4 MB (25415299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d3f183994e69eba1204884688522c3d3bebca8e94804080e6479d971c904bce5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762d9a1a8423b45bcb6c922ce7ecd33c6b7d93bcfed7466fde4b48e011de3c88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:51:24 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:51:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:52:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092abc720fccf8c8741a6a05b645345539a17504f0b8ee8a8c61d62acac51a74`  
		Last Modified: Thu, 23 Apr 2020 03:04:43 GMT  
		Size: 244.6 KB (244606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac0d8819b7a78b917c7978fbb485db1ac5b2f3e0b87172a542b077871dba7d`  
		Last Modified: Thu, 23 Apr 2020 03:04:52 GMT  
		Size: 24.6 MB (24648603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:69ee0edafc4eb0d75f27f75a0870e798abf17be5c7b386cfdbb5820d9cdb6643
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50052965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169d747ff6f91f9062e2ac693e9d33d9e722d97aa30a1efd2f837f74585844ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:58:38 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 03:58:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a613c1e437bd181cec840599438a9cafe1261ef24174c4d6cdc45068e521bf`  
		Last Modified: Thu, 23 Apr 2020 04:09:56 GMT  
		Size: 244.4 KB (244383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30965877704d115035d3df32eedac7ff9b25fcc6479c6abfb6dbd6f8b2cebc11`  
		Last Modified: Thu, 23 Apr 2020 04:10:07 GMT  
		Size: 29.4 MB (29438489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; 386

```console
$ docker pull mono@sha256:a0ac6b4bdd3d9afea4096b59694f0b606472414433c3d035705aed0080cfe308
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90133370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d67cb1f0471d746abc265542e8168ced8da1ff1614c4118e963641dd9629f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0.161-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:157399d581bf6c3c455a8ed804974f9f5d977135e910c9e8630d85dab98987d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48857929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5b0ef5361e4d9b104a8a68582e1c664b948c0d9379611f1d2562b47726892`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:33:46 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:34:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:35:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe41c226541af3bbd0797b5d3f53fa7f8979c19ce96676209666c0d5b1c2e`  
		Last Modified: Thu, 23 Apr 2020 02:57:21 GMT  
		Size: 244.5 KB (244522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25177009e07c7ce1a7798a6d0f9cad7334ba19e40d0c812a3d0c56c8c89784`  
		Last Modified: Thu, 23 Apr 2020 02:57:28 GMT  
		Size: 25.8 MB (25828002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6.0-slim`

```console
$ docker pull mono@sha256:915bc54e25778a4ed37ea8df5056108286a87dc98120026bc3b89c80c5ddb56b
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
$ docker pull mono@sha256:e03c444502022dd73573d892596a6bb4cab789a4f66a61e9ee6dffd8ff9ef1c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85729530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa672f39c92e71df557f447a2ab1ebfcf309747e3f6f883f2ccf571ac14d999`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:10 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:49:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:49:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f7d13fbf11ea37b0afce7d19a2618fdef52ce09eeed3be5d6c2cba3ff89bc`  
		Last Modified: Thu, 23 Apr 2020 02:19:31 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4778f199830e07df7630da3469e683d4db678333a3b3d661eaadaf4866f90`  
		Last Modified: Thu, 23 Apr 2020 02:19:48 GMT  
		Size: 63.0 MB (62971564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c7906036c3817541ff4c781b5e8059548a816543c14e439af57ac39f71c61f96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c649e27d8abfb6b20f45b5a41695200bb6b3c5a38580ce3d958dfc212051dd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:45 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:11:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:12:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09679394a81018547ba09b984030af4f9b67cad71e45f1c68f9bff20e5cf4271`  
		Last Modified: Thu, 23 Apr 2020 02:35:43 GMT  
		Size: 244.6 KB (244576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9460908a68c0df86289e96c31e664d653d5f320efeb5a2a2d614a9344732dd`  
		Last Modified: Thu, 23 Apr 2020 02:35:52 GMT  
		Size: 25.4 MB (25415299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d3f183994e69eba1204884688522c3d3bebca8e94804080e6479d971c904bce5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762d9a1a8423b45bcb6c922ce7ecd33c6b7d93bcfed7466fde4b48e011de3c88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:51:24 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:51:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:52:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092abc720fccf8c8741a6a05b645345539a17504f0b8ee8a8c61d62acac51a74`  
		Last Modified: Thu, 23 Apr 2020 03:04:43 GMT  
		Size: 244.6 KB (244606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac0d8819b7a78b917c7978fbb485db1ac5b2f3e0b87172a542b077871dba7d`  
		Last Modified: Thu, 23 Apr 2020 03:04:52 GMT  
		Size: 24.6 MB (24648603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:69ee0edafc4eb0d75f27f75a0870e798abf17be5c7b386cfdbb5820d9cdb6643
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50052965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169d747ff6f91f9062e2ac693e9d33d9e722d97aa30a1efd2f837f74585844ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:58:38 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 03:58:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a613c1e437bd181cec840599438a9cafe1261ef24174c4d6cdc45068e521bf`  
		Last Modified: Thu, 23 Apr 2020 04:09:56 GMT  
		Size: 244.4 KB (244383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30965877704d115035d3df32eedac7ff9b25fcc6479c6abfb6dbd6f8b2cebc11`  
		Last Modified: Thu, 23 Apr 2020 04:10:07 GMT  
		Size: 29.4 MB (29438489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; 386

```console
$ docker pull mono@sha256:a0ac6b4bdd3d9afea4096b59694f0b606472414433c3d035705aed0080cfe308
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90133370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d67cb1f0471d746abc265542e8168ced8da1ff1614c4118e963641dd9629f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:157399d581bf6c3c455a8ed804974f9f5d977135e910c9e8630d85dab98987d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48857929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5b0ef5361e4d9b104a8a68582e1c664b948c0d9379611f1d2562b47726892`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:33:46 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:34:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:35:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe41c226541af3bbd0797b5d3f53fa7f8979c19ce96676209666c0d5b1c2e`  
		Last Modified: Thu, 23 Apr 2020 02:57:21 GMT  
		Size: 244.5 KB (244522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25177009e07c7ce1a7798a6d0f9cad7334ba19e40d0c812a3d0c56c8c89784`  
		Last Modified: Thu, 23 Apr 2020 02:57:28 GMT  
		Size: 25.8 MB (25828002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.6-slim`

```console
$ docker pull mono@sha256:915bc54e25778a4ed37ea8df5056108286a87dc98120026bc3b89c80c5ddb56b
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
$ docker pull mono@sha256:e03c444502022dd73573d892596a6bb4cab789a4f66a61e9ee6dffd8ff9ef1c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85729530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa672f39c92e71df557f447a2ab1ebfcf309747e3f6f883f2ccf571ac14d999`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:10 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:49:21 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:49:54 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485f7d13fbf11ea37b0afce7d19a2618fdef52ce09eeed3be5d6c2cba3ff89bc`  
		Last Modified: Thu, 23 Apr 2020 02:19:31 GMT  
		Size: 244.5 KB (244478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a4778f199830e07df7630da3469e683d4db678333a3b3d661eaadaf4866f90`  
		Last Modified: Thu, 23 Apr 2020 02:19:48 GMT  
		Size: 63.0 MB (62971564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c7906036c3817541ff4c781b5e8059548a816543c14e439af57ac39f71c61f96
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46850721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c649e27d8abfb6b20f45b5a41695200bb6b3c5a38580ce3d958dfc212051dd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:10:45 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:11:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:12:06 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09679394a81018547ba09b984030af4f9b67cad71e45f1c68f9bff20e5cf4271`  
		Last Modified: Thu, 23 Apr 2020 02:35:43 GMT  
		Size: 244.6 KB (244576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9460908a68c0df86289e96c31e664d653d5f320efeb5a2a2d614a9344732dd`  
		Last Modified: Thu, 23 Apr 2020 02:35:52 GMT  
		Size: 25.4 MB (25415299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:d3f183994e69eba1204884688522c3d3bebca8e94804080e6479d971c904bce5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762d9a1a8423b45bcb6c922ce7ecd33c6b7d93bcfed7466fde4b48e011de3c88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:51:24 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:51:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:52:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092abc720fccf8c8741a6a05b645345539a17504f0b8ee8a8c61d62acac51a74`  
		Last Modified: Thu, 23 Apr 2020 03:04:43 GMT  
		Size: 244.6 KB (244606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac0d8819b7a78b917c7978fbb485db1ac5b2f3e0b87172a542b077871dba7d`  
		Last Modified: Thu, 23 Apr 2020 03:04:52 GMT  
		Size: 24.6 MB (24648603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:69ee0edafc4eb0d75f27f75a0870e798abf17be5c7b386cfdbb5820d9cdb6643
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50052965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169d747ff6f91f9062e2ac693e9d33d9e722d97aa30a1efd2f837f74585844ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:58:38 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 03:58:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a613c1e437bd181cec840599438a9cafe1261ef24174c4d6cdc45068e521bf`  
		Last Modified: Thu, 23 Apr 2020 04:09:56 GMT  
		Size: 244.4 KB (244383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30965877704d115035d3df32eedac7ff9b25fcc6479c6abfb6dbd6f8b2cebc11`  
		Last Modified: Thu, 23 Apr 2020 04:10:07 GMT  
		Size: 29.4 MB (29438489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; 386

```console
$ docker pull mono@sha256:a0ac6b4bdd3d9afea4096b59694f0b606472414433c3d035705aed0080cfe308
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90133370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d67cb1f0471d746abc265542e8168ced8da1ff1614c4118e963641dd9629f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:05:07 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 01:05:17 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beb89e4f0bd2e26a4512b29f2528cda17c529914331e656630af13f14143f8`  
		Last Modified: Thu, 23 Apr 2020 01:14:38 GMT  
		Size: 244.5 KB (244501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70df528f46cab25e9c07e896d643cac9c7968e0e534e9d4702c3645865f689b`  
		Last Modified: Thu, 23 Apr 2020 01:14:55 GMT  
		Size: 66.7 MB (66747446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:157399d581bf6c3c455a8ed804974f9f5d977135e910c9e8630d85dab98987d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48857929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead5b0ef5361e4d9b104a8a68582e1c664b948c0d9379611f1d2562b47726892`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:33:46 GMT
ENV MONO_VERSION=6.6.0.161
# Thu, 23 Apr 2020 02:34:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:35:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe41c226541af3bbd0797b5d3f53fa7f8979c19ce96676209666c0d5b1c2e`  
		Last Modified: Thu, 23 Apr 2020 02:57:21 GMT  
		Size: 244.5 KB (244522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25177009e07c7ce1a7798a6d0f9cad7334ba19e40d0c812a3d0c56c8c89784`  
		Last Modified: Thu, 23 Apr 2020 02:57:28 GMT  
		Size: 25.8 MB (25828002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8`

```console
$ docker pull mono@sha256:5369341c2c163d02bbd085644993ecc35d7366385ea36fd97130ceea5ed3872e
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
$ docker pull mono@sha256:2351a2ba6c2228ecac8696680f65e49607432bb7fd6c0494fd254060c48f6a02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235136555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59599093bfc20b4291b6019e7cd8bd648dab8dc3c341bc26001f807264ac44dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:59:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e83f8e35ba5681f2772165e09a403fab75e2cb54d9c6166e85301ad905d258`  
		Last Modified: Thu, 23 Apr 2020 02:20:55 GMT  
		Size: 147.8 MB (147794220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v5

```console
$ docker pull mono@sha256:638eb478bc2d77761637d3c38bdd315feca956bb670fe7a57de4cc35cb6c7215
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbdf0b0401ab5130c35b7db945960e55082c3ab6023657188752ec82f91cae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:27:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3f3bb75c812ff1a60644fe7dce9fbed58cd4578c80f3e37b9714f26987ed2`  
		Last Modified: Thu, 23 Apr 2020 02:37:17 GMT  
		Size: 129.9 MB (129892151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:c874c01c6f92382c5cec60d09cc395518c556217595e4c806afb22d672d3e45c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e196d31d2f638e7440ab21cfc4440afb3d32e9e49ee3ea6698a7331936ea0ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2fcd3e55989df99fa1643abe68ef9911caf777caf659f98a9672df51bab1`  
		Last Modified: Thu, 23 Apr 2020 03:06:12 GMT  
		Size: 128.6 MB (128556011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2c4a103ab7827cd92c451d3eb273403a21172601e646618353670b5bc9c11d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9689c7b697340040a0333ddb72fe3f1026947a0fd9aafd57a27eead437208c5d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:03:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e858c5d0189c31dc4dd9dfe8546a68dfb734613feaf85697642b6b0798f08`  
		Last Modified: Thu, 23 Apr 2020 04:11:28 GMT  
		Size: 144.7 MB (144712974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8` - linux; ppc64le

```console
$ docker pull mono@sha256:c872e3bb21f26535dfc38f43e7e622be64e67b77e2c05818d04390929a2b7227
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178995140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25acb6d4e7f1006ab9ff7f6d82a649bf9ee795479e883b74dd7e66e21cb07a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f154d5f25d2332d3ea9f8ebb837c6f0156ffe8f2420773f3907230be4b2b85`  
		Last Modified: Thu, 23 Apr 2020 02:58:31 GMT  
		Size: 130.2 MB (130190019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0`

```console
$ docker pull mono@sha256:5369341c2c163d02bbd085644993ecc35d7366385ea36fd97130ceea5ed3872e
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
$ docker pull mono@sha256:2351a2ba6c2228ecac8696680f65e49607432bb7fd6c0494fd254060c48f6a02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235136555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59599093bfc20b4291b6019e7cd8bd648dab8dc3c341bc26001f807264ac44dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:59:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e83f8e35ba5681f2772165e09a403fab75e2cb54d9c6166e85301ad905d258`  
		Last Modified: Thu, 23 Apr 2020 02:20:55 GMT  
		Size: 147.8 MB (147794220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:638eb478bc2d77761637d3c38bdd315feca956bb670fe7a57de4cc35cb6c7215
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbdf0b0401ab5130c35b7db945960e55082c3ab6023657188752ec82f91cae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:27:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3f3bb75c812ff1a60644fe7dce9fbed58cd4578c80f3e37b9714f26987ed2`  
		Last Modified: Thu, 23 Apr 2020 02:37:17 GMT  
		Size: 129.9 MB (129892151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:c874c01c6f92382c5cec60d09cc395518c556217595e4c806afb22d672d3e45c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e196d31d2f638e7440ab21cfc4440afb3d32e9e49ee3ea6698a7331936ea0ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2fcd3e55989df99fa1643abe68ef9911caf777caf659f98a9672df51bab1`  
		Last Modified: Thu, 23 Apr 2020 03:06:12 GMT  
		Size: 128.6 MB (128556011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2c4a103ab7827cd92c451d3eb273403a21172601e646618353670b5bc9c11d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9689c7b697340040a0333ddb72fe3f1026947a0fd9aafd57a27eead437208c5d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:03:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e858c5d0189c31dc4dd9dfe8546a68dfb734613feaf85697642b6b0798f08`  
		Last Modified: Thu, 23 Apr 2020 04:11:28 GMT  
		Size: 144.7 MB (144712974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0` - linux; ppc64le

```console
$ docker pull mono@sha256:c872e3bb21f26535dfc38f43e7e622be64e67b77e2c05818d04390929a2b7227
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178995140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25acb6d4e7f1006ab9ff7f6d82a649bf9ee795479e883b74dd7e66e21cb07a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f154d5f25d2332d3ea9f8ebb837c6f0156ffe8f2420773f3907230be4b2b85`  
		Last Modified: Thu, 23 Apr 2020 02:58:31 GMT  
		Size: 130.2 MB (130190019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.96`

```console
$ docker pull mono@sha256:5369341c2c163d02bbd085644993ecc35d7366385ea36fd97130ceea5ed3872e
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
$ docker pull mono@sha256:2351a2ba6c2228ecac8696680f65e49607432bb7fd6c0494fd254060c48f6a02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235136555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59599093bfc20b4291b6019e7cd8bd648dab8dc3c341bc26001f807264ac44dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:59:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e83f8e35ba5681f2772165e09a403fab75e2cb54d9c6166e85301ad905d258`  
		Last Modified: Thu, 23 Apr 2020 02:20:55 GMT  
		Size: 147.8 MB (147794220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v5

```console
$ docker pull mono@sha256:638eb478bc2d77761637d3c38bdd315feca956bb670fe7a57de4cc35cb6c7215
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbdf0b0401ab5130c35b7db945960e55082c3ab6023657188752ec82f91cae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:27:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3f3bb75c812ff1a60644fe7dce9fbed58cd4578c80f3e37b9714f26987ed2`  
		Last Modified: Thu, 23 Apr 2020 02:37:17 GMT  
		Size: 129.9 MB (129892151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm variant v7

```console
$ docker pull mono@sha256:c874c01c6f92382c5cec60d09cc395518c556217595e4c806afb22d672d3e45c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e196d31d2f638e7440ab21cfc4440afb3d32e9e49ee3ea6698a7331936ea0ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2fcd3e55989df99fa1643abe68ef9911caf777caf659f98a9672df51bab1`  
		Last Modified: Thu, 23 Apr 2020 03:06:12 GMT  
		Size: 128.6 MB (128556011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2c4a103ab7827cd92c451d3eb273403a21172601e646618353670b5bc9c11d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9689c7b697340040a0333ddb72fe3f1026947a0fd9aafd57a27eead437208c5d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:03:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e858c5d0189c31dc4dd9dfe8546a68dfb734613feaf85697642b6b0798f08`  
		Last Modified: Thu, 23 Apr 2020 04:11:28 GMT  
		Size: 144.7 MB (144712974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96` - linux; ppc64le

```console
$ docker pull mono@sha256:c872e3bb21f26535dfc38f43e7e622be64e67b77e2c05818d04390929a2b7227
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178995140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25acb6d4e7f1006ab9ff7f6d82a649bf9ee795479e883b74dd7e66e21cb07a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f154d5f25d2332d3ea9f8ebb837c6f0156ffe8f2420773f3907230be4b2b85`  
		Last Modified: Thu, 23 Apr 2020 02:58:31 GMT  
		Size: 130.2 MB (130190019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0.96-slim`

```console
$ docker pull mono@sha256:b03b2b1fd60aaea59ad7432d46737b415cad60f949eb027b763062b64e393d36
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
$ docker pull mono@sha256:dea2a84843d47ee855a58ca9291c5838d5f13a703074e85ce81a2b324675a091
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522d57eded02abb2b3358f68714c4c066951809e1257fee584c4f22ad8347f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c84055314f27f19e52dcac51c9fad016f4788d9abf0ee3b25eaf28da1055e3be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae020d257a70091fa1eeec6f788f3605c24b889a34533f2b521b15cf20721b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3ff96831a86c406c1bd704aa1789773fc50ab566670193c88f5dffcdfd5281fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44152019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73087f72fc1d05c4643520860084c4f1f3a4a25510590944ab098aeefe83f5ac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:957f793fa4f8f14a4599c09d19e599edf0863a2d959dc4833217d1bd48a1971d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba956c66d116f07f43717d84cd75a95617bcda4d5ee277b58c631c47683a784`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0.96-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89bfa6ac390cb3e3c3550d6a5c823fb530789e87855094aaf2f00ec85dc6d0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b273d008dfb57b47f4b740d65ed19b4e7eece7c2b9d0ca4c16e272a395f249`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8.0-slim`

```console
$ docker pull mono@sha256:b03b2b1fd60aaea59ad7432d46737b415cad60f949eb027b763062b64e393d36
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
$ docker pull mono@sha256:dea2a84843d47ee855a58ca9291c5838d5f13a703074e85ce81a2b324675a091
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522d57eded02abb2b3358f68714c4c066951809e1257fee584c4f22ad8347f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c84055314f27f19e52dcac51c9fad016f4788d9abf0ee3b25eaf28da1055e3be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae020d257a70091fa1eeec6f788f3605c24b889a34533f2b521b15cf20721b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3ff96831a86c406c1bd704aa1789773fc50ab566670193c88f5dffcdfd5281fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44152019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73087f72fc1d05c4643520860084c4f1f3a4a25510590944ab098aeefe83f5ac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:957f793fa4f8f14a4599c09d19e599edf0863a2d959dc4833217d1bd48a1971d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba956c66d116f07f43717d84cd75a95617bcda4d5ee277b58c631c47683a784`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89bfa6ac390cb3e3c3550d6a5c823fb530789e87855094aaf2f00ec85dc6d0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b273d008dfb57b47f4b740d65ed19b4e7eece7c2b9d0ca4c16e272a395f249`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.8-slim`

```console
$ docker pull mono@sha256:b03b2b1fd60aaea59ad7432d46737b415cad60f949eb027b763062b64e393d36
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
$ docker pull mono@sha256:dea2a84843d47ee855a58ca9291c5838d5f13a703074e85ce81a2b324675a091
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522d57eded02abb2b3358f68714c4c066951809e1257fee584c4f22ad8347f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c84055314f27f19e52dcac51c9fad016f4788d9abf0ee3b25eaf28da1055e3be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae020d257a70091fa1eeec6f788f3605c24b889a34533f2b521b15cf20721b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3ff96831a86c406c1bd704aa1789773fc50ab566670193c88f5dffcdfd5281fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44152019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73087f72fc1d05c4643520860084c4f1f3a4a25510590944ab098aeefe83f5ac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:957f793fa4f8f14a4599c09d19e599edf0863a2d959dc4833217d1bd48a1971d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba956c66d116f07f43717d84cd75a95617bcda4d5ee277b58c631c47683a784`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.8-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89bfa6ac390cb3e3c3550d6a5c823fb530789e87855094aaf2f00ec85dc6d0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b273d008dfb57b47f4b740d65ed19b4e7eece7c2b9d0ca4c16e272a395f249`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:b03b2b1fd60aaea59ad7432d46737b415cad60f949eb027b763062b64e393d36
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
$ docker pull mono@sha256:dea2a84843d47ee855a58ca9291c5838d5f13a703074e85ce81a2b324675a091
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522d57eded02abb2b3358f68714c4c066951809e1257fee584c4f22ad8347f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c84055314f27f19e52dcac51c9fad016f4788d9abf0ee3b25eaf28da1055e3be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae020d257a70091fa1eeec6f788f3605c24b889a34533f2b521b15cf20721b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3ff96831a86c406c1bd704aa1789773fc50ab566670193c88f5dffcdfd5281fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44152019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73087f72fc1d05c4643520860084c4f1f3a4a25510590944ab098aeefe83f5ac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:957f793fa4f8f14a4599c09d19e599edf0863a2d959dc4833217d1bd48a1971d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba956c66d116f07f43717d84cd75a95617bcda4d5ee277b58c631c47683a784`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89bfa6ac390cb3e3c3550d6a5c823fb530789e87855094aaf2f00ec85dc6d0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b273d008dfb57b47f4b740d65ed19b4e7eece7c2b9d0ca4c16e272a395f249`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:5369341c2c163d02bbd085644993ecc35d7366385ea36fd97130ceea5ed3872e
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
$ docker pull mono@sha256:2351a2ba6c2228ecac8696680f65e49607432bb7fd6c0494fd254060c48f6a02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235136555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59599093bfc20b4291b6019e7cd8bd648dab8dc3c341bc26001f807264ac44dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:59:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e83f8e35ba5681f2772165e09a403fab75e2cb54d9c6166e85301ad905d258`  
		Last Modified: Thu, 23 Apr 2020 02:20:55 GMT  
		Size: 147.8 MB (147794220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:638eb478bc2d77761637d3c38bdd315feca956bb670fe7a57de4cc35cb6c7215
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176695663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbdf0b0401ab5130c35b7db945960e55082c3ab6023657188752ec82f91cae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:27:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3f3bb75c812ff1a60644fe7dce9fbed58cd4578c80f3e37b9714f26987ed2`  
		Last Modified: Thu, 23 Apr 2020 02:37:17 GMT  
		Size: 129.9 MB (129892151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:c874c01c6f92382c5cec60d09cc395518c556217595e4c806afb22d672d3e45c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172708030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e196d31d2f638e7440ab21cfc4440afb3d32e9e49ee3ea6698a7331936ea0ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:56:44 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d2fcd3e55989df99fa1643abe68ef9911caf777caf659f98a9672df51bab1`  
		Last Modified: Thu, 23 Apr 2020 03:06:12 GMT  
		Size: 128.6 MB (128556011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:e2c4a103ab7827cd92c451d3eb273403a21172601e646618353670b5bc9c11d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194747555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9689c7b697340040a0333ddb72fe3f1026947a0fd9aafd57a27eead437208c5d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 04:03:56 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e858c5d0189c31dc4dd9dfe8546a68dfb734613feaf85697642b6b0798f08`  
		Last Modified: Thu, 23 Apr 2020 04:11:28 GMT  
		Size: 144.7 MB (144712974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:9c689075bb69bade3f528bb36bfe204fd3529387d13addcfe9d2c43db444d7a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243509400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1505bc590d4dce8f057579c70b93a89b4ce6d044fd5f80a06eb1765872b2e2b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 01:09:10 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f8d38ff41ce32cf902046d0c45ed81a3a5475418bddade545b50a630ae181`  
		Last Modified: Thu, 23 Apr 2020 01:16:08 GMT  
		Size: 151.5 MB (151492512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:c872e3bb21f26535dfc38f43e7e622be64e67b77e2c05818d04390929a2b7227
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178995140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25acb6d4e7f1006ab9ff7f6d82a649bf9ee795479e883b74dd7e66e21cb07a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Apr 2020 02:44:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f154d5f25d2332d3ea9f8ebb837c6f0156ffe8f2420773f3907230be4b2b85`  
		Last Modified: Thu, 23 Apr 2020 02:58:31 GMT  
		Size: 130.2 MB (130190019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:b03b2b1fd60aaea59ad7432d46737b415cad60f949eb027b763062b64e393d36
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
$ docker pull mono@sha256:dea2a84843d47ee855a58ca9291c5838d5f13a703074e85ce81a2b324675a091
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87342335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522d57eded02abb2b3358f68714c4c066951809e1257fee584c4f22ad8347f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:48:15 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:48:26 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:48:58 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f98f65ba396764fe9568783d5a5c15abaed85471ba915f7533777d9ee788d`  
		Last Modified: Thu, 23 Apr 2020 02:19:07 GMT  
		Size: 244.5 KB (244473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df397516278d03ee36a7c24249bc8b0b57b23701952818c89538b9856c1ffb`  
		Last Modified: Thu, 23 Apr 2020 02:19:25 GMT  
		Size: 64.6 MB (64584374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c84055314f27f19e52dcac51c9fad016f4788d9abf0ee3b25eaf28da1055e3be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46803512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae020d257a70091fa1eeec6f788f3605c24b889a34533f2b521b15cf20721b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:04 GMT
ADD file:60586a4bfaca91a5985bf13744e752136a597186e5bd3aa0eddf7bdd600130fe in / 
# Thu, 23 Apr 2020 00:56:06 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:09:25 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:09:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:10:36 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:a07595075223d769a641d7054a9dd729aaba7d95a05cf2e83dd10958a78d9e04`  
		Last Modified: Thu, 23 Apr 2020 01:03:53 GMT  
		Size: 21.2 MB (21190846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d6fd4c06cc8f4923081530e30b7e3a8745891826cbf8c01310ee0f072c2bfd`  
		Last Modified: Thu, 23 Apr 2020 02:35:16 GMT  
		Size: 244.6 KB (244557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae990ae22590a42ab1c4bf2804eedb7c6156066008ecda48b2e934810391f8`  
		Last Modified: Thu, 23 Apr 2020 02:35:26 GMT  
		Size: 25.4 MB (25368109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:3ff96831a86c406c1bd704aa1789773fc50ab566670193c88f5dffcdfd5281fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44152019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73087f72fc1d05c4643520860084c4f1f3a4a25510590944ab098aeefe83f5ac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:49:52 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:50:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:51:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039d96cd64773696fdd57e5b4e56627377b34c8f994cb379003dca020688a871`  
		Last Modified: Thu, 23 Apr 2020 03:04:21 GMT  
		Size: 244.6 KB (244585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2e62f69e35dd345637b31ba135f59556486a6b1a5ce47cc3de7e61bc8979c7`  
		Last Modified: Thu, 23 Apr 2020 03:04:28 GMT  
		Size: 24.6 MB (24608971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:957f793fa4f8f14a4599c09d19e599edf0863a2d959dc4833217d1bd48a1971d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50034581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba956c66d116f07f43717d84cd75a95617bcda4d5ee277b58c631c47683a784`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:57:21 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 03:57:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 03:58:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cea723c9ac27330e9038d62385757c1062449c5ae055b34af6e2f80611c8f0`  
		Last Modified: Thu, 23 Apr 2020 04:09:30 GMT  
		Size: 244.4 KB (244380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c72e9862cc95c36bed5a80139020f8f6240a122dcba876cc648cfe45c2d10f`  
		Last Modified: Thu, 23 Apr 2020 04:09:40 GMT  
		Size: 29.4 MB (29420108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:992d47fb588cd80517b999abe4626317c65dcfd5eb0dea3bea6b02cdb56b5db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41612f812aa87758c87bf3cf7d3d08ab20128631db6c4454c68b94583387608`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:04:12 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 01:04:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 01:05:02 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3b9d440d2c40f2a9f3756fc7f8347bb9ec214b84fa396a388bd94782e1a678`  
		Last Modified: Thu, 23 Apr 2020 01:14:10 GMT  
		Size: 244.5 KB (244496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b74896e741d2269bb5084cfdbe6af6d2fc8d9d0ed1fc3f055d7c644afad5d`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 68.6 MB (68630969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:e89bfa6ac390cb3e3c3550d6a5c823fb530789e87855094aaf2f00ec85dc6d0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48805121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b273d008dfb57b47f4b740d65ed19b4e7eece7c2b9d0ca4c16e272a395f249`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:31:35 GMT
ENV MONO_VERSION=6.8.0.96
# Thu, 23 Apr 2020 02:32:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Apr 2020 02:33:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-vs.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff60a83a61c064637d7b71ee4cde3095f4d26a52203198411674b27034acf5f5`  
		Last Modified: Thu, 23 Apr 2020 02:56:58 GMT  
		Size: 244.5 KB (244517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615e483d5e6ec2721b8e876bee0e377def7f3cac05835c66d44494e1b671ee61`  
		Last Modified: Thu, 23 Apr 2020 02:57:04 GMT  
		Size: 25.8 MB (25775199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
