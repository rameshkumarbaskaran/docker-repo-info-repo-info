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
$ docker pull mono@sha256:95939f6a108a97b92df0aad61cfabdd3a0a18ad39533729119c58caa4c5cf3c8
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
$ docker pull mono@sha256:48da387d38afec20165754e6adf264eafd08fa12ae4ce3780b75d6dba22f38f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235965053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777317da614ea8bf50fbc6bc71686d06e57c2c5b4ba8b359c23e5103734e72a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:40:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5d9356f775d18751fb7820029948fa58b9d6ba26cd819e0b42a0a7331ee6a`  
		Last Modified: Wed, 31 Mar 2021 04:48:16 GMT  
		Size: 141.4 MB (141440749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:c1018cc74bfac980315c3d606d6614e31099f0715fc1939fe75c17ac72e7fdf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75659769146021e6b9ed2ebdbb8b250a55bd699b06e904f0f902a936c41807db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:05:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41835d228f7030fcede189a173bd594d51881369bd5413aadec2cd6caaf6b90`  
		Last Modified: Tue, 30 Mar 2021 23:10:16 GMT  
		Size: 140.1 MB (140108559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:37bed4aae0165bf8cdc2ec35cda4585aa3d45675d6210cc2b5e4a99b27a995d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187672912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba418b8af22818a8aaaa279b7b2f7808af5c9f847c1e94d8f9079ce48175839`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:14:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2c49c3ba5fae015dc4d96f60186f4f4130581809c6f9b54c601500bc7876cb`  
		Last Modified: Wed, 31 Mar 2021 02:18:55 GMT  
		Size: 138.9 MB (138938914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ab7191405acfc4ead53f78b16701d311de07615307bfb304bdfbaba1981d3bf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214513849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dd6ff96d37bcb9f3bc1790e37b1d6343f0cfb5b1ed6830cfec063f2fa59e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:44:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7a09d57266a1dda9f6e7aea520280baf520a95c3afc2c94fd5caafcee3499d`  
		Last Modified: Wed, 31 Mar 2021 00:48:45 GMT  
		Size: 156.6 MB (156583801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:f71ffa9e2a24c11ebd07053eecfe0fb8f43fbabeaecedf9bfc77c7d2cd8b7be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241743217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e707d5b2754a3784dfd3b60f01aa8ac01f96336d4185936572cd82ff537ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:04:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0459dd9be36d8cb55c9982a60ab9750af9f4a3ac029dcae263faaaf7307fd`  
		Last Modified: Wed, 31 Mar 2021 01:09:44 GMT  
		Size: 142.5 MB (142545402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:979e32f7a4f2d88b59ab7a09e438c4f1e3bd3156af0aecbf49b87c5a0dba3810
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203387126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8d1971f212c16d77db8c226a4c03f6e5b8c1ba6ada70b252deb3dd55765c8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:10:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49679dfc81c703dced9e288a562fb5d829ee6a3590d634713af480bd29f539f6`  
		Last Modified: Wed, 31 Mar 2021 09:29:00 GMT  
		Size: 143.2 MB (143226383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:198e28d9dd67ca2005de1c04322ba6c5ae49339bc8515a287594a908352e2df4
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
$ docker pull mono@sha256:1689a87b5899086fbb5ea9e41775f31d614428e9896847a2b4ce92344eb18479
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94524304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b12d1e4dc8986186fccd56af26a97086e8dac777daea17e5c8207d476a14d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:354f5dee981224e43d3c3ba0e19e556ef6b3ce22f7b0c23dd9b6d38897f667f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373fb5887f45d2b5c2a5e7e92126a3dadce297976945037453fcc1d3b8e9e06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:30f03097f8ece841862858920c078668a55f8a704b40575d371a02567f4fb9af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48733998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb4c3005f816a12b4da50d92fa9e723451478662bba36ab8d05d920ad45398`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c77bf99637e0a5ecf54b8d0ea09285a37a46404b086b34faccd81d89263eacca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57930048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a31d2b4fab70ba604f33d6a733093d0a579233c5728ab83e7dd40f825e78e8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:3b2e86f199e62d0e369b22c2d2fb5efd5f2cbd81e826bbd665d781fd4ae63f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f5bd1353b65ee76104817fd0a098f7e3cc0acddabfd98f5721c8137a399ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:5ee949613d4f06ee0710ee610ab2587c0227ef868f0e1b81c1e3856b636e6df1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523d9a67b23dcea8e33d00d873dc6fbcb88185ab6cf6d8a5428adf97d429bef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:7a77b4c1042130cea1593653a1377e3ea24a88be836eb9501dec8e1b96e0f999
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
$ docker pull mono@sha256:c462a4a69cd014a50871ef739bb7cfeee4d34bb79276fb7d8644931dc83be330
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224840980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ec088d8b412757cf10d2f3a3b726ceaa3167cf1e9d185c5dde3ba99e969945`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:33:37 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 04:33:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:34:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:46:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66fbcae6ea823fca44c6722b23050a94f9e5eae7e5e5f0ad0aa39501aad7d4`  
		Last Modified: Wed, 31 Mar 2021 04:47:21 GMT  
		Size: 256.1 KB (256061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967cca2e1d645a524966e20f59d8dc0a0ddbead6587bf7ffeff8f4c242680f8`  
		Last Modified: Wed, 31 Mar 2021 04:47:36 GMT  
		Size: 67.1 MB (67147993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc22743b7d503121cb758d28ad4db76e3dafa5bc25c58f01dde785975df0395`  
		Last Modified: Wed, 31 Mar 2021 04:49:04 GMT  
		Size: 130.3 MB (130297633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:a96c48e2debbf3487a6c1bf42a36e631acb3a46b181bed4d2afa324cae4a52e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180665999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e1175a89b4b4e454045f44578c7bcf103f1a6396a5431fff8d47cc102b263f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:01:06 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 30 Mar 2021 23:01:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:02:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:08:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96089afd24199f535d6df683228886f03eb5d1f4c599f734fd8c25dc66f73e4c`  
		Last Modified: Tue, 30 Mar 2021 23:09:04 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d9197acc7de794f7ffe3098a1736f1cc74bb200b0c8fdcedba72b84a94d19`  
		Last Modified: Tue, 30 Mar 2021 23:09:13 GMT  
		Size: 26.6 MB (26574726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233fd67c30510a2d7d52db4c6cbfd5e5b7d9d7aa8510dfa00b0478e4441df6ce`  
		Last Modified: Tue, 30 Mar 2021 23:11:15 GMT  
		Size: 129.0 MB (128962097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:b6747ad91143adb3d5df1027df51b2765a657bf50a9d5140e2bb895a70102c48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176585609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644d661608a7536b936de83122aee7fcaef9f216b3a15e7e9248b9b070bf629`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:10:40 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 02:11:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:11:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:16:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcffbd0eb1fb67e9d80392c801b9053eeaba02385589f35159d652f1a9daa80`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 256.0 KB (256002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ee187d463afd28541d1479883f9433458dd86374e755c83f60a7f59503e82`  
		Last Modified: Wed, 31 Mar 2021 02:17:57 GMT  
		Size: 25.8 MB (25775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029d2f4e5dc65dc273d53eea2195e5fd9814523ca293609f218432ee18a631ed`  
		Last Modified: Wed, 31 Mar 2021 02:19:49 GMT  
		Size: 127.8 MB (127814187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:37bc8b87788fe24dfa48ee7818ad82ba531a1d635bd8e4fbc0fef8b43b811004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203400936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d8ea9373302c8c7abe6210a189c55a3aabccd6b32411d01315b82493fe4642`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:40:30 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 00:40:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:41:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:46:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e90dba5d1418ac149ffc0c0011dff7202da38e0a89e27096c6a4c610297ec`  
		Last Modified: Wed, 31 Mar 2021 00:47:34 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aad1c64a94b8f8895bfe4c0e02822cb382baddd69862132e1d673b59f6b4dc`  
		Last Modified: Wed, 31 Mar 2021 00:47:44 GMT  
		Size: 31.8 MB (31790742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f56903157f7bcd56fe4cada607621a3d52eb32e5774dfb2ffad42991f7dabc`  
		Last Modified: Wed, 31 Mar 2021 00:49:39 GMT  
		Size: 145.4 MB (145449730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:06a735489b97d9bba2beaa3b4de41ad471a6dd84e3d0438af9a9a209c22959cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230630062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5948814f2ce465514de0817a8e8e79c433d1e353ac2be38e32614be905a1380f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:01:15 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 01:01:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:02:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:06:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7bbba408068aee15cc039bb6eeac8d1d4e3e6a0c143a32afc4ae00999646c7`  
		Last Modified: Wed, 31 Mar 2021 01:08:40 GMT  
		Size: 255.9 KB (255947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86784460a62e2d6d80d17d363a5ddfa9adfc67b75ef42a2f279ddbe341ea1b11`  
		Last Modified: Wed, 31 Mar 2021 01:08:53 GMT  
		Size: 71.2 MB (71178041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eaf840d66fd4fe3421c26301c2f4c59a7ed6d7db7d59164c0219a187f4da71`  
		Last Modified: Wed, 31 Mar 2021 01:10:53 GMT  
		Size: 131.4 MB (131407078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:e5874c86cafbe5bc27f52492ca4c0790a2e6d7eaf465262a958e904bd55f3c94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192175128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39abe50e97a0ef18ecd753439ca72b66323307fb9dc0531f24784a7b247a091a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:52:55 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 08:55:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:57:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:27:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488d4ffc99cd2680dbe337a75c9de243d3364b4b4e40db2e449d99b1ab7685d`  
		Last Modified: Wed, 31 Mar 2021 09:28:10 GMT  
		Size: 256.3 KB (256270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae38eeaf30139b9022d3e9b63f5c40bed3883f5b585e7339333cee53e992a54`  
		Last Modified: Wed, 31 Mar 2021 09:28:15 GMT  
		Size: 29.4 MB (29393631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0296b80e6cb45d1b48ab7f533fe3550ce6bfa996d506d8f7dbf90df557b3b78`  
		Last Modified: Wed, 31 Mar 2021 09:29:50 GMT  
		Size: 132.0 MB (131979320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:c422a2093dd075d378891fe91bdfbb71104e95bd5f834c8c2d041d5c35d70889
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
$ docker pull mono@sha256:4396a4cdebaed49b364970ecd4cdb3fc4c1fa9a70f6b37cc0ba66a679eb2d843
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94543347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d60e5c0fdfa843201ec6eb0aefb9fe0ae970926ebd49ddff76513f5f69d1612`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:33:37 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 04:33:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:34:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66fbcae6ea823fca44c6722b23050a94f9e5eae7e5e5f0ad0aa39501aad7d4`  
		Last Modified: Wed, 31 Mar 2021 04:47:21 GMT  
		Size: 256.1 KB (256061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967cca2e1d645a524966e20f59d8dc0a0ddbead6587bf7ffeff8f4c242680f8`  
		Last Modified: Wed, 31 Mar 2021 04:47:36 GMT  
		Size: 67.1 MB (67147993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bde7f874f3b8c007b4a20caa4bcb6b11afa494af311b3430f87e826eac5738bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51703902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334fa59a4aa99e043269ccb4287539de0b24723947a41d9345fbdbf839fc50ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:01:06 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 30 Mar 2021 23:01:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:02:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96089afd24199f535d6df683228886f03eb5d1f4c599f734fd8c25dc66f73e4c`  
		Last Modified: Tue, 30 Mar 2021 23:09:04 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d9197acc7de794f7ffe3098a1736f1cc74bb200b0c8fdcedba72b84a94d19`  
		Last Modified: Tue, 30 Mar 2021 23:09:13 GMT  
		Size: 26.6 MB (26574726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:8bc07f97d84ba8798455317f6f6abfb517e638ec3879f74974f4beebb4dc6c5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cd6a4ebe817569298dcfd290ef92063ddcfd8fdf9e8da43605fc2356110e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:10:40 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 02:11:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:11:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcffbd0eb1fb67e9d80392c801b9053eeaba02385589f35159d652f1a9daa80`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 256.0 KB (256002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ee187d463afd28541d1479883f9433458dd86374e755c83f60a7f59503e82`  
		Last Modified: Wed, 31 Mar 2021 02:17:57 GMT  
		Size: 25.8 MB (25775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b40ebf91cde0bc479c9dc92ab9d25f447411abaa7ff9665d52c10cc7d50d1b8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57951206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c52f84e37b83b6c49b8998de6590981fd985f22dd04ce577d9f82c07ac84a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:40:30 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 00:40:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:41:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e90dba5d1418ac149ffc0c0011dff7202da38e0a89e27096c6a4c610297ec`  
		Last Modified: Wed, 31 Mar 2021 00:47:34 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aad1c64a94b8f8895bfe4c0e02822cb382baddd69862132e1d673b59f6b4dc`  
		Last Modified: Wed, 31 Mar 2021 00:47:44 GMT  
		Size: 31.8 MB (31790742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:21d127a4a2b9a913c46919bc150193336ba3b5c34e8591b5812776b1b844dffc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99222984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf2d0a8296f8617e8593b482a5badd2e46e735b09c1b3ba26c40ce33e26226c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:01:15 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 01:01:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:02:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7bbba408068aee15cc039bb6eeac8d1d4e3e6a0c143a32afc4ae00999646c7`  
		Last Modified: Wed, 31 Mar 2021 01:08:40 GMT  
		Size: 255.9 KB (255947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86784460a62e2d6d80d17d363a5ddfa9adfc67b75ef42a2f279ddbe341ea1b11`  
		Last Modified: Wed, 31 Mar 2021 01:08:53 GMT  
		Size: 71.2 MB (71178041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:bb00e308c1db7977ff88064bbcb7084d02669416367d56c85e2f72a8260f3619
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60195808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff6d8e8b13f6561348c1c79c414c173d1e9b797d78d79e1cc5c1d9087791be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:52:55 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 08:55:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:57:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488d4ffc99cd2680dbe337a75c9de243d3364b4b4e40db2e449d99b1ab7685d`  
		Last Modified: Wed, 31 Mar 2021 09:28:10 GMT  
		Size: 256.3 KB (256270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae38eeaf30139b9022d3e9b63f5c40bed3883f5b585e7339333cee53e992a54`  
		Last Modified: Wed, 31 Mar 2021 09:28:15 GMT  
		Size: 29.4 MB (29393631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:7a77b4c1042130cea1593653a1377e3ea24a88be836eb9501dec8e1b96e0f999
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
$ docker pull mono@sha256:c462a4a69cd014a50871ef739bb7cfeee4d34bb79276fb7d8644931dc83be330
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224840980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ec088d8b412757cf10d2f3a3b726ceaa3167cf1e9d185c5dde3ba99e969945`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:33:37 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 04:33:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:34:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:46:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66fbcae6ea823fca44c6722b23050a94f9e5eae7e5e5f0ad0aa39501aad7d4`  
		Last Modified: Wed, 31 Mar 2021 04:47:21 GMT  
		Size: 256.1 KB (256061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967cca2e1d645a524966e20f59d8dc0a0ddbead6587bf7ffeff8f4c242680f8`  
		Last Modified: Wed, 31 Mar 2021 04:47:36 GMT  
		Size: 67.1 MB (67147993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc22743b7d503121cb758d28ad4db76e3dafa5bc25c58f01dde785975df0395`  
		Last Modified: Wed, 31 Mar 2021 04:49:04 GMT  
		Size: 130.3 MB (130297633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:a96c48e2debbf3487a6c1bf42a36e631acb3a46b181bed4d2afa324cae4a52e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180665999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e1175a89b4b4e454045f44578c7bcf103f1a6396a5431fff8d47cc102b263f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:01:06 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 30 Mar 2021 23:01:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:02:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:08:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96089afd24199f535d6df683228886f03eb5d1f4c599f734fd8c25dc66f73e4c`  
		Last Modified: Tue, 30 Mar 2021 23:09:04 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d9197acc7de794f7ffe3098a1736f1cc74bb200b0c8fdcedba72b84a94d19`  
		Last Modified: Tue, 30 Mar 2021 23:09:13 GMT  
		Size: 26.6 MB (26574726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233fd67c30510a2d7d52db4c6cbfd5e5b7d9d7aa8510dfa00b0478e4441df6ce`  
		Last Modified: Tue, 30 Mar 2021 23:11:15 GMT  
		Size: 129.0 MB (128962097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:b6747ad91143adb3d5df1027df51b2765a657bf50a9d5140e2bb895a70102c48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176585609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644d661608a7536b936de83122aee7fcaef9f216b3a15e7e9248b9b070bf629`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:10:40 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 02:11:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:11:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:16:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcffbd0eb1fb67e9d80392c801b9053eeaba02385589f35159d652f1a9daa80`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 256.0 KB (256002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ee187d463afd28541d1479883f9433458dd86374e755c83f60a7f59503e82`  
		Last Modified: Wed, 31 Mar 2021 02:17:57 GMT  
		Size: 25.8 MB (25775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029d2f4e5dc65dc273d53eea2195e5fd9814523ca293609f218432ee18a631ed`  
		Last Modified: Wed, 31 Mar 2021 02:19:49 GMT  
		Size: 127.8 MB (127814187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:37bc8b87788fe24dfa48ee7818ad82ba531a1d635bd8e4fbc0fef8b43b811004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203400936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d8ea9373302c8c7abe6210a189c55a3aabccd6b32411d01315b82493fe4642`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:40:30 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 00:40:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:41:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:46:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e90dba5d1418ac149ffc0c0011dff7202da38e0a89e27096c6a4c610297ec`  
		Last Modified: Wed, 31 Mar 2021 00:47:34 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aad1c64a94b8f8895bfe4c0e02822cb382baddd69862132e1d673b59f6b4dc`  
		Last Modified: Wed, 31 Mar 2021 00:47:44 GMT  
		Size: 31.8 MB (31790742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f56903157f7bcd56fe4cada607621a3d52eb32e5774dfb2ffad42991f7dabc`  
		Last Modified: Wed, 31 Mar 2021 00:49:39 GMT  
		Size: 145.4 MB (145449730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:06a735489b97d9bba2beaa3b4de41ad471a6dd84e3d0438af9a9a209c22959cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230630062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5948814f2ce465514de0817a8e8e79c433d1e353ac2be38e32614be905a1380f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:01:15 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 01:01:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:02:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:06:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7bbba408068aee15cc039bb6eeac8d1d4e3e6a0c143a32afc4ae00999646c7`  
		Last Modified: Wed, 31 Mar 2021 01:08:40 GMT  
		Size: 255.9 KB (255947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86784460a62e2d6d80d17d363a5ddfa9adfc67b75ef42a2f279ddbe341ea1b11`  
		Last Modified: Wed, 31 Mar 2021 01:08:53 GMT  
		Size: 71.2 MB (71178041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eaf840d66fd4fe3421c26301c2f4c59a7ed6d7db7d59164c0219a187f4da71`  
		Last Modified: Wed, 31 Mar 2021 01:10:53 GMT  
		Size: 131.4 MB (131407078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:e5874c86cafbe5bc27f52492ca4c0790a2e6d7eaf465262a958e904bd55f3c94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192175128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39abe50e97a0ef18ecd753439ca72b66323307fb9dc0531f24784a7b247a091a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:52:55 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 08:55:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:57:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:27:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488d4ffc99cd2680dbe337a75c9de243d3364b4b4e40db2e449d99b1ab7685d`  
		Last Modified: Wed, 31 Mar 2021 09:28:10 GMT  
		Size: 256.3 KB (256270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae38eeaf30139b9022d3e9b63f5c40bed3883f5b585e7339333cee53e992a54`  
		Last Modified: Wed, 31 Mar 2021 09:28:15 GMT  
		Size: 29.4 MB (29393631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0296b80e6cb45d1b48ab7f533fe3550ce6bfa996d506d8f7dbf90df557b3b78`  
		Last Modified: Wed, 31 Mar 2021 09:29:50 GMT  
		Size: 132.0 MB (131979320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:c422a2093dd075d378891fe91bdfbb71104e95bd5f834c8c2d041d5c35d70889
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
$ docker pull mono@sha256:4396a4cdebaed49b364970ecd4cdb3fc4c1fa9a70f6b37cc0ba66a679eb2d843
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94543347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d60e5c0fdfa843201ec6eb0aefb9fe0ae970926ebd49ddff76513f5f69d1612`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:33:37 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 04:33:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:34:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66fbcae6ea823fca44c6722b23050a94f9e5eae7e5e5f0ad0aa39501aad7d4`  
		Last Modified: Wed, 31 Mar 2021 04:47:21 GMT  
		Size: 256.1 KB (256061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967cca2e1d645a524966e20f59d8dc0a0ddbead6587bf7ffeff8f4c242680f8`  
		Last Modified: Wed, 31 Mar 2021 04:47:36 GMT  
		Size: 67.1 MB (67147993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bde7f874f3b8c007b4a20caa4bcb6b11afa494af311b3430f87e826eac5738bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51703902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334fa59a4aa99e043269ccb4287539de0b24723947a41d9345fbdbf839fc50ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:01:06 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 30 Mar 2021 23:01:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:02:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96089afd24199f535d6df683228886f03eb5d1f4c599f734fd8c25dc66f73e4c`  
		Last Modified: Tue, 30 Mar 2021 23:09:04 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d9197acc7de794f7ffe3098a1736f1cc74bb200b0c8fdcedba72b84a94d19`  
		Last Modified: Tue, 30 Mar 2021 23:09:13 GMT  
		Size: 26.6 MB (26574726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:8bc07f97d84ba8798455317f6f6abfb517e638ec3879f74974f4beebb4dc6c5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cd6a4ebe817569298dcfd290ef92063ddcfd8fdf9e8da43605fc2356110e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:10:40 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 02:11:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:11:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcffbd0eb1fb67e9d80392c801b9053eeaba02385589f35159d652f1a9daa80`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 256.0 KB (256002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ee187d463afd28541d1479883f9433458dd86374e755c83f60a7f59503e82`  
		Last Modified: Wed, 31 Mar 2021 02:17:57 GMT  
		Size: 25.8 MB (25775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b40ebf91cde0bc479c9dc92ab9d25f447411abaa7ff9665d52c10cc7d50d1b8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57951206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c52f84e37b83b6c49b8998de6590981fd985f22dd04ce577d9f82c07ac84a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:40:30 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 00:40:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:41:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e90dba5d1418ac149ffc0c0011dff7202da38e0a89e27096c6a4c610297ec`  
		Last Modified: Wed, 31 Mar 2021 00:47:34 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aad1c64a94b8f8895bfe4c0e02822cb382baddd69862132e1d673b59f6b4dc`  
		Last Modified: Wed, 31 Mar 2021 00:47:44 GMT  
		Size: 31.8 MB (31790742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:21d127a4a2b9a913c46919bc150193336ba3b5c34e8591b5812776b1b844dffc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99222984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf2d0a8296f8617e8593b482a5badd2e46e735b09c1b3ba26c40ce33e26226c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:01:15 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 01:01:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:02:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7bbba408068aee15cc039bb6eeac8d1d4e3e6a0c143a32afc4ae00999646c7`  
		Last Modified: Wed, 31 Mar 2021 01:08:40 GMT  
		Size: 255.9 KB (255947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86784460a62e2d6d80d17d363a5ddfa9adfc67b75ef42a2f279ddbe341ea1b11`  
		Last Modified: Wed, 31 Mar 2021 01:08:53 GMT  
		Size: 71.2 MB (71178041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:bb00e308c1db7977ff88064bbcb7084d02669416367d56c85e2f72a8260f3619
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60195808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff6d8e8b13f6561348c1c79c414c173d1e9b797d78d79e1cc5c1d9087791be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:52:55 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 08:55:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:57:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488d4ffc99cd2680dbe337a75c9de243d3364b4b4e40db2e449d99b1ab7685d`  
		Last Modified: Wed, 31 Mar 2021 09:28:10 GMT  
		Size: 256.3 KB (256270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae38eeaf30139b9022d3e9b63f5c40bed3883f5b585e7339333cee53e992a54`  
		Last Modified: Wed, 31 Mar 2021 09:28:15 GMT  
		Size: 29.4 MB (29393631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:7a77b4c1042130cea1593653a1377e3ea24a88be836eb9501dec8e1b96e0f999
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
$ docker pull mono@sha256:c462a4a69cd014a50871ef739bb7cfeee4d34bb79276fb7d8644931dc83be330
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224840980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ec088d8b412757cf10d2f3a3b726ceaa3167cf1e9d185c5dde3ba99e969945`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:33:37 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 04:33:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:34:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:46:08 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66fbcae6ea823fca44c6722b23050a94f9e5eae7e5e5f0ad0aa39501aad7d4`  
		Last Modified: Wed, 31 Mar 2021 04:47:21 GMT  
		Size: 256.1 KB (256061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967cca2e1d645a524966e20f59d8dc0a0ddbead6587bf7ffeff8f4c242680f8`  
		Last Modified: Wed, 31 Mar 2021 04:47:36 GMT  
		Size: 67.1 MB (67147993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc22743b7d503121cb758d28ad4db76e3dafa5bc25c58f01dde785975df0395`  
		Last Modified: Wed, 31 Mar 2021 04:49:04 GMT  
		Size: 130.3 MB (130297633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:a96c48e2debbf3487a6c1bf42a36e631acb3a46b181bed4d2afa324cae4a52e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180665999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e1175a89b4b4e454045f44578c7bcf103f1a6396a5431fff8d47cc102b263f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:01:06 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 30 Mar 2021 23:01:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:02:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:08:01 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96089afd24199f535d6df683228886f03eb5d1f4c599f734fd8c25dc66f73e4c`  
		Last Modified: Tue, 30 Mar 2021 23:09:04 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d9197acc7de794f7ffe3098a1736f1cc74bb200b0c8fdcedba72b84a94d19`  
		Last Modified: Tue, 30 Mar 2021 23:09:13 GMT  
		Size: 26.6 MB (26574726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233fd67c30510a2d7d52db4c6cbfd5e5b7d9d7aa8510dfa00b0478e4441df6ce`  
		Last Modified: Tue, 30 Mar 2021 23:11:15 GMT  
		Size: 129.0 MB (128962097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:b6747ad91143adb3d5df1027df51b2765a657bf50a9d5140e2bb895a70102c48
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176585609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644d661608a7536b936de83122aee7fcaef9f216b3a15e7e9248b9b070bf629`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:10:40 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 02:11:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:11:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:16:47 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcffbd0eb1fb67e9d80392c801b9053eeaba02385589f35159d652f1a9daa80`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 256.0 KB (256002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ee187d463afd28541d1479883f9433458dd86374e755c83f60a7f59503e82`  
		Last Modified: Wed, 31 Mar 2021 02:17:57 GMT  
		Size: 25.8 MB (25775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029d2f4e5dc65dc273d53eea2195e5fd9814523ca293609f218432ee18a631ed`  
		Last Modified: Wed, 31 Mar 2021 02:19:49 GMT  
		Size: 127.8 MB (127814187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:37bc8b87788fe24dfa48ee7818ad82ba531a1d635bd8e4fbc0fef8b43b811004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203400936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d8ea9373302c8c7abe6210a189c55a3aabccd6b32411d01315b82493fe4642`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:40:30 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 00:40:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:41:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:46:26 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e90dba5d1418ac149ffc0c0011dff7202da38e0a89e27096c6a4c610297ec`  
		Last Modified: Wed, 31 Mar 2021 00:47:34 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aad1c64a94b8f8895bfe4c0e02822cb382baddd69862132e1d673b59f6b4dc`  
		Last Modified: Wed, 31 Mar 2021 00:47:44 GMT  
		Size: 31.8 MB (31790742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f56903157f7bcd56fe4cada607621a3d52eb32e5774dfb2ffad42991f7dabc`  
		Last Modified: Wed, 31 Mar 2021 00:49:39 GMT  
		Size: 145.4 MB (145449730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:06a735489b97d9bba2beaa3b4de41ad471a6dd84e3d0438af9a9a209c22959cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230630062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5948814f2ce465514de0817a8e8e79c433d1e353ac2be38e32614be905a1380f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:01:15 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 01:01:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:02:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:06:42 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7bbba408068aee15cc039bb6eeac8d1d4e3e6a0c143a32afc4ae00999646c7`  
		Last Modified: Wed, 31 Mar 2021 01:08:40 GMT  
		Size: 255.9 KB (255947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86784460a62e2d6d80d17d363a5ddfa9adfc67b75ef42a2f279ddbe341ea1b11`  
		Last Modified: Wed, 31 Mar 2021 01:08:53 GMT  
		Size: 71.2 MB (71178041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eaf840d66fd4fe3421c26301c2f4c59a7ed6d7db7d59164c0219a187f4da71`  
		Last Modified: Wed, 31 Mar 2021 01:10:53 GMT  
		Size: 131.4 MB (131407078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:e5874c86cafbe5bc27f52492ca4c0790a2e6d7eaf465262a958e904bd55f3c94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192175128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39abe50e97a0ef18ecd753439ca72b66323307fb9dc0531f24784a7b247a091a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:52:55 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 08:55:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:57:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:27:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488d4ffc99cd2680dbe337a75c9de243d3364b4b4e40db2e449d99b1ab7685d`  
		Last Modified: Wed, 31 Mar 2021 09:28:10 GMT  
		Size: 256.3 KB (256270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae38eeaf30139b9022d3e9b63f5c40bed3883f5b585e7339333cee53e992a54`  
		Last Modified: Wed, 31 Mar 2021 09:28:15 GMT  
		Size: 29.4 MB (29393631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0296b80e6cb45d1b48ab7f533fe3550ce6bfa996d506d8f7dbf90df557b3b78`  
		Last Modified: Wed, 31 Mar 2021 09:29:50 GMT  
		Size: 132.0 MB (131979320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:c422a2093dd075d378891fe91bdfbb71104e95bd5f834c8c2d041d5c35d70889
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
$ docker pull mono@sha256:4396a4cdebaed49b364970ecd4cdb3fc4c1fa9a70f6b37cc0ba66a679eb2d843
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94543347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d60e5c0fdfa843201ec6eb0aefb9fe0ae970926ebd49ddff76513f5f69d1612`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:33:37 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 04:33:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:34:16 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66fbcae6ea823fca44c6722b23050a94f9e5eae7e5e5f0ad0aa39501aad7d4`  
		Last Modified: Wed, 31 Mar 2021 04:47:21 GMT  
		Size: 256.1 KB (256061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967cca2e1d645a524966e20f59d8dc0a0ddbead6587bf7ffeff8f4c242680f8`  
		Last Modified: Wed, 31 Mar 2021 04:47:36 GMT  
		Size: 67.1 MB (67147993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:bde7f874f3b8c007b4a20caa4bcb6b11afa494af311b3430f87e826eac5738bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51703902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334fa59a4aa99e043269ccb4287539de0b24723947a41d9345fbdbf839fc50ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:01:06 GMT
ENV MONO_VERSION=6.10.0.104
# Tue, 30 Mar 2021 23:01:28 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:02:15 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96089afd24199f535d6df683228886f03eb5d1f4c599f734fd8c25dc66f73e4c`  
		Last Modified: Tue, 30 Mar 2021 23:09:04 GMT  
		Size: 256.0 KB (255962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d9197acc7de794f7ffe3098a1736f1cc74bb200b0c8fdcedba72b84a94d19`  
		Last Modified: Tue, 30 Mar 2021 23:09:13 GMT  
		Size: 26.6 MB (26574726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:8bc07f97d84ba8798455317f6f6abfb517e638ec3879f74974f4beebb4dc6c5d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64cd6a4ebe817569298dcfd290ef92063ddcfd8fdf9e8da43605fc2356110e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:10:40 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 02:11:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:11:41 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcffbd0eb1fb67e9d80392c801b9053eeaba02385589f35159d652f1a9daa80`  
		Last Modified: Wed, 31 Mar 2021 02:17:47 GMT  
		Size: 256.0 KB (256002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ee187d463afd28541d1479883f9433458dd86374e755c83f60a7f59503e82`  
		Last Modified: Wed, 31 Mar 2021 02:17:57 GMT  
		Size: 25.8 MB (25775606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b40ebf91cde0bc479c9dc92ab9d25f447411abaa7ff9665d52c10cc7d50d1b8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57951206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c52f84e37b83b6c49b8998de6590981fd985f22dd04ce577d9f82c07ac84a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:40:30 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 00:40:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:41:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e90dba5d1418ac149ffc0c0011dff7202da38e0a89e27096c6a4c610297ec`  
		Last Modified: Wed, 31 Mar 2021 00:47:34 GMT  
		Size: 256.0 KB (255951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aad1c64a94b8f8895bfe4c0e02822cb382baddd69862132e1d673b59f6b4dc`  
		Last Modified: Wed, 31 Mar 2021 00:47:44 GMT  
		Size: 31.8 MB (31790742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:21d127a4a2b9a913c46919bc150193336ba3b5c34e8591b5812776b1b844dffc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99222984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf2d0a8296f8617e8593b482a5badd2e46e735b09c1b3ba26c40ce33e26226c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:01:15 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 01:01:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:02:12 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7bbba408068aee15cc039bb6eeac8d1d4e3e6a0c143a32afc4ae00999646c7`  
		Last Modified: Wed, 31 Mar 2021 01:08:40 GMT  
		Size: 255.9 KB (255947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86784460a62e2d6d80d17d363a5ddfa9adfc67b75ef42a2f279ddbe341ea1b11`  
		Last Modified: Wed, 31 Mar 2021 01:08:53 GMT  
		Size: 71.2 MB (71178041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:bb00e308c1db7977ff88064bbcb7084d02669416367d56c85e2f72a8260f3619
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60195808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff6d8e8b13f6561348c1c79c414c173d1e9b797d78d79e1cc5c1d9087791be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:52:55 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 31 Mar 2021 08:55:29 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:57:28 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488d4ffc99cd2680dbe337a75c9de243d3364b4b4e40db2e449d99b1ab7685d`  
		Last Modified: Wed, 31 Mar 2021 09:28:10 GMT  
		Size: 256.3 KB (256270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae38eeaf30139b9022d3e9b63f5c40bed3883f5b585e7339333cee53e992a54`  
		Last Modified: Wed, 31 Mar 2021 09:28:15 GMT  
		Size: 29.4 MB (29393631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:95939f6a108a97b92df0aad61cfabdd3a0a18ad39533729119c58caa4c5cf3c8
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
$ docker pull mono@sha256:48da387d38afec20165754e6adf264eafd08fa12ae4ce3780b75d6dba22f38f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235965053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777317da614ea8bf50fbc6bc71686d06e57c2c5b4ba8b359c23e5103734e72a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:40:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5d9356f775d18751fb7820029948fa58b9d6ba26cd819e0b42a0a7331ee6a`  
		Last Modified: Wed, 31 Mar 2021 04:48:16 GMT  
		Size: 141.4 MB (141440749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:c1018cc74bfac980315c3d606d6614e31099f0715fc1939fe75c17ac72e7fdf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75659769146021e6b9ed2ebdbb8b250a55bd699b06e904f0f902a936c41807db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:05:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41835d228f7030fcede189a173bd594d51881369bd5413aadec2cd6caaf6b90`  
		Last Modified: Tue, 30 Mar 2021 23:10:16 GMT  
		Size: 140.1 MB (140108559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:37bed4aae0165bf8cdc2ec35cda4585aa3d45675d6210cc2b5e4a99b27a995d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187672912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba418b8af22818a8aaaa279b7b2f7808af5c9f847c1e94d8f9079ce48175839`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:14:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2c49c3ba5fae015dc4d96f60186f4f4130581809c6f9b54c601500bc7876cb`  
		Last Modified: Wed, 31 Mar 2021 02:18:55 GMT  
		Size: 138.9 MB (138938914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ab7191405acfc4ead53f78b16701d311de07615307bfb304bdfbaba1981d3bf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214513849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dd6ff96d37bcb9f3bc1790e37b1d6343f0cfb5b1ed6830cfec063f2fa59e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:44:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7a09d57266a1dda9f6e7aea520280baf520a95c3afc2c94fd5caafcee3499d`  
		Last Modified: Wed, 31 Mar 2021 00:48:45 GMT  
		Size: 156.6 MB (156583801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:f71ffa9e2a24c11ebd07053eecfe0fb8f43fbabeaecedf9bfc77c7d2cd8b7be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241743217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e707d5b2754a3784dfd3b60f01aa8ac01f96336d4185936572cd82ff537ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:04:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0459dd9be36d8cb55c9982a60ab9750af9f4a3ac029dcae263faaaf7307fd`  
		Last Modified: Wed, 31 Mar 2021 01:09:44 GMT  
		Size: 142.5 MB (142545402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:979e32f7a4f2d88b59ab7a09e438c4f1e3bd3156af0aecbf49b87c5a0dba3810
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203387126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8d1971f212c16d77db8c226a4c03f6e5b8c1ba6ada70b252deb3dd55765c8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:10:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49679dfc81c703dced9e288a562fb5d829ee6a3590d634713af480bd29f539f6`  
		Last Modified: Wed, 31 Mar 2021 09:29:00 GMT  
		Size: 143.2 MB (143226383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:198e28d9dd67ca2005de1c04322ba6c5ae49339bc8515a287594a908352e2df4
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
$ docker pull mono@sha256:1689a87b5899086fbb5ea9e41775f31d614428e9896847a2b4ce92344eb18479
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94524304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b12d1e4dc8986186fccd56af26a97086e8dac777daea17e5c8207d476a14d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:354f5dee981224e43d3c3ba0e19e556ef6b3ce22f7b0c23dd9b6d38897f667f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373fb5887f45d2b5c2a5e7e92126a3dadce297976945037453fcc1d3b8e9e06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:30f03097f8ece841862858920c078668a55f8a704b40575d371a02567f4fb9af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48733998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb4c3005f816a12b4da50d92fa9e723451478662bba36ab8d05d920ad45398`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c77bf99637e0a5ecf54b8d0ea09285a37a46404b086b34faccd81d89263eacca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57930048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a31d2b4fab70ba604f33d6a733093d0a579233c5728ab83e7dd40f825e78e8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:3b2e86f199e62d0e369b22c2d2fb5efd5f2cbd81e826bbd665d781fd4ae63f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f5bd1353b65ee76104817fd0a098f7e3cc0acddabfd98f5721c8137a399ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:5ee949613d4f06ee0710ee610ab2587c0227ef868f0e1b81c1e3856b636e6df1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523d9a67b23dcea8e33d00d873dc6fbcb88185ab6cf6d8a5428adf97d429bef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:95939f6a108a97b92df0aad61cfabdd3a0a18ad39533729119c58caa4c5cf3c8
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
$ docker pull mono@sha256:48da387d38afec20165754e6adf264eafd08fa12ae4ce3780b75d6dba22f38f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235965053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777317da614ea8bf50fbc6bc71686d06e57c2c5b4ba8b359c23e5103734e72a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:40:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5d9356f775d18751fb7820029948fa58b9d6ba26cd819e0b42a0a7331ee6a`  
		Last Modified: Wed, 31 Mar 2021 04:48:16 GMT  
		Size: 141.4 MB (141440749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:c1018cc74bfac980315c3d606d6614e31099f0715fc1939fe75c17ac72e7fdf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75659769146021e6b9ed2ebdbb8b250a55bd699b06e904f0f902a936c41807db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:05:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41835d228f7030fcede189a173bd594d51881369bd5413aadec2cd6caaf6b90`  
		Last Modified: Tue, 30 Mar 2021 23:10:16 GMT  
		Size: 140.1 MB (140108559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:37bed4aae0165bf8cdc2ec35cda4585aa3d45675d6210cc2b5e4a99b27a995d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187672912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba418b8af22818a8aaaa279b7b2f7808af5c9f847c1e94d8f9079ce48175839`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:14:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2c49c3ba5fae015dc4d96f60186f4f4130581809c6f9b54c601500bc7876cb`  
		Last Modified: Wed, 31 Mar 2021 02:18:55 GMT  
		Size: 138.9 MB (138938914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ab7191405acfc4ead53f78b16701d311de07615307bfb304bdfbaba1981d3bf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214513849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dd6ff96d37bcb9f3bc1790e37b1d6343f0cfb5b1ed6830cfec063f2fa59e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:44:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7a09d57266a1dda9f6e7aea520280baf520a95c3afc2c94fd5caafcee3499d`  
		Last Modified: Wed, 31 Mar 2021 00:48:45 GMT  
		Size: 156.6 MB (156583801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:f71ffa9e2a24c11ebd07053eecfe0fb8f43fbabeaecedf9bfc77c7d2cd8b7be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241743217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e707d5b2754a3784dfd3b60f01aa8ac01f96336d4185936572cd82ff537ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:04:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0459dd9be36d8cb55c9982a60ab9750af9f4a3ac029dcae263faaaf7307fd`  
		Last Modified: Wed, 31 Mar 2021 01:09:44 GMT  
		Size: 142.5 MB (142545402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:979e32f7a4f2d88b59ab7a09e438c4f1e3bd3156af0aecbf49b87c5a0dba3810
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203387126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8d1971f212c16d77db8c226a4c03f6e5b8c1ba6ada70b252deb3dd55765c8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:10:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49679dfc81c703dced9e288a562fb5d829ee6a3590d634713af480bd29f539f6`  
		Last Modified: Wed, 31 Mar 2021 09:29:00 GMT  
		Size: 143.2 MB (143226383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:198e28d9dd67ca2005de1c04322ba6c5ae49339bc8515a287594a908352e2df4
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
$ docker pull mono@sha256:1689a87b5899086fbb5ea9e41775f31d614428e9896847a2b4ce92344eb18479
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94524304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b12d1e4dc8986186fccd56af26a97086e8dac777daea17e5c8207d476a14d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:354f5dee981224e43d3c3ba0e19e556ef6b3ce22f7b0c23dd9b6d38897f667f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373fb5887f45d2b5c2a5e7e92126a3dadce297976945037453fcc1d3b8e9e06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:30f03097f8ece841862858920c078668a55f8a704b40575d371a02567f4fb9af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48733998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb4c3005f816a12b4da50d92fa9e723451478662bba36ab8d05d920ad45398`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c77bf99637e0a5ecf54b8d0ea09285a37a46404b086b34faccd81d89263eacca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57930048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a31d2b4fab70ba604f33d6a733093d0a579233c5728ab83e7dd40f825e78e8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:3b2e86f199e62d0e369b22c2d2fb5efd5f2cbd81e826bbd665d781fd4ae63f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f5bd1353b65ee76104817fd0a098f7e3cc0acddabfd98f5721c8137a399ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:5ee949613d4f06ee0710ee610ab2587c0227ef868f0e1b81c1e3856b636e6df1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523d9a67b23dcea8e33d00d873dc6fbcb88185ab6cf6d8a5428adf97d429bef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107`

```console
$ docker pull mono@sha256:95939f6a108a97b92df0aad61cfabdd3a0a18ad39533729119c58caa4c5cf3c8
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
$ docker pull mono@sha256:48da387d38afec20165754e6adf264eafd08fa12ae4ce3780b75d6dba22f38f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235965053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777317da614ea8bf50fbc6bc71686d06e57c2c5b4ba8b359c23e5103734e72a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:40:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5d9356f775d18751fb7820029948fa58b9d6ba26cd819e0b42a0a7331ee6a`  
		Last Modified: Wed, 31 Mar 2021 04:48:16 GMT  
		Size: 141.4 MB (141440749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v5

```console
$ docker pull mono@sha256:c1018cc74bfac980315c3d606d6614e31099f0715fc1939fe75c17ac72e7fdf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75659769146021e6b9ed2ebdbb8b250a55bd699b06e904f0f902a936c41807db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:05:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41835d228f7030fcede189a173bd594d51881369bd5413aadec2cd6caaf6b90`  
		Last Modified: Tue, 30 Mar 2021 23:10:16 GMT  
		Size: 140.1 MB (140108559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm variant v7

```console
$ docker pull mono@sha256:37bed4aae0165bf8cdc2ec35cda4585aa3d45675d6210cc2b5e4a99b27a995d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187672912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba418b8af22818a8aaaa279b7b2f7808af5c9f847c1e94d8f9079ce48175839`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:14:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2c49c3ba5fae015dc4d96f60186f4f4130581809c6f9b54c601500bc7876cb`  
		Last Modified: Wed, 31 Mar 2021 02:18:55 GMT  
		Size: 138.9 MB (138938914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ab7191405acfc4ead53f78b16701d311de07615307bfb304bdfbaba1981d3bf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214513849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dd6ff96d37bcb9f3bc1790e37b1d6343f0cfb5b1ed6830cfec063f2fa59e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:44:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7a09d57266a1dda9f6e7aea520280baf520a95c3afc2c94fd5caafcee3499d`  
		Last Modified: Wed, 31 Mar 2021 00:48:45 GMT  
		Size: 156.6 MB (156583801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; 386

```console
$ docker pull mono@sha256:f71ffa9e2a24c11ebd07053eecfe0fb8f43fbabeaecedf9bfc77c7d2cd8b7be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241743217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e707d5b2754a3784dfd3b60f01aa8ac01f96336d4185936572cd82ff537ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:04:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0459dd9be36d8cb55c9982a60ab9750af9f4a3ac029dcae263faaaf7307fd`  
		Last Modified: Wed, 31 Mar 2021 01:09:44 GMT  
		Size: 142.5 MB (142545402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107` - linux; ppc64le

```console
$ docker pull mono@sha256:979e32f7a4f2d88b59ab7a09e438c4f1e3bd3156af0aecbf49b87c5a0dba3810
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203387126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8d1971f212c16d77db8c226a4c03f6e5b8c1ba6ada70b252deb3dd55765c8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:10:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49679dfc81c703dced9e288a562fb5d829ee6a3590d634713af480bd29f539f6`  
		Last Modified: Wed, 31 Mar 2021 09:29:00 GMT  
		Size: 143.2 MB (143226383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.107-slim`

```console
$ docker pull mono@sha256:198e28d9dd67ca2005de1c04322ba6c5ae49339bc8515a287594a908352e2df4
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
$ docker pull mono@sha256:1689a87b5899086fbb5ea9e41775f31d614428e9896847a2b4ce92344eb18479
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94524304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b12d1e4dc8986186fccd56af26a97086e8dac777daea17e5c8207d476a14d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:354f5dee981224e43d3c3ba0e19e556ef6b3ce22f7b0c23dd9b6d38897f667f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373fb5887f45d2b5c2a5e7e92126a3dadce297976945037453fcc1d3b8e9e06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:30f03097f8ece841862858920c078668a55f8a704b40575d371a02567f4fb9af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48733998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb4c3005f816a12b4da50d92fa9e723451478662bba36ab8d05d920ad45398`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c77bf99637e0a5ecf54b8d0ea09285a37a46404b086b34faccd81d89263eacca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57930048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a31d2b4fab70ba604f33d6a733093d0a579233c5728ab83e7dd40f825e78e8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; 386

```console
$ docker pull mono@sha256:3b2e86f199e62d0e369b22c2d2fb5efd5f2cbd81e826bbd665d781fd4ae63f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f5bd1353b65ee76104817fd0a098f7e3cc0acddabfd98f5721c8137a399ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.107-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:5ee949613d4f06ee0710ee610ab2587c0227ef868f0e1b81c1e3856b636e6df1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523d9a67b23dcea8e33d00d873dc6fbcb88185ab6cf6d8a5428adf97d429bef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:95939f6a108a97b92df0aad61cfabdd3a0a18ad39533729119c58caa4c5cf3c8
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
$ docker pull mono@sha256:48da387d38afec20165754e6adf264eafd08fa12ae4ce3780b75d6dba22f38f8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235965053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777317da614ea8bf50fbc6bc71686d06e57c2c5b4ba8b359c23e5103734e72a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 04:40:06 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5d9356f775d18751fb7820029948fa58b9d6ba26cd819e0b42a0a7331ee6a`  
		Last Modified: Wed, 31 Mar 2021 04:48:16 GMT  
		Size: 141.4 MB (141440749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:c1018cc74bfac980315c3d606d6614e31099f0715fc1939fe75c17ac72e7fdf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75659769146021e6b9ed2ebdbb8b250a55bd699b06e904f0f902a936c41807db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 30 Mar 2021 23:05:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41835d228f7030fcede189a173bd594d51881369bd5413aadec2cd6caaf6b90`  
		Last Modified: Tue, 30 Mar 2021 23:10:16 GMT  
		Size: 140.1 MB (140108559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:37bed4aae0165bf8cdc2ec35cda4585aa3d45675d6210cc2b5e4a99b27a995d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187672912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba418b8af22818a8aaaa279b7b2f7808af5c9f847c1e94d8f9079ce48175839`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 02:14:21 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2c49c3ba5fae015dc4d96f60186f4f4130581809c6f9b54c601500bc7876cb`  
		Last Modified: Wed, 31 Mar 2021 02:18:55 GMT  
		Size: 138.9 MB (138938914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:ab7191405acfc4ead53f78b16701d311de07615307bfb304bdfbaba1981d3bf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214513849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dd6ff96d37bcb9f3bc1790e37b1d6343f0cfb5b1ed6830cfec063f2fa59e53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 00:44:02 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7a09d57266a1dda9f6e7aea520280baf520a95c3afc2c94fd5caafcee3499d`  
		Last Modified: Wed, 31 Mar 2021 00:48:45 GMT  
		Size: 156.6 MB (156583801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:f71ffa9e2a24c11ebd07053eecfe0fb8f43fbabeaecedf9bfc77c7d2cd8b7be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241743217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45e707d5b2754a3784dfd3b60f01aa8ac01f96336d4185936572cd82ff537ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 01:04:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0459dd9be36d8cb55c9982a60ab9750af9f4a3ac029dcae263faaaf7307fd`  
		Last Modified: Wed, 31 Mar 2021 01:09:44 GMT  
		Size: 142.5 MB (142545402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:979e32f7a4f2d88b59ab7a09e438c4f1e3bd3156af0aecbf49b87c5a0dba3810
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203387126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8d1971f212c16d77db8c226a4c03f6e5b8c1ba6ada70b252deb3dd55765c8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Wed, 31 Mar 2021 09:10:51 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49679dfc81c703dced9e288a562fb5d829ee6a3590d634713af480bd29f539f6`  
		Last Modified: Wed, 31 Mar 2021 09:29:00 GMT  
		Size: 143.2 MB (143226383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:198e28d9dd67ca2005de1c04322ba6c5ae49339bc8515a287594a908352e2df4
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
$ docker pull mono@sha256:1689a87b5899086fbb5ea9e41775f31d614428e9896847a2b4ce92344eb18479
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94524304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b12d1e4dc8986186fccd56af26a97086e8dac777daea17e5c8207d476a14d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 04:32:46 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 04:32:56 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 04:33:27 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abffe3eb603097f33c168ba3e6ef84b99a573d5c316193c50e7de6c38ca533`  
		Last Modified: Wed, 31 Mar 2021 04:46:46 GMT  
		Size: 256.1 KB (256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2986bf771ff5efbe852c19b8e92a16b20622ce38db25c9c2b45463067f66f8dc`  
		Last Modified: Wed, 31 Mar 2021 04:47:01 GMT  
		Size: 67.1 MB (67128935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:354f5dee981224e43d3c3ba0e19e556ef6b3ce22f7b0c23dd9b6d38897f667f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373fb5887f45d2b5c2a5e7e92126a3dadce297976945037453fcc1d3b8e9e06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:51:08 GMT
ADD file:779165b34b3be18f6c24e448997bf6497e3b27ff72954fe3cdced0ebcc77b6b8 in / 
# Tue, 30 Mar 2021 21:51:11 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:59:46 GMT
ENV MONO_VERSION=6.12.0.107
# Tue, 30 Mar 2021 23:00:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 30 Mar 2021 23:00:55 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7cbaf854daf876ddd338771dec41777b0dfcad33c1fc8ea3512a0708333e4465`  
		Last Modified: Tue, 30 Mar 2021 21:58:44 GMT  
		Size: 24.9 MB (24873214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecc1879253d988f851b426e45eab1f00dc37e06175a483a2947d82c87ca693a`  
		Last Modified: Tue, 30 Mar 2021 23:08:40 GMT  
		Size: 256.0 KB (255971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0e6c4a26fc503c88bc0ca6e466b49d45bffe4eff185334b88d266c3ff2fac5`  
		Last Modified: Tue, 30 Mar 2021 23:08:51 GMT  
		Size: 26.6 MB (26550096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:30f03097f8ece841862858920c078668a55f8a704b40575d371a02567f4fb9af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48733998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb4c3005f816a12b4da50d92fa9e723451478662bba36ab8d05d920ad45398`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:08:38 GMT
ADD file:c1eeb99fc8ec483e175d4948a58d7f7b246b0d6b887f435a5fef07ef43699f76 in / 
# Tue, 30 Mar 2021 23:08:41 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:09:19 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 02:09:39 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 02:10:22 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ee0a2cc24f2963b99b1d30dc2613f196b7c9e38337cf99332d6c4efe07f01ef2`  
		Last Modified: Tue, 30 Mar 2021 23:16:25 GMT  
		Size: 22.7 MB (22739814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2630b9e89b3f8e8bf5cf459714f0533e6965dd6f7a15c681f983fd753a5052`  
		Last Modified: Wed, 31 Mar 2021 02:17:26 GMT  
		Size: 256.0 KB (256007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688600d68f090a392c73014c7e4218a813575f2ab38e51dbe586c894b269087d`  
		Last Modified: Wed, 31 Mar 2021 02:17:36 GMT  
		Size: 25.7 MB (25738177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c77bf99637e0a5ecf54b8d0ea09285a37a46404b086b34faccd81d89263eacca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57930048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a31d2b4fab70ba604f33d6a733093d0a579233c5728ab83e7dd40f825e78e8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:39:21 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 00:39:40 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 00:40:21 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580211237e340484647d3b7247615a7af051f85cfd9b3f5682bc81b0ad81bf1`  
		Last Modified: Wed, 31 Mar 2021 00:47:06 GMT  
		Size: 256.0 KB (255973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84925b1302919cd20a82a541f5db57fa566b54d5cdc0f88d267859471e0495`  
		Last Modified: Wed, 31 Mar 2021 00:47:13 GMT  
		Size: 31.8 MB (31769562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:3b2e86f199e62d0e369b22c2d2fb5efd5f2cbd81e826bbd665d781fd4ae63f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99197815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f5bd1353b65ee76104817fd0a098f7e3cc0acddabfd98f5721c8137a399ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:39:48 GMT
ADD file:d11c47560c0a88a83a3a0ce5af82fc17a07075e877293e4f922f126959810ea3 in / 
# Tue, 30 Mar 2021 21:39:49 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:00:01 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 01:00:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 01:01:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:548dde0830bd6b881c0c068db5a4e39aa720d2a0c5ac3897296a023dda7b3391`  
		Last Modified: Tue, 30 Mar 2021 21:46:41 GMT  
		Size: 27.8 MB (27788996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98ead88653c863870e7a39eb99edc7de4d043f96c4e0929a8b9b0a9fcb8ae6`  
		Last Modified: Wed, 31 Mar 2021 01:07:58 GMT  
		Size: 256.0 KB (255958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71b5743d08a8b002bb14a919acbb40e11d6f112d1bc1be653046a2e08a28c9d`  
		Last Modified: Wed, 31 Mar 2021 01:08:14 GMT  
		Size: 71.2 MB (71152861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:5ee949613d4f06ee0710ee610ab2587c0227ef868f0e1b81c1e3856b636e6df1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6523d9a67b23dcea8e33d00d873dc6fbcb88185ab6cf6d8a5428adf97d429bef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:03 GMT
ADD file:a544303d3ec263b38c231310d807e05249140188df5c5a5c785b2f176455ac39 in / 
# Tue, 30 Mar 2021 22:36:09 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:00 GMT
ENV MONO_VERSION=6.12.0.107
# Wed, 31 Mar 2021 08:49:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 31 Mar 2021 08:52:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:c840eb5e9aed613b2af7557a4b5ad46898b8bc475a2d470c65ec7896b11282f1`  
		Last Modified: Tue, 30 Mar 2021 22:42:39 GMT  
		Size: 30.5 MB (30545907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0c8391df180c1b3750ebfc75ce9972dbad034c6fb7fecce0919fcbe64a2b57`  
		Last Modified: Wed, 31 Mar 2021 09:27:42 GMT  
		Size: 256.4 KB (256409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee9d42dfafce5578675e0d0b336a094a13abbe35323a941072ee94300adaa53`  
		Last Modified: Wed, 31 Mar 2021 09:27:51 GMT  
		Size: 29.4 MB (29358427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
