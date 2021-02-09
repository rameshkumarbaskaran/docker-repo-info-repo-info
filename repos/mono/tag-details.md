<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:6`](#mono6)
-	[`mono:6.10`](#mono610)
-	[`mono:6.10.0`](#mono6100)
-	[`mono:6.10.0.104`](#mono6100104)
-	[`mono:6.10.0.104-slim`](#mono6100104-slim)
-	[`mono:6.10.0-slim`](#mono6100-slim)
-	[`mono:6.10-slim`](#mono610-slim)
-	[`mono:6.12`](#mono612)
-	[`mono:6.12.0`](#mono6120)
-	[`mono:6.12.0.107`](#mono6120107)
-	[`mono:6.12.0.107-slim`](#mono6120107-slim)
-	[`mono:6.12.0-slim`](#mono6120-slim)
-	[`mono:6.12-slim`](#mono612-slim)
-	[`mono:6-slim`](#mono6-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:27c87f0e658e1e7b581c6cebba40291b7b9b8c5f185097487c11421a9affab91
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
$ docker pull mono@sha256:cb9847ac5d6fd26161bf205fa114d86cc9a758990eb0a7a98ab4d0c2f6bdd44f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235890229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f933583298fbfd77736a41005ee5a89646c27f585ddfb0a311e25f11e39bced4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:40:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ddc40d3fd3ff23fc8c7d609df57d5e59757495cfa018aeafa321f297607ab8`  
		Last Modified: Tue, 09 Feb 2021 06:50:24 GMT  
		Size: 141.4 MB (141414462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb7704cbafeb7d923de33db68ef4e02e9f94841b0e32fe829efd4fdecbed3fae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ebdb4f4808487be7fd9c23f9913d029636f61c776e8e029e88f16f3816ff0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:29:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b073e05819fa9a1049e7fafecd7017e92c5ed02402cc0c054eaa6eaf60ff70`  
		Last Modified: Tue, 09 Feb 2021 06:34:25 GMT  
		Size: 156.6 MB (156583695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:9196cb7af6c2772da7f6ddfec282377c2bb5e772e18830b1904c7919ff5fe995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241671010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db70dec2a082291d4e42c8bc96bb8d8a179f2be44f8f6a7a2e367746b38da63a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:25:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37e3c3267ba37fca1ca8ec497a3b1da52bdbeb8b2e5e6ffd3cfa0da52318fb`  
		Last Modified: Tue, 09 Feb 2021 07:29:40 GMT  
		Size: 142.5 MB (142513705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:d48033fb4677aeb49fd8d32c65d72f852447b5c4a70259eded4be1b64e6bd216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203359826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218f591f82b680524575e557e913cc587ef62f97da719fd0b36a91225000d92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:19:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ddb78f1e2738129e590d0602d2a6fc879aeffba4a36af01622f8672a0dcba`  
		Last Modified: Tue, 09 Feb 2021 10:36:46 GMT  
		Size: 143.2 MB (143226471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:ac717fcbf4d7a137c9c3acc99967314ce0589e7ce201d016299591ebac8fc068
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
$ docker pull mono@sha256:a70d121bacb47c6a8f1acd4bfae0b3ff90268b9a19675749e587586a9b9803b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1339008bba2354c54569ab253b234a96920152c8d229a80349e52b9f8bd7edf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:31:05 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:31:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:31:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:48:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602a2523b4c1702e9f4d7980b1e596f1f2e873139eaed79e245fe923c75da45f`  
		Last Modified: Tue, 09 Feb 2021 06:49:24 GMT  
		Size: 255.9 KB (255927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33d629a5e809c2dadb3d970680f4c12832313948aabdaeffc129ba0ea22ce45`  
		Last Modified: Tue, 09 Feb 2021 06:49:43 GMT  
		Size: 67.1 MB (67142461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3720b65351f9ba9a88990f0feb500c882282a109f4c935b4f9124919613af6a1`  
		Last Modified: Tue, 09 Feb 2021 06:51:04 GMT  
		Size: 130.3 MB (130289905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:5af63248159aed358b06ada57e95e308ea1c223a298088d91422fd0ce00f40e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180632533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478ed95add121817e320c0f83fe2b60aa2b2dbb1cf8229d680f2d56dbd5ce38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b135eeb77d4910d732e79e8132148b43949a28bc3d231923f3de862124ab98`  
		Last Modified: Tue, 09 Feb 2021 04:21:55 GMT  
		Size: 129.0 MB (128962193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d39d372380f5a73de1f4c13baefe5fe30208504c2ee87a5c3a46da5d2c5a7ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176550748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3606599470c3663a458214939b09b22fac76dba598915323586f15dfa2c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95880f81ec1d835fef70912336e6b01cad3de5a478b93b5e46c148f4247812`  
		Last Modified: Tue, 09 Feb 2021 04:21:35 GMT  
		Size: 127.8 MB (127815548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:dec7a2f69af5a4bb8ef93dff6ab2fe9fd3805664c7122ab41e1b172d28e496e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203347521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf2d0fab3a65170b6aaef9f0963fc8480a41c2f46327afb20487d7c5c09d9ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:26:42 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:26:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:27:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:32:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd57133f207df525339b618cd5d8470b92a2e5cb087f8b2c9120e75b70f487`  
		Last Modified: Tue, 09 Feb 2021 06:33:09 GMT  
		Size: 255.9 KB (255914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb7eb4af2e43b98ecb88d92ca13d1c71b3044d4f7c3fe18dd36d272bd059f9`  
		Last Modified: Tue, 09 Feb 2021 06:33:29 GMT  
		Size: 31.8 MB (31790638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5d6b793a1dea33038ac206501746356a1323165f1f3576a95e67b902d54bce`  
		Last Modified: Tue, 09 Feb 2021 06:35:17 GMT  
		Size: 145.4 MB (145449520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:72faca682011d8fac4643911b475eeb7180e1fecc9e1ec85db0959c8e2eab638
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230573441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed52e8a5a33c9bc96c3f4e93a8b1bdfb59762f7a7b873877c063e8d595ba43c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:20:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 07:21:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:22:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:27:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983a43b23ae79d508f5964d45ee87ae0a5ee8d2cbc7ac265aea2e88f7969c12`  
		Last Modified: Tue, 09 Feb 2021 07:28:31 GMT  
		Size: 255.9 KB (255864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5f6745e05a0237853f5d31cddef2805f6e0c40f1550490f6bd0bbe741d1e6`  
		Last Modified: Tue, 09 Feb 2021 07:28:50 GMT  
		Size: 71.2 MB (71174281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba50c8af50ca3f1ef98f08d05e972027a213420c82af6c6fc06402dee53a3e5`  
		Last Modified: Tue, 09 Feb 2021 07:30:31 GMT  
		Size: 131.4 MB (131390565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:a909a63e17de1f7d8221d68679c466f114c3c11d1d7b28b92cdb95228264fde9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192149819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73768f0d5d30453f0f1a7ea39c4a0ece2fc04663d5db12369631558004ec4b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:01:25 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 10:03:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:06:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:34:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f4993e21317e9a1f38f5521a1f92380c9e2222b0efa8fe5fdd25fd4bb319`  
		Last Modified: Tue, 09 Feb 2021 10:35:57 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0ced8721828e3bd795405b0bf7f06c518ec9e3f9559b1cca1d5b3a6b2e3b39`  
		Last Modified: Tue, 09 Feb 2021 10:36:03 GMT  
		Size: 29.4 MB (29394248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0559f578ae7696b574f53e1d963a0701e2712e889f13566509a3db13f0ce`  
		Last Modified: Tue, 09 Feb 2021 10:37:33 GMT  
		Size: 132.0 MB (131979802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:ac717fcbf4d7a137c9c3acc99967314ce0589e7ce201d016299591ebac8fc068
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
$ docker pull mono@sha256:a70d121bacb47c6a8f1acd4bfae0b3ff90268b9a19675749e587586a9b9803b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1339008bba2354c54569ab253b234a96920152c8d229a80349e52b9f8bd7edf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:31:05 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:31:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:31:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:48:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602a2523b4c1702e9f4d7980b1e596f1f2e873139eaed79e245fe923c75da45f`  
		Last Modified: Tue, 09 Feb 2021 06:49:24 GMT  
		Size: 255.9 KB (255927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33d629a5e809c2dadb3d970680f4c12832313948aabdaeffc129ba0ea22ce45`  
		Last Modified: Tue, 09 Feb 2021 06:49:43 GMT  
		Size: 67.1 MB (67142461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3720b65351f9ba9a88990f0feb500c882282a109f4c935b4f9124919613af6a1`  
		Last Modified: Tue, 09 Feb 2021 06:51:04 GMT  
		Size: 130.3 MB (130289905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:5af63248159aed358b06ada57e95e308ea1c223a298088d91422fd0ce00f40e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180632533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478ed95add121817e320c0f83fe2b60aa2b2dbb1cf8229d680f2d56dbd5ce38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b135eeb77d4910d732e79e8132148b43949a28bc3d231923f3de862124ab98`  
		Last Modified: Tue, 09 Feb 2021 04:21:55 GMT  
		Size: 129.0 MB (128962193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d39d372380f5a73de1f4c13baefe5fe30208504c2ee87a5c3a46da5d2c5a7ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176550748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3606599470c3663a458214939b09b22fac76dba598915323586f15dfa2c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95880f81ec1d835fef70912336e6b01cad3de5a478b93b5e46c148f4247812`  
		Last Modified: Tue, 09 Feb 2021 04:21:35 GMT  
		Size: 127.8 MB (127815548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:dec7a2f69af5a4bb8ef93dff6ab2fe9fd3805664c7122ab41e1b172d28e496e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203347521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf2d0fab3a65170b6aaef9f0963fc8480a41c2f46327afb20487d7c5c09d9ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:26:42 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:26:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:27:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:32:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd57133f207df525339b618cd5d8470b92a2e5cb087f8b2c9120e75b70f487`  
		Last Modified: Tue, 09 Feb 2021 06:33:09 GMT  
		Size: 255.9 KB (255914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb7eb4af2e43b98ecb88d92ca13d1c71b3044d4f7c3fe18dd36d272bd059f9`  
		Last Modified: Tue, 09 Feb 2021 06:33:29 GMT  
		Size: 31.8 MB (31790638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5d6b793a1dea33038ac206501746356a1323165f1f3576a95e67b902d54bce`  
		Last Modified: Tue, 09 Feb 2021 06:35:17 GMT  
		Size: 145.4 MB (145449520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:72faca682011d8fac4643911b475eeb7180e1fecc9e1ec85db0959c8e2eab638
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230573441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed52e8a5a33c9bc96c3f4e93a8b1bdfb59762f7a7b873877c063e8d595ba43c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:20:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 07:21:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:22:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:27:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983a43b23ae79d508f5964d45ee87ae0a5ee8d2cbc7ac265aea2e88f7969c12`  
		Last Modified: Tue, 09 Feb 2021 07:28:31 GMT  
		Size: 255.9 KB (255864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5f6745e05a0237853f5d31cddef2805f6e0c40f1550490f6bd0bbe741d1e6`  
		Last Modified: Tue, 09 Feb 2021 07:28:50 GMT  
		Size: 71.2 MB (71174281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba50c8af50ca3f1ef98f08d05e972027a213420c82af6c6fc06402dee53a3e5`  
		Last Modified: Tue, 09 Feb 2021 07:30:31 GMT  
		Size: 131.4 MB (131390565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:a909a63e17de1f7d8221d68679c466f114c3c11d1d7b28b92cdb95228264fde9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192149819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73768f0d5d30453f0f1a7ea39c4a0ece2fc04663d5db12369631558004ec4b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:01:25 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 10:03:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:06:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:34:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f4993e21317e9a1f38f5521a1f92380c9e2222b0efa8fe5fdd25fd4bb319`  
		Last Modified: Tue, 09 Feb 2021 10:35:57 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0ced8721828e3bd795405b0bf7f06c518ec9e3f9559b1cca1d5b3a6b2e3b39`  
		Last Modified: Tue, 09 Feb 2021 10:36:03 GMT  
		Size: 29.4 MB (29394248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0559f578ae7696b574f53e1d963a0701e2712e889f13566509a3db13f0ce`  
		Last Modified: Tue, 09 Feb 2021 10:37:33 GMT  
		Size: 132.0 MB (131979802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:ac717fcbf4d7a137c9c3acc99967314ce0589e7ce201d016299591ebac8fc068
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
$ docker pull mono@sha256:a70d121bacb47c6a8f1acd4bfae0b3ff90268b9a19675749e587586a9b9803b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224783435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1339008bba2354c54569ab253b234a96920152c8d229a80349e52b9f8bd7edf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:31:05 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:31:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:31:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:48:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602a2523b4c1702e9f4d7980b1e596f1f2e873139eaed79e245fe923c75da45f`  
		Last Modified: Tue, 09 Feb 2021 06:49:24 GMT  
		Size: 255.9 KB (255927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33d629a5e809c2dadb3d970680f4c12832313948aabdaeffc129ba0ea22ce45`  
		Last Modified: Tue, 09 Feb 2021 06:49:43 GMT  
		Size: 67.1 MB (67142461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3720b65351f9ba9a88990f0feb500c882282a109f4c935b4f9124919613af6a1`  
		Last Modified: Tue, 09 Feb 2021 06:51:04 GMT  
		Size: 130.3 MB (130289905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:5af63248159aed358b06ada57e95e308ea1c223a298088d91422fd0ce00f40e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180632533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478ed95add121817e320c0f83fe2b60aa2b2dbb1cf8229d680f2d56dbd5ce38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:43 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b135eeb77d4910d732e79e8132148b43949a28bc3d231923f3de862124ab98`  
		Last Modified: Tue, 09 Feb 2021 04:21:55 GMT  
		Size: 129.0 MB (128962193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:8d39d372380f5a73de1f4c13baefe5fe30208504c2ee87a5c3a46da5d2c5a7ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176550748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c3606599470c3663a458214939b09b22fac76dba598915323586f15dfa2c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:18:18 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c95880f81ec1d835fef70912336e6b01cad3de5a478b93b5e46c148f4247812`  
		Last Modified: Tue, 09 Feb 2021 04:21:35 GMT  
		Size: 127.8 MB (127815548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:dec7a2f69af5a4bb8ef93dff6ab2fe9fd3805664c7122ab41e1b172d28e496e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203347521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf2d0fab3a65170b6aaef9f0963fc8480a41c2f46327afb20487d7c5c09d9ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:26:42 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:26:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:27:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:32:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd57133f207df525339b618cd5d8470b92a2e5cb087f8b2c9120e75b70f487`  
		Last Modified: Tue, 09 Feb 2021 06:33:09 GMT  
		Size: 255.9 KB (255914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb7eb4af2e43b98ecb88d92ca13d1c71b3044d4f7c3fe18dd36d272bd059f9`  
		Last Modified: Tue, 09 Feb 2021 06:33:29 GMT  
		Size: 31.8 MB (31790638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5d6b793a1dea33038ac206501746356a1323165f1f3576a95e67b902d54bce`  
		Last Modified: Tue, 09 Feb 2021 06:35:17 GMT  
		Size: 145.4 MB (145449520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:72faca682011d8fac4643911b475eeb7180e1fecc9e1ec85db0959c8e2eab638
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230573441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed52e8a5a33c9bc96c3f4e93a8b1bdfb59762f7a7b873877c063e8d595ba43c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:20:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 07:21:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:22:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:27:20 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983a43b23ae79d508f5964d45ee87ae0a5ee8d2cbc7ac265aea2e88f7969c12`  
		Last Modified: Tue, 09 Feb 2021 07:28:31 GMT  
		Size: 255.9 KB (255864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5f6745e05a0237853f5d31cddef2805f6e0c40f1550490f6bd0bbe741d1e6`  
		Last Modified: Tue, 09 Feb 2021 07:28:50 GMT  
		Size: 71.2 MB (71174281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba50c8af50ca3f1ef98f08d05e972027a213420c82af6c6fc06402dee53a3e5`  
		Last Modified: Tue, 09 Feb 2021 07:30:31 GMT  
		Size: 131.4 MB (131390565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:a909a63e17de1f7d8221d68679c466f114c3c11d1d7b28b92cdb95228264fde9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192149819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73768f0d5d30453f0f1a7ea39c4a0ece2fc04663d5db12369631558004ec4b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:01:25 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 10:03:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:06:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:34:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f4993e21317e9a1f38f5521a1f92380c9e2222b0efa8fe5fdd25fd4bb319`  
		Last Modified: Tue, 09 Feb 2021 10:35:57 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0ced8721828e3bd795405b0bf7f06c518ec9e3f9559b1cca1d5b3a6b2e3b39`  
		Last Modified: Tue, 09 Feb 2021 10:36:03 GMT  
		Size: 29.4 MB (29394248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0559f578ae7696b574f53e1d963a0701e2712e889f13566509a3db13f0ce`  
		Last Modified: Tue, 09 Feb 2021 10:37:33 GMT  
		Size: 132.0 MB (131979802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:b6fd7277ebab0bdad60bc6dd82cd6163d0e38877321b1654998ec265efeaeee3
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
$ docker pull mono@sha256:fabd15ed370739b5dd3340197b84d63bc6a7ec96e4b4af34a837dbd9ff175c46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94493530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20707adc2bd007b59c91cadcf545d9753974cabc0030f3777b21f5325ae642bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:31:05 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:31:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:31:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602a2523b4c1702e9f4d7980b1e596f1f2e873139eaed79e245fe923c75da45f`  
		Last Modified: Tue, 09 Feb 2021 06:49:24 GMT  
		Size: 255.9 KB (255927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33d629a5e809c2dadb3d970680f4c12832313948aabdaeffc129ba0ea22ce45`  
		Last Modified: Tue, 09 Feb 2021 06:49:43 GMT  
		Size: 67.1 MB (67142461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c712f335d3056624b71f739eab72063f54dfdc9b1e79505f492350d575120386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51670340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebaa3f292c5fd2c5f88f4c02fde89257131eddc5ecc1b5f4ab3aefb23f54cf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1f06a597ee6d31d6be24bc45bd61b8bdbf82f41e4d20c6693c0562118c8c44d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48735200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c6e0275747a42fb6d529c5e573d92cb73aed4ef196a5dd6421239f57cc5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0ffc07f5df288d0d6d3d45106a3728df184ebc39666e96168d06042f72348f29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57898001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b13a85201da319c434186e445674c2e04c855cfd37259b7d054942b0152678`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:26:42 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:26:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:27:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd57133f207df525339b618cd5d8470b92a2e5cb087f8b2c9120e75b70f487`  
		Last Modified: Tue, 09 Feb 2021 06:33:09 GMT  
		Size: 255.9 KB (255914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb7eb4af2e43b98ecb88d92ca13d1c71b3044d4f7c3fe18dd36d272bd059f9`  
		Last Modified: Tue, 09 Feb 2021 06:33:29 GMT  
		Size: 31.8 MB (31790638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:4c57348f87c4d03004a9938ba22339081588011a6bdba35128251c7b85035277
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99182876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a2d075bc307db2644ff9cc4521a0299fa1bc1b9f791e32e9bafd2ec8fadf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:20:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 07:21:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:22:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983a43b23ae79d508f5964d45ee87ae0a5ee8d2cbc7ac265aea2e88f7969c12`  
		Last Modified: Tue, 09 Feb 2021 07:28:31 GMT  
		Size: 255.9 KB (255864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5f6745e05a0237853f5d31cddef2805f6e0c40f1550490f6bd0bbe741d1e6`  
		Last Modified: Tue, 09 Feb 2021 07:28:50 GMT  
		Size: 71.2 MB (71174281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:64f348c43c3e0152f5e4c381aa9cbf8dbd3c64feaeb405e8331346c7d7871cc7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1f5e2bb6d5faa4207770830f1adb379842f0cf37220730cf92c415e507ca6b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:01:25 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 10:03:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:06:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f4993e21317e9a1f38f5521a1f92380c9e2222b0efa8fe5fdd25fd4bb319`  
		Last Modified: Tue, 09 Feb 2021 10:35:57 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0ced8721828e3bd795405b0bf7f06c518ec9e3f9559b1cca1d5b3a6b2e3b39`  
		Last Modified: Tue, 09 Feb 2021 10:36:03 GMT  
		Size: 29.4 MB (29394248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:b6fd7277ebab0bdad60bc6dd82cd6163d0e38877321b1654998ec265efeaeee3
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
$ docker pull mono@sha256:fabd15ed370739b5dd3340197b84d63bc6a7ec96e4b4af34a837dbd9ff175c46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94493530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20707adc2bd007b59c91cadcf545d9753974cabc0030f3777b21f5325ae642bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:31:05 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:31:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:31:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602a2523b4c1702e9f4d7980b1e596f1f2e873139eaed79e245fe923c75da45f`  
		Last Modified: Tue, 09 Feb 2021 06:49:24 GMT  
		Size: 255.9 KB (255927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33d629a5e809c2dadb3d970680f4c12832313948aabdaeffc129ba0ea22ce45`  
		Last Modified: Tue, 09 Feb 2021 06:49:43 GMT  
		Size: 67.1 MB (67142461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c712f335d3056624b71f739eab72063f54dfdc9b1e79505f492350d575120386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51670340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebaa3f292c5fd2c5f88f4c02fde89257131eddc5ecc1b5f4ab3aefb23f54cf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1f06a597ee6d31d6be24bc45bd61b8bdbf82f41e4d20c6693c0562118c8c44d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48735200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c6e0275747a42fb6d529c5e573d92cb73aed4ef196a5dd6421239f57cc5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0ffc07f5df288d0d6d3d45106a3728df184ebc39666e96168d06042f72348f29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57898001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b13a85201da319c434186e445674c2e04c855cfd37259b7d054942b0152678`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:26:42 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:26:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:27:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd57133f207df525339b618cd5d8470b92a2e5cb087f8b2c9120e75b70f487`  
		Last Modified: Tue, 09 Feb 2021 06:33:09 GMT  
		Size: 255.9 KB (255914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb7eb4af2e43b98ecb88d92ca13d1c71b3044d4f7c3fe18dd36d272bd059f9`  
		Last Modified: Tue, 09 Feb 2021 06:33:29 GMT  
		Size: 31.8 MB (31790638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:4c57348f87c4d03004a9938ba22339081588011a6bdba35128251c7b85035277
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99182876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a2d075bc307db2644ff9cc4521a0299fa1bc1b9f791e32e9bafd2ec8fadf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:20:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 07:21:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:22:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983a43b23ae79d508f5964d45ee87ae0a5ee8d2cbc7ac265aea2e88f7969c12`  
		Last Modified: Tue, 09 Feb 2021 07:28:31 GMT  
		Size: 255.9 KB (255864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5f6745e05a0237853f5d31cddef2805f6e0c40f1550490f6bd0bbe741d1e6`  
		Last Modified: Tue, 09 Feb 2021 07:28:50 GMT  
		Size: 71.2 MB (71174281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:64f348c43c3e0152f5e4c381aa9cbf8dbd3c64feaeb405e8331346c7d7871cc7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1f5e2bb6d5faa4207770830f1adb379842f0cf37220730cf92c415e507ca6b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:01:25 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 10:03:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:06:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f4993e21317e9a1f38f5521a1f92380c9e2222b0efa8fe5fdd25fd4bb319`  
		Last Modified: Tue, 09 Feb 2021 10:35:57 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0ced8721828e3bd795405b0bf7f06c518ec9e3f9559b1cca1d5b3a6b2e3b39`  
		Last Modified: Tue, 09 Feb 2021 10:36:03 GMT  
		Size: 29.4 MB (29394248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:b6fd7277ebab0bdad60bc6dd82cd6163d0e38877321b1654998ec265efeaeee3
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
$ docker pull mono@sha256:fabd15ed370739b5dd3340197b84d63bc6a7ec96e4b4af34a837dbd9ff175c46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94493530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20707adc2bd007b59c91cadcf545d9753974cabc0030f3777b21f5325ae642bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:31:05 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:31:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:31:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602a2523b4c1702e9f4d7980b1e596f1f2e873139eaed79e245fe923c75da45f`  
		Last Modified: Tue, 09 Feb 2021 06:49:24 GMT  
		Size: 255.9 KB (255927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33d629a5e809c2dadb3d970680f4c12832313948aabdaeffc129ba0ea22ce45`  
		Last Modified: Tue, 09 Feb 2021 06:49:43 GMT  
		Size: 67.1 MB (67142461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:c712f335d3056624b71f739eab72063f54dfdc9b1e79505f492350d575120386
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51670340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebaa3f292c5fd2c5f88f4c02fde89257131eddc5ecc1b5f4ab3aefb23f54cf7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:23 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cb1c784014fc8011ca8f4610f5131311b17486b9d6077606eaddacde5a2c27`  
		Last Modified: Tue, 09 Feb 2021 04:19:46 GMT  
		Size: 256.0 KB (256004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4b453be37d3b9ff06672c4a993a5489066cd5c2df5d33b2e6a60b32cadecdb`  
		Last Modified: Tue, 09 Feb 2021 04:19:58 GMT  
		Size: 26.6 MB (26575039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:1f06a597ee6d31d6be24bc45bd61b8bdbf82f41e4d20c6693c0562118c8c44d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48735200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c6e0275747a42fb6d529c5e573d92cb73aed4ef196a5dd6421239f57cc5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:11:24 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 04:11:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:12:29 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7698330b69a6c19085fab2ed78c48495acb00c18a4ffc6e0f6f40d54b9421b50`  
		Last Modified: Tue, 09 Feb 2021 04:19:18 GMT  
		Size: 256.0 KB (255991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44741965a508902c904fb46c6cdf26919ecb482fe42acc022eede0e3bab5e501`  
		Last Modified: Tue, 09 Feb 2021 04:19:28 GMT  
		Size: 25.8 MB (25775825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0ffc07f5df288d0d6d3d45106a3728df184ebc39666e96168d06042f72348f29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57898001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b13a85201da319c434186e445674c2e04c855cfd37259b7d054942b0152678`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:26:42 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 06:26:57 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:27:32 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd57133f207df525339b618cd5d8470b92a2e5cb087f8b2c9120e75b70f487`  
		Last Modified: Tue, 09 Feb 2021 06:33:09 GMT  
		Size: 255.9 KB (255914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb7eb4af2e43b98ecb88d92ca13d1c71b3044d4f7c3fe18dd36d272bd059f9`  
		Last Modified: Tue, 09 Feb 2021 06:33:29 GMT  
		Size: 31.8 MB (31790638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:4c57348f87c4d03004a9938ba22339081588011a6bdba35128251c7b85035277
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99182876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a2d075bc307db2644ff9cc4521a0299fa1bc1b9f791e32e9bafd2ec8fadf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:20:55 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 07:21:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:22:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983a43b23ae79d508f5964d45ee87ae0a5ee8d2cbc7ac265aea2e88f7969c12`  
		Last Modified: Tue, 09 Feb 2021 07:28:31 GMT  
		Size: 255.9 KB (255864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e5f6745e05a0237853f5d31cddef2805f6e0c40f1550490f6bd0bbe741d1e6`  
		Last Modified: Tue, 09 Feb 2021 07:28:50 GMT  
		Size: 71.2 MB (71174281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:64f348c43c3e0152f5e4c381aa9cbf8dbd3c64feaeb405e8331346c7d7871cc7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60170017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1f5e2bb6d5faa4207770830f1adb379842f0cf37220730cf92c415e507ca6b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 10:01:25 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 09 Feb 2021 10:03:32 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:06:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f4993e21317e9a1f38f5521a1f92380c9e2222b0efa8fe5fdd25fd4bb319`  
		Last Modified: Tue, 09 Feb 2021 10:35:57 GMT  
		Size: 256.3 KB (256260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0ced8721828e3bd795405b0bf7f06c518ec9e3f9559b1cca1d5b3a6b2e3b39`  
		Last Modified: Tue, 09 Feb 2021 10:36:03 GMT  
		Size: 29.4 MB (29394248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:27c87f0e658e1e7b581c6cebba40291b7b9b8c5f185097487c11421a9affab91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12` - linux; amd64

```console
$ docker pull mono@sha256:cb9847ac5d6fd26161bf205fa114d86cc9a758990eb0a7a98ab4d0c2f6bdd44f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235890229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f933583298fbfd77736a41005ee5a89646c27f585ddfb0a311e25f11e39bced4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:40:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ddc40d3fd3ff23fc8c7d609df57d5e59757495cfa018aeafa321f297607ab8`  
		Last Modified: Tue, 09 Feb 2021 06:50:24 GMT  
		Size: 141.4 MB (141414462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb7704cbafeb7d923de33db68ef4e02e9f94841b0e32fe829efd4fdecbed3fae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ebdb4f4808487be7fd9c23f9913d029636f61c776e8e029e88f16f3816ff0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:29:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b073e05819fa9a1049e7fafecd7017e92c5ed02402cc0c054eaa6eaf60ff70`  
		Last Modified: Tue, 09 Feb 2021 06:34:25 GMT  
		Size: 156.6 MB (156583695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:9196cb7af6c2772da7f6ddfec282377c2bb5e772e18830b1904c7919ff5fe995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241671010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db70dec2a082291d4e42c8bc96bb8d8a179f2be44f8f6a7a2e367746b38da63a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:25:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37e3c3267ba37fca1ca8ec497a3b1da52bdbeb8b2e5e6ffd3cfa0da52318fb`  
		Last Modified: Tue, 09 Feb 2021 07:29:40 GMT  
		Size: 142.5 MB (142513705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:d48033fb4677aeb49fd8d32c65d72f852447b5c4a70259eded4be1b64e6bd216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203359826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218f591f82b680524575e557e913cc587ef62f97da719fd0b36a91225000d92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:19:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ddb78f1e2738129e590d0602d2a6fc879aeffba4a36af01622f8672a0dcba`  
		Last Modified: Tue, 09 Feb 2021 10:36:46 GMT  
		Size: 143.2 MB (143226471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:27c87f0e658e1e7b581c6cebba40291b7b9b8c5f185097487c11421a9affab91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0` - linux; amd64

```console
$ docker pull mono@sha256:cb9847ac5d6fd26161bf205fa114d86cc9a758990eb0a7a98ab4d0c2f6bdd44f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235890229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f933583298fbfd77736a41005ee5a89646c27f585ddfb0a311e25f11e39bced4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:40:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ddc40d3fd3ff23fc8c7d609df57d5e59757495cfa018aeafa321f297607ab8`  
		Last Modified: Tue, 09 Feb 2021 06:50:24 GMT  
		Size: 141.4 MB (141414462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb7704cbafeb7d923de33db68ef4e02e9f94841b0e32fe829efd4fdecbed3fae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ebdb4f4808487be7fd9c23f9913d029636f61c776e8e029e88f16f3816ff0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:29:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b073e05819fa9a1049e7fafecd7017e92c5ed02402cc0c054eaa6eaf60ff70`  
		Last Modified: Tue, 09 Feb 2021 06:34:25 GMT  
		Size: 156.6 MB (156583695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:9196cb7af6c2772da7f6ddfec282377c2bb5e772e18830b1904c7919ff5fe995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241671010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db70dec2a082291d4e42c8bc96bb8d8a179f2be44f8f6a7a2e367746b38da63a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:25:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37e3c3267ba37fca1ca8ec497a3b1da52bdbeb8b2e5e6ffd3cfa0da52318fb`  
		Last Modified: Tue, 09 Feb 2021 07:29:40 GMT  
		Size: 142.5 MB (142513705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:d48033fb4677aeb49fd8d32c65d72f852447b5c4a70259eded4be1b64e6bd216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203359826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218f591f82b680524575e557e913cc587ef62f97da719fd0b36a91225000d92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:19:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ddb78f1e2738129e590d0602d2a6fc879aeffba4a36af01622f8672a0dcba`  
		Last Modified: Tue, 09 Feb 2021 10:36:46 GMT  
		Size: 143.2 MB (143226471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107`

```console
$ docker pull mono@sha256:27c87f0e658e1e7b581c6cebba40291b7b9b8c5f185097487c11421a9affab91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107` - linux; amd64

```console
$ docker pull mono@sha256:cb9847ac5d6fd26161bf205fa114d86cc9a758990eb0a7a98ab4d0c2f6bdd44f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235890229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f933583298fbfd77736a41005ee5a89646c27f585ddfb0a311e25f11e39bced4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:40:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ddc40d3fd3ff23fc8c7d609df57d5e59757495cfa018aeafa321f297607ab8`  
		Last Modified: Tue, 09 Feb 2021 06:50:24 GMT  
		Size: 141.4 MB (141414462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb7704cbafeb7d923de33db68ef4e02e9f94841b0e32fe829efd4fdecbed3fae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ebdb4f4808487be7fd9c23f9913d029636f61c776e8e029e88f16f3816ff0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:29:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b073e05819fa9a1049e7fafecd7017e92c5ed02402cc0c054eaa6eaf60ff70`  
		Last Modified: Tue, 09 Feb 2021 06:34:25 GMT  
		Size: 156.6 MB (156583695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; 386

```console
$ docker pull mono@sha256:9196cb7af6c2772da7f6ddfec282377c2bb5e772e18830b1904c7919ff5fe995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241671010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db70dec2a082291d4e42c8bc96bb8d8a179f2be44f8f6a7a2e367746b38da63a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:25:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37e3c3267ba37fca1ca8ec497a3b1da52bdbeb8b2e5e6ffd3cfa0da52318fb`  
		Last Modified: Tue, 09 Feb 2021 07:29:40 GMT  
		Size: 142.5 MB (142513705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; ppc64le

```console
$ docker pull mono@sha256:d48033fb4677aeb49fd8d32c65d72f852447b5c4a70259eded4be1b64e6bd216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203359826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218f591f82b680524575e557e913cc587ef62f97da719fd0b36a91225000d92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:19:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ddb78f1e2738129e590d0602d2a6fc879aeffba4a36af01622f8672a0dcba`  
		Last Modified: Tue, 09 Feb 2021 10:36:46 GMT  
		Size: 143.2 MB (143226471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107-slim`

```console
$ docker pull mono@sha256:cc3b0873ea9d6cf7631abde58182ae7e3266d072440468c0f8f14279f6d813cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.107-slim` - linux; amd64

```console
$ docker pull mono@sha256:b345a98aec0b4f580217cf5942edb8488256edc63993c0f20c99f6f9be121941
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94475767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0a397518e81c5082088c3bee32a7aa6119d22d3096f451847d08edea876099`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:7cb672dd0eddc8de2299f3f3a4db421e2102a0c0ee87f9d79813f7a644681def
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57877003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8fd3521c313c83971ba466f58c9c2c68acbfe89c7a18b673f651683ce52e8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; 386

```console
$ docker pull mono@sha256:6c70f99d482b74150529414bd636340db13762b3c23f15db1cddeb8852e57a1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541135733b9c041f4723379541c34d3e9e24d001231dabeb20d67ef893bc275e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:00ce59b7eb2ae15020879cfe2b8b2d12ba61658cdc561287172a16095e12ba03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60133355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41039e5dd5571a5a495222c463a380f6334e74f17fe769b616ed5eec4364b91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:cc3b0873ea9d6cf7631abde58182ae7e3266d072440468c0f8f14279f6d813cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0-slim` - linux; amd64

```console
$ docker pull mono@sha256:b345a98aec0b4f580217cf5942edb8488256edc63993c0f20c99f6f9be121941
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94475767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0a397518e81c5082088c3bee32a7aa6119d22d3096f451847d08edea876099`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:7cb672dd0eddc8de2299f3f3a4db421e2102a0c0ee87f9d79813f7a644681def
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57877003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8fd3521c313c83971ba466f58c9c2c68acbfe89c7a18b673f651683ce52e8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:6c70f99d482b74150529414bd636340db13762b3c23f15db1cddeb8852e57a1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541135733b9c041f4723379541c34d3e9e24d001231dabeb20d67ef893bc275e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:00ce59b7eb2ae15020879cfe2b8b2d12ba61658cdc561287172a16095e12ba03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60133355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41039e5dd5571a5a495222c463a380f6334e74f17fe769b616ed5eec4364b91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:cc3b0873ea9d6cf7631abde58182ae7e3266d072440468c0f8f14279f6d813cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12-slim` - linux; amd64

```console
$ docker pull mono@sha256:b345a98aec0b4f580217cf5942edb8488256edc63993c0f20c99f6f9be121941
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94475767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0a397518e81c5082088c3bee32a7aa6119d22d3096f451847d08edea876099`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:7cb672dd0eddc8de2299f3f3a4db421e2102a0c0ee87f9d79813f7a644681def
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57877003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8fd3521c313c83971ba466f58c9c2c68acbfe89c7a18b673f651683ce52e8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:6c70f99d482b74150529414bd636340db13762b3c23f15db1cddeb8852e57a1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541135733b9c041f4723379541c34d3e9e24d001231dabeb20d67ef893bc275e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:00ce59b7eb2ae15020879cfe2b8b2d12ba61658cdc561287172a16095e12ba03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60133355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41039e5dd5571a5a495222c463a380f6334e74f17fe769b616ed5eec4364b91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:cc3b0873ea9d6cf7631abde58182ae7e3266d072440468c0f8f14279f6d813cd
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
$ docker pull mono@sha256:b345a98aec0b4f580217cf5942edb8488256edc63993c0f20c99f6f9be121941
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94475767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0a397518e81c5082088c3bee32a7aa6119d22d3096f451847d08edea876099`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:7cb672dd0eddc8de2299f3f3a4db421e2102a0c0ee87f9d79813f7a644681def
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57877003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8fd3521c313c83971ba466f58c9c2c68acbfe89c7a18b673f651683ce52e8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:6c70f99d482b74150529414bd636340db13762b3c23f15db1cddeb8852e57a1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541135733b9c041f4723379541c34d3e9e24d001231dabeb20d67ef893bc275e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:00ce59b7eb2ae15020879cfe2b8b2d12ba61658cdc561287172a16095e12ba03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60133355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41039e5dd5571a5a495222c463a380f6334e74f17fe769b616ed5eec4364b91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:27c87f0e658e1e7b581c6cebba40291b7b9b8c5f185097487c11421a9affab91
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
$ docker pull mono@sha256:cb9847ac5d6fd26161bf205fa114d86cc9a758990eb0a7a98ab4d0c2f6bdd44f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235890229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f933583298fbfd77736a41005ee5a89646c27f585ddfb0a311e25f11e39bced4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:40:25 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ddc40d3fd3ff23fc8c7d609df57d5e59757495cfa018aeafa321f297607ab8`  
		Last Modified: Tue, 09 Feb 2021 06:50:24 GMT  
		Size: 141.4 MB (141414462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:1d24028dba828fdc96b2b742b714f446f92b64abd6d180f3941954836178a989
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191752100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bcdc117695b526e00f4bac23d6c63d036306f5db62472b44bb3778d586032a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88dcc371a0eb826a2922cd9da711f02c951f809c2d794f69ed376a2fece59`  
		Last Modified: Tue, 09 Feb 2021 04:20:55 GMT  
		Size: 140.1 MB (140107311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:c73416458bcb7bf5fa69488bd6815e282f46605e12f39a780d06ca20f5bc052d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187637328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808ec81fbec92ca5875883f0c5df523025c9784692513d2affb1e388dc139163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 04:15:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195bce90b1707cb6f414c434f6348a2daa6c8bce4b713a9a1fa52e0d024305de`  
		Last Modified: Tue, 09 Feb 2021 04:20:29 GMT  
		Size: 138.9 MB (138939518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:bb7704cbafeb7d923de33db68ef4e02e9f94841b0e32fe829efd4fdecbed3fae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214460698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ebdb4f4808487be7fd9c23f9913d029636f61c776e8e029e88f16f3816ff0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 06:29:59 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b073e05819fa9a1049e7fafecd7017e92c5ed02402cc0c054eaa6eaf60ff70`  
		Last Modified: Tue, 09 Feb 2021 06:34:25 GMT  
		Size: 156.6 MB (156583695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:9196cb7af6c2772da7f6ddfec282377c2bb5e772e18830b1904c7919ff5fe995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241671010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db70dec2a082291d4e42c8bc96bb8d8a179f2be44f8f6a7a2e367746b38da63a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 07:25:09 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37e3c3267ba37fca1ca8ec497a3b1da52bdbeb8b2e5e6ffd3cfa0da52318fb`  
		Last Modified: Tue, 09 Feb 2021 07:29:40 GMT  
		Size: 142.5 MB (142513705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:d48033fb4677aeb49fd8d32c65d72f852447b5c4a70259eded4be1b64e6bd216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203359826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6218f591f82b680524575e557e913cc587ef62f97da719fd0b36a91225000d92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 09 Feb 2021 10:19:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ddb78f1e2738129e590d0602d2a6fc879aeffba4a36af01622f8672a0dcba`  
		Last Modified: Tue, 09 Feb 2021 10:36:46 GMT  
		Size: 143.2 MB (143226471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:cc3b0873ea9d6cf7631abde58182ae7e3266d072440468c0f8f14279f6d813cd
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
$ docker pull mono@sha256:b345a98aec0b4f580217cf5942edb8488256edc63993c0f20c99f6f9be121941
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94475767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0a397518e81c5082088c3bee32a7aa6119d22d3096f451847d08edea876099`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:29:48 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:29:58 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:30:51 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3434c98e4e9d123f2bcc5d31e6bddf026c80ecfbd23aaddffdb04ba328e964d`  
		Last Modified: Tue, 09 Feb 2021 06:48:56 GMT  
		Size: 255.9 KB (255919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e2c0c1b064079f811792dbcf7f6373876e299ec9e4eed2a8d410d7f959cdfd`  
		Last Modified: Tue, 09 Feb 2021 06:49:15 GMT  
		Size: 67.1 MB (67124706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8398b92c5c9ef1d23664c131cc481982d148088d6e42f84a8a0070ad44075388
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51644789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15784a653dc26ebe76aa4ee3d2579ec792b224fbe78e00ecf4e8198fdbd8ce18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:02 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde96ceb106b030b6613e2af7b31392ff5411289b30d0edc47bcb0aa0824fdc6`  
		Last Modified: Tue, 09 Feb 2021 04:19:25 GMT  
		Size: 256.0 KB (255987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa46d2afe21de1e8348272585b0d67b372fce53c9c5230ad311bb05d3ff11fc1`  
		Last Modified: Tue, 09 Feb 2021 04:19:35 GMT  
		Size: 26.5 MB (26549505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:0a95ecd350ee8679ab79ea59d0e4988d3410469917f8c16e3c330acfc0dc0e88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f18c744ee67ee6ee2cfd81cffcab55fde0eb2c114377b949cea02c6d2327c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:10:05 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 04:10:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 04:11:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a906447c1220d30ffea79fadacfcae391956bad432fc9108918dd6af372016a`  
		Last Modified: Tue, 09 Feb 2021 04:18:57 GMT  
		Size: 256.0 KB (255974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b655366d8c9d647313d81578488f9a534872067e3c4fd502a12606fbd4025`  
		Last Modified: Tue, 09 Feb 2021 04:19:06 GMT  
		Size: 25.7 MB (25738452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:7cb672dd0eddc8de2299f3f3a4db421e2102a0c0ee87f9d79813f7a644681def
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57877003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8fd3521c313c83971ba466f58c9c2c68acbfe89c7a18b673f651683ce52e8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:25:34 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 06:25:51 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 06:26:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9711602173a6c4fc34ad7980c64f84c4cad1f78adf812c78ea5253de1e48`  
		Last Modified: Tue, 09 Feb 2021 06:32:47 GMT  
		Size: 255.9 KB (255934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da2ec84d677d7f20faf6ff61fbdd9b28e35b7e4f2082e082930a803f5ecbe4`  
		Last Modified: Tue, 09 Feb 2021 06:32:56 GMT  
		Size: 31.8 MB (31769620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:6c70f99d482b74150529414bd636340db13762b3c23f15db1cddeb8852e57a1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541135733b9c041f4723379541c34d3e9e24d001231dabeb20d67ef893bc275e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:19:47 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 07:19:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 07:20:48 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388b5008732405ac86289f0e94ff85285339364c6d144ec9205eb77b9f791b0`  
		Last Modified: Tue, 09 Feb 2021 07:27:50 GMT  
		Size: 255.9 KB (255852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5e2aa8ccc877af5d7052d5f552bd27201f21994387b4d4bf2216734aca07d6`  
		Last Modified: Tue, 09 Feb 2021 07:28:13 GMT  
		Size: 71.1 MB (71148722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:00ce59b7eb2ae15020879cfe2b8b2d12ba61658cdc561287172a16095e12ba03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60133355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41039e5dd5571a5a495222c463a380f6334e74f17fe769b616ed5eec4364b91`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 09:56:19 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 09 Feb 2021 09:58:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 09 Feb 2021 10:01:08 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e55e70a3215bcf0881838b631c8f50bec76f06e0170e7a3c21a4add21fcf61`  
		Last Modified: Tue, 09 Feb 2021 10:35:32 GMT  
		Size: 256.3 KB (256273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a431f3a2300c062cd1e6a171fec0d99a4a4fb64e0dd6bc6716cc5972f0d9ff8`  
		Last Modified: Tue, 09 Feb 2021 10:35:39 GMT  
		Size: 29.4 MB (29357573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
