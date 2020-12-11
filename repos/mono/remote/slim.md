## `mono:slim`

```console
$ docker pull mono@sha256:ec0d3b3a54671e6961b36fb878d90c9c8a8d0372f08a9cc4a54f274c7c25e0c9
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
$ docker pull mono@sha256:97fea20b1b77d25cc11fac7ad33c667d95c7bfa42d70a4cb747db480ce72db47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94453366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2452815b8c37bc96ea426ec2f1186a97e324ac5037e7f1a97a171adb6230dab4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:08:45 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 07:08:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 07:09:24 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e204cb0a8a1bcd014c8e9cd36d92f0d1a42125d7203b02283c9b039997aeac`  
		Last Modified: Wed, 18 Nov 2020 07:27:13 GMT  
		Size: 255.9 KB (255899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b378d0795c2a4b816636afdff794c4c0bb82d4d4e6a63d36d8de5be2f6872f1`  
		Last Modified: Wed, 18 Nov 2020 07:27:32 GMT  
		Size: 67.1 MB (67091983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:4f5d32d9ec766bfaf329547b4755bfe02eefb4d45046cbdfa491b9feed6d23fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51605469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6ab1e05a0017d8e4c4beaf5fabda95e3a4f4db3453015c92807fbd2af6d7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:37 GMT
ADD file:d75cebdc79385debd2d6d1c8c34855d2bd4779b13ee47f76e34c6d8fca037531 in / 
# Tue, 17 Nov 2020 20:20:45 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:48:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:49:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:49:53 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:1b8dd2ec17ab788b6ea03a9b6cf68afada9a8692681d29e9795db0abf6554404`  
		Last Modified: Tue, 17 Nov 2020 20:30:33 GMT  
		Size: 24.9 MB (24850311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05baa1a4580b5db26b6e95be46ea7c3c911e02763abc687ff0b7ff1ac8c3d69e`  
		Last Modified: Fri, 11 Dec 2020 00:53:53 GMT  
		Size: 255.9 KB (255949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcd83802c296fe8f139c457197e375b3de65bebb1f2b2a4f96b337a147d3010`  
		Last Modified: Fri, 11 Dec 2020 00:54:03 GMT  
		Size: 26.5 MB (26499209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:800fceb9a67e83837fae2e11f4b64ae33b8d3553062c74eb27a773036ea5be92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48699604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12763218e02f17c76b24f4a7331eddeb6198fbee718bc11b781c70c9ba124d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 14:56:54 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 14:57:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 14:58:11 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071e69fcfb9ee0aee198b34d2e65971bce210154ca78029673f7a4587dba98c`  
		Last Modified: Wed, 18 Nov 2020 15:07:42 GMT  
		Size: 256.0 KB (255978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c6379263fdd01744f7b8bcdcf328bb04a1efc5e78229d1770f08c3ab63adf9`  
		Last Modified: Wed, 18 Nov 2020 15:07:51 GMT  
		Size: 25.7 MB (25729440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:0e552be64b73e95995178f3530c280d8b01a775904f49958c49105ef6f7f8e61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57838654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3089f8d93db672126a2806d8d9cc50d2bcda4ba3dbaecca6bb9e7e8426eaa201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:40:21 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:40:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:41:18 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9211a1c3bffc7a39cf8c3174d7f7de9329295b6474bdd8d72ab9644fff94e`  
		Last Modified: Fri, 11 Dec 2020 00:44:08 GMT  
		Size: 255.9 KB (255921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc83dcb6b6716a71be07cbacf280c77737ea97150be83a369ab6b491deef0418`  
		Last Modified: Fri, 11 Dec 2020 00:44:18 GMT  
		Size: 31.7 MB (31720201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:922f4e6c316eab63210eb6f2f45686bfa934cd76a3b57e0a6ddc887bc4665dc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99127254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340aca337949030e11c7970bba606992f53421fdc526f4cebfc013e77c38303`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 00:38:44 GMT
ENV MONO_VERSION=6.12.0.107
# Fri, 11 Dec 2020 00:38:53 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Fri, 11 Dec 2020 00:39:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddafc845098e9a2a66850e53bdcfaa1173904510dc84bf2c6910925a4c3c045a`  
		Last Modified: Fri, 11 Dec 2020 00:41:47 GMT  
		Size: 255.8 KB (255802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dbe8684dd9be0f4cf763eb0f7f7c137403ef2666575c628e10ed25e8938eef`  
		Last Modified: Fri, 11 Dec 2020 00:42:06 GMT  
		Size: 71.1 MB (71105266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:56fd040b508e826ca2b4b9571814abb328162114225e6359bb91fe88d073102b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60138191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb3e30769d83f47adfb9790d84cf97bcfa99f68ec9d8f786d76e0c1156a4ad1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 02:30:57 GMT
ENV MONO_VERSION=6.10.0.104
# Wed, 18 Nov 2020 02:34:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Wed, 18 Nov 2020 02:38:07 GMT
RUN echo "deb http://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14255bc818ce18b4ab09d9ee61d303092bc8657a173fc74c8c64df944e601a5`  
		Last Modified: Wed, 18 Nov 2020 03:15:04 GMT  
		Size: 256.3 KB (256335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851074b86d7cc53505b83fe532498eba28284dcefcfa6e682fe54a43bbc6298`  
		Last Modified: Wed, 18 Nov 2020 03:15:10 GMT  
		Size: 29.4 MB (29350154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
