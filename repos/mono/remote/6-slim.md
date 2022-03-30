## `mono:6-slim`

```console
$ docker pull mono@sha256:457a99323d75c4d6704451eebb9223d0ec161f1242ccf8d25a882ef7afacc76c
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
$ docker pull mono@sha256:87038a7da02d5efff3bfab1ec93dc3020d04cd3fad6bff479d3252cf3cb13695
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc621103738e68eb59281907e2ec643435dbb8dd82d504d49655526191a0199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 22:50:30 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 22:50:38 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 22:51:01 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d839cde201cd1385a1c2c927214c614f1cd1bab02a62fd34b6df69e6f95daa7e`  
		Last Modified: Tue, 29 Mar 2022 23:02:05 GMT  
		Size: 2.8 MB (2777377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158befabd0cf5fbeb7cb51a0cfc2f6c20399efe3be6abfd6d7dc8187d886b4a0`  
		Last Modified: Tue, 29 Mar 2022 23:02:14 GMT  
		Size: 64.8 MB (64760477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:2858e2824edbcaaefd73dd8b888c39d6c10cfd27bc7b2b1b420570403b00a924
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51848447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41535ed442f086e8d8103e40ebab589e248cc742505317bfb8c17b5746bc567f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:36 GMT
ADD file:7ac5498e2c44686d7eb272ef7645a0a64486cf942610f6754aa4a932f5b1a4be in / 
# Tue, 29 Mar 2022 00:51:37 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:50:15 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 08:50:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 08:51:31 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:8f10b1b67f0119a2dd5f838a3e98ab2c412e4b51fb1e4841e2b79fd4cae86105`  
		Last Modified: Tue, 29 Mar 2022 01:06:51 GMT  
		Size: 24.9 MB (24887495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103ccfc95d14718dd5bd47005c93225d5f82bdc075ccfc346e1b366afb616d57`  
		Last Modified: Tue, 29 Mar 2022 09:01:39 GMT  
		Size: 2.5 MB (2467692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13697b82f395905c310bf0030c74844e8f8fc5979a009c041a18de4488636164`  
		Last Modified: Tue, 29 Mar 2022 09:01:50 GMT  
		Size: 24.5 MB (24493260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2ac88da5d3c67e62e0687502448009b09b127f0c57bf294dddbcb4e3c67ebdaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48899046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0484404d76497f77102c5cad66c1b3d4fcd09bb1379a444779e070ca97beaf88`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:32:07 GMT
ADD file:ca7a6b7c138de7fd85996719398396d0ed0f059d2e12b7f401cd460b64924e25 in / 
# Thu, 17 Mar 2022 09:32:08 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 04:12:25 GMT
ENV MONO_VERSION=6.12.0.122
# Sat, 19 Mar 2022 04:13:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Sat, 19 Mar 2022 04:13:46 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0b8f06901fc5e8a29999e260b4ada4ee1cc4415e5c1a16fb7bb21cc2ac995f72`  
		Last Modified: Thu, 17 Mar 2022 09:48:01 GMT  
		Size: 22.8 MB (22754389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635212b9c70cb02c0aa647ee91ce1417572add8cdc66e2e2998bcb3a9ad605d8`  
		Last Modified: Sat, 19 Mar 2022 04:23:11 GMT  
		Size: 2.4 MB (2361883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2618a06f8bc8c9377958b480ea3d540f429435783b225a5bf6c0246baf3af`  
		Last Modified: Sat, 19 Mar 2022 04:23:27 GMT  
		Size: 23.8 MB (23782774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b59f4f7bc7c6bb2a267b5550c0522fd32c39acaea406fb0ce5e99fad0ad1c1af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57879410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e0d90c8e274883c6779dc03297086f922f40537cb0eab2c05fc55a7b74edf4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:46:20 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 02:46:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 02:46:53 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67cb289097e9051e621fb2d3504fa9edc303c8f8f5dc9d862aafebd2d8061ed`  
		Last Modified: Wed, 30 Mar 2022 02:51:08 GMT  
		Size: 2.6 MB (2641061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e73ba17b3be4b16e17a57383933f38521997a198f5fab534ec9453756fab69`  
		Last Modified: Wed, 30 Mar 2022 02:51:13 GMT  
		Size: 29.3 MB (29318572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:ad2b667b5f0896ddb64fd58494874f8a15bdbb194d559a860a1f2e6623cd3f58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99159811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a8eae2747d9e265311e2b7446014eecd943892a15c34dff942b2c39eee1bf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:26 GMT
ADD file:bcf3d504dc285de8b639c7f4017c41a4593a6c2aa6f046c9be79e587d05b5120 in / 
# Tue, 29 Mar 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 15:02:04 GMT
ENV MONO_VERSION=6.12.0.122
# Tue, 29 Mar 2022 15:02:13 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 29 Mar 2022 15:02:36 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:65b92490caa5e2c0588fab60d39315a2a8c09aa8ea0fe208d23f6984a47ecc03`  
		Last Modified: Tue, 29 Mar 2022 00:50:02 GMT  
		Size: 27.8 MB (27801252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebbeca4656bb310b6dac7751436576af2e3c06066b222f9a962062ff4114cc1`  
		Last Modified: Tue, 29 Mar 2022 15:06:05 GMT  
		Size: 2.8 MB (2789213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98d81278fc0743b83c503c809fdcffbaa11e083f06455ea6dfed18642791ba`  
		Last Modified: Tue, 29 Mar 2022 15:06:14 GMT  
		Size: 68.6 MB (68569346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:9b3a0defce0a5c2ae9bfc6d34af244911ccd407e7973e0f3eedce5fe3670f57e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60326275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184331441c848755861d28d51bfb13f10dc8e51ace7607db24b3326be9c1166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 06:30:50 GMT
ENV MONO_VERSION=6.12.0.122
# Wed, 30 Mar 2022 06:32:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 30 Mar 2022 06:33:27 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55feab57ab15634326c723014da448815650e9737d6c5671ca5a4cd4503905cb`  
		Last Modified: Wed, 30 Mar 2022 06:53:14 GMT  
		Size: 2.9 MB (2892687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00a3dcf742861f8ca53669004126ef6bead547f42b4f28c1d7ba21debbc8b5`  
		Last Modified: Wed, 30 Mar 2022 06:53:20 GMT  
		Size: 26.9 MB (26873425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
