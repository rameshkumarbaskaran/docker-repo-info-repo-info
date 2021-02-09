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
