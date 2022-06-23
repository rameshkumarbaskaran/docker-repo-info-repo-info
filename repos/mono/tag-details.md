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
-	[`mono:6.12.0.182`](#mono6120182)
-	[`mono:6.12.0.182-slim`](#mono6120182-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:6`

```console
$ docker pull mono@sha256:6c5d93f65380b6439d832cce0210b220aa6f881a57f9409e896c2b540a78500f
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
$ docker pull mono@sha256:20cd1f6970624d00c69b114e95b07676ccc6759b4bfa96d87d2d316456851640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254417452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95165788dbeb36ffdb7a7d8071b13c8aa2338ba749946ac19e68ad93cd748feb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:57:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaae8abfcf8730ac3b34c9af2e194c634d79ab358331c72f2fe28b50fe5e4dc`  
		Last Modified: Thu, 23 Jun 2022 04:04:32 GMT  
		Size: 159.7 MB (159726737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v5

```console
$ docker pull mono@sha256:8aa046ef67f31390b606aa89317cf7f4ba20acd26033d954295baed80353e0a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa301c44b356146dc040190aed33fd0cca784625d0373c0d9ef9cbe574bdd304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:54:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07364fcd207cbc719207643ef95f8aeafc3a0f9e643868b571e5727f07e0c4f`  
		Last Modified: Thu, 23 Jun 2022 03:02:40 GMT  
		Size: 141.0 MB (141020175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm variant v7

```console
$ docker pull mono@sha256:55b20826ffcc17aafa45701264c09278d7a2973cf733b9ccec05665c2943c207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188781499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ffec2694682ff07163bbea623875ce9eaec1eea0ad55ad7e1f2005d03c10b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:34:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c98ca037e20a62b0cced06c13b8c6fc9e9ba64fbaf561f4fa8f5406a0bbb6`  
		Last Modified: Thu, 23 Jun 2022 06:41:45 GMT  
		Size: 139.9 MB (139877601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e0e44f68f1a2979ca2068876ae7da5a1f0c01714d6a956fe663f2f28f9ede37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab20306c5069132bb06b29329268f9ba198476d019e87d892aaf3ce2734e132f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:59:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bb1c55b3452215fbd3c902191776c8056a40d8b981530a4760c718eabd1fb2`  
		Last Modified: Thu, 23 Jun 2022 04:03:16 GMT  
		Size: 158.0 MB (158015895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; 386

```console
$ docker pull mono@sha256:6b9f0c5a13b0df94fe37120381befa7a7a838da47809cdd7e61750ccd374aef6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259078850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcfcd03261e069b509d727d927c7c3055a9bafde656ddab4d91cba67eddae6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:00:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3889a12c50905383ca7c05ea29c70a6570224a3d3c598eeea858b8a652213a6`  
		Last Modified: Thu, 23 Jun 2022 04:03:38 GMT  
		Size: 159.9 MB (159904036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6` - linux; ppc64le

```console
$ docker pull mono@sha256:a36a61a79a75faac96928984c885e16dc5341bae264940f42a5be34a44e737f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204233859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb0f938c8562bad3d2e08a792165c349021fcffaf26d84b85331d22b8cfd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:31:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9975e82a149a6eaee70df67907a8f1fd670cdd0ecffe8cd999f41b5074cb9`  
		Last Modified: Thu, 23 Jun 2022 08:39:38 GMT  
		Size: 143.9 MB (143883802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6-slim`

```console
$ docker pull mono@sha256:fcaa25d7d118eac8b9d66135146a0105206dd0ea7d3e23a60e9563e5247aacc7
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
$ docker pull mono@sha256:ce5fec9f6149a6202c0242fc3e649eb5232ebe605379f2d3ef37dbc7af903c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813dedd8591fe7c1f3f073914c9f7c04955ce813eca1d7f8428dc389a52d13af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8c29be2f9d245b365d8f8336ca067ecafe5f7d47d5e166f5c165b4b3e1a31c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09704630f58fa24aeb180e87b94d96c3b947485ce67334a9dda1a008dc2d3c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2cca758f375964ad1c50f290c0ea0cacba46ccfbc61c6ac9b8e54430965ae443
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a08449c8b4b191ee4205a1bc99c781243a6be08d86ebb04d06e38ccf7eb08e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b912a9a3fc92daa6749d801197f3ee1737e82089072cda6a8bbd88ef81c4089f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e9bdff1be7098a2aa07d47d1c9cf8b769e2667f48528b10f39c6a8144a47e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; 386

```console
$ docker pull mono@sha256:0285fbd408e63c399e5b4e4f7267681d71acb1109666aaa483c22950356a3aac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b6b7aeb9563163ff07c47584af59c6dfa008a13fbbe44752ae829ff5a2f27`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0fdda7fdadd09e05567be879251f26eca1b603c6017cf1f6cb128f29257cd27e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cdd98bc63a5f7ad37871b875331ad1005ce7b20ee0ef05652786fb64439bab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10`

```console
$ docker pull mono@sha256:4672244da2194c1b3ee2ea572934853aa6cd5d8d604b1fc2ec2a58aff1d18cde
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
$ docker pull mono@sha256:5f9c34940e48f078dc7f265d5b1def39db7868b7d855e18167080685850cdf98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225005574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb918e8ca2d45af3fff9408f7691e961f7b8ce9b8ec79e6a789493a75d2fef8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:46 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:55:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:02:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34cfd6ea6b484e460bddab320e5151debe1700c47960dae29d8ed14c5a69d89`  
		Last Modified: Thu, 23 Jun 2022 04:03:46 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd7a2db6f7d18f364dd03630ccf125bc07bc1a0a82f4a485fd6c11df4cb40ce`  
		Last Modified: Thu, 23 Jun 2022 04:03:55 GMT  
		Size: 64.8 MB (64778855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707596ea98fcf877e52f592145dec2e28f1035b35b740f9ae25663ba551dbb`  
		Last Modified: Thu, 23 Jun 2022 04:05:08 GMT  
		Size: 130.3 MB (130309114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v5

```console
$ docker pull mono@sha256:4a8d120d4bb8673ddb683433b1b49ae9f3a1755a589b84afa4881fb01cfc3b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180859834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c00e325614a080a36047e87e8a2e20f399f2f3a24bea2b37960229f1660b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:49:56 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 02:50:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:51:10 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:58:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77ca9f16c48c9e023ec7af4682c4083dd595048ce82664d8b4077125bcca64`  
		Last Modified: Thu, 23 Jun 2022 03:00:31 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba1007acb7141a129a311a9c9d88e5453735acedfe046bd055c861fe48cb266`  
		Last Modified: Thu, 23 Jun 2022 03:00:49 GMT  
		Size: 24.5 MB (24521803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ebc017a6079e22d4065532d8a2638ad6628da7eabda853a593713e3b056f03`  
		Last Modified: Thu, 23 Jun 2022 03:04:30 GMT  
		Size: 129.0 MB (128980280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm variant v7

```console
$ docker pull mono@sha256:de1e0a75aac4b76c634fb25a80c1662aba3db8031ada3d6f1993502eeaeb7d18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1396a8273a78da562526a30c5e1f72ad84e68c12b1e9d548c39179e1978c92c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:29:41 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 06:30:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:30:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:37:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f3229cd778d1d470ccd83725c2a442fbbf7f75a7e9ca6208de8ec529bf305`  
		Last Modified: Thu, 23 Jun 2022 06:39:38 GMT  
		Size: 2.4 MB (2367008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab125b86b0f835325258503d1b9918f6717f4b21705b57c2e4bdd4f943a72f6`  
		Last Modified: Thu, 23 Jun 2022 06:39:54 GMT  
		Size: 23.8 MB (23815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136b51ecc570d24e6f490fe9157b298728d24250e9f448d272ee4589e86bf476`  
		Last Modified: Thu, 23 Jun 2022 06:43:40 GMT  
		Size: 127.8 MB (127830609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4081635ca31f05abd93ff5ad7c6fdd45a1211039deb1162822e0ff0652da0e3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203365680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2459c686ed8d18a2f6ec17932a094e862b09e0fe8fd525fd2b23d3d0fd19674e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:03 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:58:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:32 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:01:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90be799bf47d9343604d35e3f85224654cd34db33334e61c28ead6e123090c21`  
		Last Modified: Thu, 23 Jun 2022 04:02:31 GMT  
		Size: 2.6 MB (2641228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afb08679575abb6885470feb2d29eb7b21b7dcb9fe4a708ac465c97b97915`  
		Last Modified: Thu, 23 Jun 2022 04:02:36 GMT  
		Size: 29.4 MB (29361523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10087051c7996ac8c61733ca1684069ee9dfb63f0bd827d1d062278381d09d97`  
		Last Modified: Thu, 23 Jun 2022 04:04:00 GMT  
		Size: 145.4 MB (145448900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; 386

```console
$ docker pull mono@sha256:a171128a240685820a71335e50b6d42648300ee5cee1762e31133a2713f52dcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c7332ecfd6ff2d4500eabcc21604fd4e350b66142a5efb8d0c8d710ef0a629`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:55 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:59:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:59:28 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:01:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee8c4df98cdb3846f6bb3e17aa1795f6cc8ae006d496ff6713fe9b240bd8cb`  
		Last Modified: Thu, 23 Jun 2022 04:02:51 GMT  
		Size: 2.8 MB (2789319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1dccead101746fc30208f1ffb0f2f4b1c5c5639a422e88abf2314b970f1cb`  
		Last Modified: Thu, 23 Jun 2022 04:03:01 GMT  
		Size: 68.6 MB (68594057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5d1fcb44eb816bf471732fdd0717febec579b500d715452d60c6a6819073c2`  
		Last Modified: Thu, 23 Jun 2022 04:04:24 GMT  
		Size: 131.4 MB (131416576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10` - linux; ppc64le

```console
$ docker pull mono@sha256:005fff0638867a11468a10b36362d9f478f16aec8595aa7e411bc3eb69265110
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192388958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fecb3b6f1246dbab7e1d7261f1c6283a1a42de4f9c793fbea587ec5d6387893`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:24:32 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 08:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:26:43 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:37:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd417d2b0395d4f6919b6bd236f90c062190e85ef8acc12781261c1f8cdc1a63`  
		Last Modified: Thu, 23 Jun 2022 08:38:52 GMT  
		Size: 2.9 MB (2892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8101c0ae8c273bb5172353652bfdabc1a6b45f2313baa54126c0ad45aee1c0`  
		Last Modified: Thu, 23 Jun 2022 08:38:57 GMT  
		Size: 26.9 MB (26917613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c73a90bb10aa07003584de73f1f7401d1b3e578c2baad6e8781dd1390b8680`  
		Last Modified: Thu, 23 Jun 2022 08:40:25 GMT  
		Size: 132.0 MB (132018285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10-slim`

```console
$ docker pull mono@sha256:f1873aca3997e76eadd84a0fc551727c116e97c749edce8174fccf643a6779f5
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
$ docker pull mono@sha256:df99b76bdedf0983fb8fe2c59886a788af0bf46eb52c7451e3e00a498a830e1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94696460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a9ce5fd13d169d1d2b8ae5a74d834e0d76f6157fff2ad7a2cc8821dab641`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:46 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:55:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34cfd6ea6b484e460bddab320e5151debe1700c47960dae29d8ed14c5a69d89`  
		Last Modified: Thu, 23 Jun 2022 04:03:46 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd7a2db6f7d18f364dd03630ccf125bc07bc1a0a82f4a485fd6c11df4cb40ce`  
		Last Modified: Thu, 23 Jun 2022 04:03:55 GMT  
		Size: 64.8 MB (64778855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:5dcb98e1b5aaeadcbe9203e93f066e526cff74133b1c01088df180bb84cae885
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7641cf2b2a2b3098c472653b50abf0158e4437d69766726ddebf38de86a05b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:49:56 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 02:50:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:51:10 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77ca9f16c48c9e023ec7af4682c4083dd595048ce82664d8b4077125bcca64`  
		Last Modified: Thu, 23 Jun 2022 03:00:31 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba1007acb7141a129a311a9c9d88e5453735acedfe046bd055c861fe48cb266`  
		Last Modified: Thu, 23 Jun 2022 03:00:49 GMT  
		Size: 24.5 MB (24521803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:6e4353d32d6bc45e008a99f48835abd1b2be0a002d7c6b653fa50adaf9dd5e02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48930032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e68ccf948623d5ffffa9c72494922bb536e4d055baed865175e1f8a733f41a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:29:41 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 06:30:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:30:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f3229cd778d1d470ccd83725c2a442fbbf7f75a7e9ca6208de8ec529bf305`  
		Last Modified: Thu, 23 Jun 2022 06:39:38 GMT  
		Size: 2.4 MB (2367008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab125b86b0f835325258503d1b9918f6717f4b21705b57c2e4bdd4f943a72f6`  
		Last Modified: Thu, 23 Jun 2022 06:39:54 GMT  
		Size: 23.8 MB (23815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:874fdd4d5cb3337332f15bb3500648a0afa24efaf3a8775410be355980c7b0bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdd4971cd661dc88ecddba4aea784f087e06b01e8231b1b112a5158806ff417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:03 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:58:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:32 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90be799bf47d9343604d35e3f85224654cd34db33334e61c28ead6e123090c21`  
		Last Modified: Thu, 23 Jun 2022 04:02:31 GMT  
		Size: 2.6 MB (2641228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afb08679575abb6885470feb2d29eb7b21b7dcb9fe4a708ac465c97b97915`  
		Last Modified: Thu, 23 Jun 2022 04:02:36 GMT  
		Size: 29.4 MB (29361523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; 386

```console
$ docker pull mono@sha256:ffaa55af82d552b6477fa510ec8d8146083aa155626573400045e1b6abc31984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99182918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea335742ee430af16e008be6aad0a4afafcb14586682824132140a596cd5c40d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:55 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:59:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:59:28 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee8c4df98cdb3846f6bb3e17aa1795f6cc8ae006d496ff6713fe9b240bd8cb`  
		Last Modified: Thu, 23 Jun 2022 04:02:51 GMT  
		Size: 2.8 MB (2789319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1dccead101746fc30208f1ffb0f2f4b1c5c5639a422e88abf2314b970f1cb`  
		Last Modified: Thu, 23 Jun 2022 04:03:01 GMT  
		Size: 68.6 MB (68594057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:3d0a4a7faaedd2b533b744868b85134b78be9c6836da0e838c94bdc94b8242cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8f2d73522136d19b28f5980c2661de05cd855f4153e4d4220bca0a8195412f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:24:32 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 08:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:26:43 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd417d2b0395d4f6919b6bd236f90c062190e85ef8acc12781261c1f8cdc1a63`  
		Last Modified: Thu, 23 Jun 2022 08:38:52 GMT  
		Size: 2.9 MB (2892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8101c0ae8c273bb5172353652bfdabc1a6b45f2313baa54126c0ad45aee1c0`  
		Last Modified: Thu, 23 Jun 2022 08:38:57 GMT  
		Size: 26.9 MB (26917613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0`

```console
$ docker pull mono@sha256:4672244da2194c1b3ee2ea572934853aa6cd5d8d604b1fc2ec2a58aff1d18cde
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
$ docker pull mono@sha256:5f9c34940e48f078dc7f265d5b1def39db7868b7d855e18167080685850cdf98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225005574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb918e8ca2d45af3fff9408f7691e961f7b8ce9b8ec79e6a789493a75d2fef8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:46 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:55:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:02:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34cfd6ea6b484e460bddab320e5151debe1700c47960dae29d8ed14c5a69d89`  
		Last Modified: Thu, 23 Jun 2022 04:03:46 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd7a2db6f7d18f364dd03630ccf125bc07bc1a0a82f4a485fd6c11df4cb40ce`  
		Last Modified: Thu, 23 Jun 2022 04:03:55 GMT  
		Size: 64.8 MB (64778855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707596ea98fcf877e52f592145dec2e28f1035b35b740f9ae25663ba551dbb`  
		Last Modified: Thu, 23 Jun 2022 04:05:08 GMT  
		Size: 130.3 MB (130309114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:4a8d120d4bb8673ddb683433b1b49ae9f3a1755a589b84afa4881fb01cfc3b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180859834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c00e325614a080a36047e87e8a2e20f399f2f3a24bea2b37960229f1660b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:49:56 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 02:50:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:51:10 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:58:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77ca9f16c48c9e023ec7af4682c4083dd595048ce82664d8b4077125bcca64`  
		Last Modified: Thu, 23 Jun 2022 03:00:31 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba1007acb7141a129a311a9c9d88e5453735acedfe046bd055c861fe48cb266`  
		Last Modified: Thu, 23 Jun 2022 03:00:49 GMT  
		Size: 24.5 MB (24521803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ebc017a6079e22d4065532d8a2638ad6628da7eabda853a593713e3b056f03`  
		Last Modified: Thu, 23 Jun 2022 03:04:30 GMT  
		Size: 129.0 MB (128980280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:de1e0a75aac4b76c634fb25a80c1662aba3db8031ada3d6f1993502eeaeb7d18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1396a8273a78da562526a30c5e1f72ad84e68c12b1e9d548c39179e1978c92c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:29:41 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 06:30:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:30:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:37:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f3229cd778d1d470ccd83725c2a442fbbf7f75a7e9ca6208de8ec529bf305`  
		Last Modified: Thu, 23 Jun 2022 06:39:38 GMT  
		Size: 2.4 MB (2367008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab125b86b0f835325258503d1b9918f6717f4b21705b57c2e4bdd4f943a72f6`  
		Last Modified: Thu, 23 Jun 2022 06:39:54 GMT  
		Size: 23.8 MB (23815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136b51ecc570d24e6f490fe9157b298728d24250e9f448d272ee4589e86bf476`  
		Last Modified: Thu, 23 Jun 2022 06:43:40 GMT  
		Size: 127.8 MB (127830609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4081635ca31f05abd93ff5ad7c6fdd45a1211039deb1162822e0ff0652da0e3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203365680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2459c686ed8d18a2f6ec17932a094e862b09e0fe8fd525fd2b23d3d0fd19674e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:03 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:58:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:32 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:01:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90be799bf47d9343604d35e3f85224654cd34db33334e61c28ead6e123090c21`  
		Last Modified: Thu, 23 Jun 2022 04:02:31 GMT  
		Size: 2.6 MB (2641228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afb08679575abb6885470feb2d29eb7b21b7dcb9fe4a708ac465c97b97915`  
		Last Modified: Thu, 23 Jun 2022 04:02:36 GMT  
		Size: 29.4 MB (29361523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10087051c7996ac8c61733ca1684069ee9dfb63f0bd827d1d062278381d09d97`  
		Last Modified: Thu, 23 Jun 2022 04:04:00 GMT  
		Size: 145.4 MB (145448900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; 386

```console
$ docker pull mono@sha256:a171128a240685820a71335e50b6d42648300ee5cee1762e31133a2713f52dcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c7332ecfd6ff2d4500eabcc21604fd4e350b66142a5efb8d0c8d710ef0a629`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:55 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:59:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:59:28 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:01:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee8c4df98cdb3846f6bb3e17aa1795f6cc8ae006d496ff6713fe9b240bd8cb`  
		Last Modified: Thu, 23 Jun 2022 04:02:51 GMT  
		Size: 2.8 MB (2789319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1dccead101746fc30208f1ffb0f2f4b1c5c5639a422e88abf2314b970f1cb`  
		Last Modified: Thu, 23 Jun 2022 04:03:01 GMT  
		Size: 68.6 MB (68594057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5d1fcb44eb816bf471732fdd0717febec579b500d715452d60c6a6819073c2`  
		Last Modified: Thu, 23 Jun 2022 04:04:24 GMT  
		Size: 131.4 MB (131416576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0` - linux; ppc64le

```console
$ docker pull mono@sha256:005fff0638867a11468a10b36362d9f478f16aec8595aa7e411bc3eb69265110
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192388958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fecb3b6f1246dbab7e1d7261f1c6283a1a42de4f9c793fbea587ec5d6387893`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:24:32 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 08:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:26:43 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:37:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd417d2b0395d4f6919b6bd236f90c062190e85ef8acc12781261c1f8cdc1a63`  
		Last Modified: Thu, 23 Jun 2022 08:38:52 GMT  
		Size: 2.9 MB (2892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8101c0ae8c273bb5172353652bfdabc1a6b45f2313baa54126c0ad45aee1c0`  
		Last Modified: Thu, 23 Jun 2022 08:38:57 GMT  
		Size: 26.9 MB (26917613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c73a90bb10aa07003584de73f1f7401d1b3e578c2baad6e8781dd1390b8680`  
		Last Modified: Thu, 23 Jun 2022 08:40:25 GMT  
		Size: 132.0 MB (132018285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0-slim`

```console
$ docker pull mono@sha256:f1873aca3997e76eadd84a0fc551727c116e97c749edce8174fccf643a6779f5
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
$ docker pull mono@sha256:df99b76bdedf0983fb8fe2c59886a788af0bf46eb52c7451e3e00a498a830e1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94696460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a9ce5fd13d169d1d2b8ae5a74d834e0d76f6157fff2ad7a2cc8821dab641`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:46 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:55:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34cfd6ea6b484e460bddab320e5151debe1700c47960dae29d8ed14c5a69d89`  
		Last Modified: Thu, 23 Jun 2022 04:03:46 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd7a2db6f7d18f364dd03630ccf125bc07bc1a0a82f4a485fd6c11df4cb40ce`  
		Last Modified: Thu, 23 Jun 2022 04:03:55 GMT  
		Size: 64.8 MB (64778855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:5dcb98e1b5aaeadcbe9203e93f066e526cff74133b1c01088df180bb84cae885
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7641cf2b2a2b3098c472653b50abf0158e4437d69766726ddebf38de86a05b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:49:56 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 02:50:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:51:10 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77ca9f16c48c9e023ec7af4682c4083dd595048ce82664d8b4077125bcca64`  
		Last Modified: Thu, 23 Jun 2022 03:00:31 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba1007acb7141a129a311a9c9d88e5453735acedfe046bd055c861fe48cb266`  
		Last Modified: Thu, 23 Jun 2022 03:00:49 GMT  
		Size: 24.5 MB (24521803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:6e4353d32d6bc45e008a99f48835abd1b2be0a002d7c6b653fa50adaf9dd5e02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48930032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e68ccf948623d5ffffa9c72494922bb536e4d055baed865175e1f8a733f41a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:29:41 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 06:30:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:30:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f3229cd778d1d470ccd83725c2a442fbbf7f75a7e9ca6208de8ec529bf305`  
		Last Modified: Thu, 23 Jun 2022 06:39:38 GMT  
		Size: 2.4 MB (2367008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab125b86b0f835325258503d1b9918f6717f4b21705b57c2e4bdd4f943a72f6`  
		Last Modified: Thu, 23 Jun 2022 06:39:54 GMT  
		Size: 23.8 MB (23815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:874fdd4d5cb3337332f15bb3500648a0afa24efaf3a8775410be355980c7b0bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdd4971cd661dc88ecddba4aea784f087e06b01e8231b1b112a5158806ff417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:03 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:58:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:32 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90be799bf47d9343604d35e3f85224654cd34db33334e61c28ead6e123090c21`  
		Last Modified: Thu, 23 Jun 2022 04:02:31 GMT  
		Size: 2.6 MB (2641228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afb08679575abb6885470feb2d29eb7b21b7dcb9fe4a708ac465c97b97915`  
		Last Modified: Thu, 23 Jun 2022 04:02:36 GMT  
		Size: 29.4 MB (29361523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; 386

```console
$ docker pull mono@sha256:ffaa55af82d552b6477fa510ec8d8146083aa155626573400045e1b6abc31984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99182918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea335742ee430af16e008be6aad0a4afafcb14586682824132140a596cd5c40d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:55 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:59:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:59:28 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee8c4df98cdb3846f6bb3e17aa1795f6cc8ae006d496ff6713fe9b240bd8cb`  
		Last Modified: Thu, 23 Jun 2022 04:02:51 GMT  
		Size: 2.8 MB (2789319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1dccead101746fc30208f1ffb0f2f4b1c5c5639a422e88abf2314b970f1cb`  
		Last Modified: Thu, 23 Jun 2022 04:03:01 GMT  
		Size: 68.6 MB (68594057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:3d0a4a7faaedd2b533b744868b85134b78be9c6836da0e838c94bdc94b8242cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8f2d73522136d19b28f5980c2661de05cd855f4153e4d4220bca0a8195412f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:24:32 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 08:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:26:43 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd417d2b0395d4f6919b6bd236f90c062190e85ef8acc12781261c1f8cdc1a63`  
		Last Modified: Thu, 23 Jun 2022 08:38:52 GMT  
		Size: 2.9 MB (2892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8101c0ae8c273bb5172353652bfdabc1a6b45f2313baa54126c0ad45aee1c0`  
		Last Modified: Thu, 23 Jun 2022 08:38:57 GMT  
		Size: 26.9 MB (26917613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104`

```console
$ docker pull mono@sha256:4672244da2194c1b3ee2ea572934853aa6cd5d8d604b1fc2ec2a58aff1d18cde
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
$ docker pull mono@sha256:5f9c34940e48f078dc7f265d5b1def39db7868b7d855e18167080685850cdf98
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225005574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb918e8ca2d45af3fff9408f7691e961f7b8ce9b8ec79e6a789493a75d2fef8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:46 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:55:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:02:49 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34cfd6ea6b484e460bddab320e5151debe1700c47960dae29d8ed14c5a69d89`  
		Last Modified: Thu, 23 Jun 2022 04:03:46 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd7a2db6f7d18f364dd03630ccf125bc07bc1a0a82f4a485fd6c11df4cb40ce`  
		Last Modified: Thu, 23 Jun 2022 04:03:55 GMT  
		Size: 64.8 MB (64778855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18707596ea98fcf877e52f592145dec2e28f1035b35b740f9ae25663ba551dbb`  
		Last Modified: Thu, 23 Jun 2022 04:05:08 GMT  
		Size: 130.3 MB (130309114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v5

```console
$ docker pull mono@sha256:4a8d120d4bb8673ddb683433b1b49ae9f3a1755a589b84afa4881fb01cfc3b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180859834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12c00e325614a080a36047e87e8a2e20f399f2f3a24bea2b37960229f1660b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:49:56 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 02:50:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:51:10 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:58:22 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77ca9f16c48c9e023ec7af4682c4083dd595048ce82664d8b4077125bcca64`  
		Last Modified: Thu, 23 Jun 2022 03:00:31 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba1007acb7141a129a311a9c9d88e5453735acedfe046bd055c861fe48cb266`  
		Last Modified: Thu, 23 Jun 2022 03:00:49 GMT  
		Size: 24.5 MB (24521803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ebc017a6079e22d4065532d8a2638ad6628da7eabda853a593713e3b056f03`  
		Last Modified: Thu, 23 Jun 2022 03:04:30 GMT  
		Size: 129.0 MB (128980280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm variant v7

```console
$ docker pull mono@sha256:de1e0a75aac4b76c634fb25a80c1662aba3db8031ada3d6f1993502eeaeb7d18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176760641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1396a8273a78da562526a30c5e1f72ad84e68c12b1e9d548c39179e1978c92c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:29:41 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 06:30:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:30:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:37:27 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f3229cd778d1d470ccd83725c2a442fbbf7f75a7e9ca6208de8ec529bf305`  
		Last Modified: Thu, 23 Jun 2022 06:39:38 GMT  
		Size: 2.4 MB (2367008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab125b86b0f835325258503d1b9918f6717f4b21705b57c2e4bdd4f943a72f6`  
		Last Modified: Thu, 23 Jun 2022 06:39:54 GMT  
		Size: 23.8 MB (23815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136b51ecc570d24e6f490fe9157b298728d24250e9f448d272ee4589e86bf476`  
		Last Modified: Thu, 23 Jun 2022 06:43:40 GMT  
		Size: 127.8 MB (127830609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4081635ca31f05abd93ff5ad7c6fdd45a1211039deb1162822e0ff0652da0e3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203365680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2459c686ed8d18a2f6ec17932a094e862b09e0fe8fd525fd2b23d3d0fd19674e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:03 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:58:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:32 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:01:19 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90be799bf47d9343604d35e3f85224654cd34db33334e61c28ead6e123090c21`  
		Last Modified: Thu, 23 Jun 2022 04:02:31 GMT  
		Size: 2.6 MB (2641228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afb08679575abb6885470feb2d29eb7b21b7dcb9fe4a708ac465c97b97915`  
		Last Modified: Thu, 23 Jun 2022 04:02:36 GMT  
		Size: 29.4 MB (29361523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10087051c7996ac8c61733ca1684069ee9dfb63f0bd827d1d062278381d09d97`  
		Last Modified: Thu, 23 Jun 2022 04:04:00 GMT  
		Size: 145.4 MB (145448900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; 386

```console
$ docker pull mono@sha256:a171128a240685820a71335e50b6d42648300ee5cee1762e31133a2713f52dcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230599494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c7332ecfd6ff2d4500eabcc21604fd4e350b66142a5efb8d0c8d710ef0a629`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:55 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:59:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:59:28 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:01:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee8c4df98cdb3846f6bb3e17aa1795f6cc8ae006d496ff6713fe9b240bd8cb`  
		Last Modified: Thu, 23 Jun 2022 04:02:51 GMT  
		Size: 2.8 MB (2789319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1dccead101746fc30208f1ffb0f2f4b1c5c5639a422e88abf2314b970f1cb`  
		Last Modified: Thu, 23 Jun 2022 04:03:01 GMT  
		Size: 68.6 MB (68594057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5d1fcb44eb816bf471732fdd0717febec579b500d715452d60c6a6819073c2`  
		Last Modified: Thu, 23 Jun 2022 04:04:24 GMT  
		Size: 131.4 MB (131416576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104` - linux; ppc64le

```console
$ docker pull mono@sha256:005fff0638867a11468a10b36362d9f478f16aec8595aa7e411bc3eb69265110
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192388958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fecb3b6f1246dbab7e1d7261f1c6283a1a42de4f9c793fbea587ec5d6387893`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:24:32 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 08:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:26:43 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:37:33 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd417d2b0395d4f6919b6bd236f90c062190e85ef8acc12781261c1f8cdc1a63`  
		Last Modified: Thu, 23 Jun 2022 08:38:52 GMT  
		Size: 2.9 MB (2892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8101c0ae8c273bb5172353652bfdabc1a6b45f2313baa54126c0ad45aee1c0`  
		Last Modified: Thu, 23 Jun 2022 08:38:57 GMT  
		Size: 26.9 MB (26917613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c73a90bb10aa07003584de73f1f7401d1b3e578c2baad6e8781dd1390b8680`  
		Last Modified: Thu, 23 Jun 2022 08:40:25 GMT  
		Size: 132.0 MB (132018285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.10.0.104-slim`

```console
$ docker pull mono@sha256:f1873aca3997e76eadd84a0fc551727c116e97c749edce8174fccf643a6779f5
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
$ docker pull mono@sha256:df99b76bdedf0983fb8fe2c59886a788af0bf46eb52c7451e3e00a498a830e1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94696460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7a9ce5fd13d169d1d2b8ae5a74d834e0d76f6157fff2ad7a2cc8821dab641`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:46 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:55:55 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:56:21 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34cfd6ea6b484e460bddab320e5151debe1700c47960dae29d8ed14c5a69d89`  
		Last Modified: Thu, 23 Jun 2022 04:03:46 GMT  
		Size: 2.8 MB (2777562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd7a2db6f7d18f364dd03630ccf125bc07bc1a0a82f4a485fd6c11df4cb40ce`  
		Last Modified: Thu, 23 Jun 2022 04:03:55 GMT  
		Size: 64.8 MB (64778855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:5dcb98e1b5aaeadcbe9203e93f066e526cff74133b1c01088df180bb84cae885
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7641cf2b2a2b3098c472653b50abf0158e4437d69766726ddebf38de86a05b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:49:56 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 02:50:23 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:51:10 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f77ca9f16c48c9e023ec7af4682c4083dd595048ce82664d8b4077125bcca64`  
		Last Modified: Thu, 23 Jun 2022 03:00:31 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba1007acb7141a129a311a9c9d88e5453735acedfe046bd055c861fe48cb266`  
		Last Modified: Thu, 23 Jun 2022 03:00:49 GMT  
		Size: 24.5 MB (24521803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:6e4353d32d6bc45e008a99f48835abd1b2be0a002d7c6b653fa50adaf9dd5e02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48930032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e68ccf948623d5ffffa9c72494922bb536e4d055baed865175e1f8a733f41a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:29:41 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 06:30:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:30:51 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f3229cd778d1d470ccd83725c2a442fbbf7f75a7e9ca6208de8ec529bf305`  
		Last Modified: Thu, 23 Jun 2022 06:39:38 GMT  
		Size: 2.4 MB (2367008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab125b86b0f835325258503d1b9918f6717f4b21705b57c2e4bdd4f943a72f6`  
		Last Modified: Thu, 23 Jun 2022 06:39:54 GMT  
		Size: 23.8 MB (23815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:874fdd4d5cb3337332f15bb3500648a0afa24efaf3a8775410be355980c7b0bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57916780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdd4971cd661dc88ecddba4aea784f087e06b01e8231b1b112a5158806ff417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:03 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:58:12 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:32 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90be799bf47d9343604d35e3f85224654cd34db33334e61c28ead6e123090c21`  
		Last Modified: Thu, 23 Jun 2022 04:02:31 GMT  
		Size: 2.6 MB (2641228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83afb08679575abb6885470feb2d29eb7b21b7dcb9fe4a708ac465c97b97915`  
		Last Modified: Thu, 23 Jun 2022 04:02:36 GMT  
		Size: 29.4 MB (29361523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; 386

```console
$ docker pull mono@sha256:ffaa55af82d552b6477fa510ec8d8146083aa155626573400045e1b6abc31984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99182918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea335742ee430af16e008be6aad0a4afafcb14586682824132140a596cd5c40d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:55 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 03:59:04 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:59:28 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee8c4df98cdb3846f6bb3e17aa1795f6cc8ae006d496ff6713fe9b240bd8cb`  
		Last Modified: Thu, 23 Jun 2022 04:02:51 GMT  
		Size: 2.8 MB (2789319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be1dccead101746fc30208f1ffb0f2f4b1c5c5639a422e88abf2314b970f1cb`  
		Last Modified: Thu, 23 Jun 2022 04:03:01 GMT  
		Size: 68.6 MB (68594057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.10.0.104-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:3d0a4a7faaedd2b533b744868b85134b78be9c6836da0e838c94bdc94b8242cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8f2d73522136d19b28f5980c2661de05cd855f4153e4d4220bca0a8195412f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:24:32 GMT
ENV MONO_VERSION=6.10.0.104
# Thu, 23 Jun 2022 08:25:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:26:43 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd417d2b0395d4f6919b6bd236f90c062190e85ef8acc12781261c1f8cdc1a63`  
		Last Modified: Thu, 23 Jun 2022 08:38:52 GMT  
		Size: 2.9 MB (2892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8101c0ae8c273bb5172353652bfdabc1a6b45f2313baa54126c0ad45aee1c0`  
		Last Modified: Thu, 23 Jun 2022 08:38:57 GMT  
		Size: 26.9 MB (26917613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12`

```console
$ docker pull mono@sha256:6c5d93f65380b6439d832cce0210b220aa6f881a57f9409e896c2b540a78500f
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
$ docker pull mono@sha256:20cd1f6970624d00c69b114e95b07676ccc6759b4bfa96d87d2d316456851640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254417452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95165788dbeb36ffdb7a7d8071b13c8aa2338ba749946ac19e68ad93cd748feb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:57:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaae8abfcf8730ac3b34c9af2e194c634d79ab358331c72f2fe28b50fe5e4dc`  
		Last Modified: Thu, 23 Jun 2022 04:04:32 GMT  
		Size: 159.7 MB (159726737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v5

```console
$ docker pull mono@sha256:8aa046ef67f31390b606aa89317cf7f4ba20acd26033d954295baed80353e0a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa301c44b356146dc040190aed33fd0cca784625d0373c0d9ef9cbe574bdd304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:54:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07364fcd207cbc719207643ef95f8aeafc3a0f9e643868b571e5727f07e0c4f`  
		Last Modified: Thu, 23 Jun 2022 03:02:40 GMT  
		Size: 141.0 MB (141020175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm variant v7

```console
$ docker pull mono@sha256:55b20826ffcc17aafa45701264c09278d7a2973cf733b9ccec05665c2943c207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188781499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ffec2694682ff07163bbea623875ce9eaec1eea0ad55ad7e1f2005d03c10b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:34:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c98ca037e20a62b0cced06c13b8c6fc9e9ba64fbaf561f4fa8f5406a0bbb6`  
		Last Modified: Thu, 23 Jun 2022 06:41:45 GMT  
		Size: 139.9 MB (139877601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e0e44f68f1a2979ca2068876ae7da5a1f0c01714d6a956fe663f2f28f9ede37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab20306c5069132bb06b29329268f9ba198476d019e87d892aaf3ce2734e132f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:59:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bb1c55b3452215fbd3c902191776c8056a40d8b981530a4760c718eabd1fb2`  
		Last Modified: Thu, 23 Jun 2022 04:03:16 GMT  
		Size: 158.0 MB (158015895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; 386

```console
$ docker pull mono@sha256:6b9f0c5a13b0df94fe37120381befa7a7a838da47809cdd7e61750ccd374aef6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259078850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcfcd03261e069b509d727d927c7c3055a9bafde656ddab4d91cba67eddae6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:00:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3889a12c50905383ca7c05ea29c70a6570224a3d3c598eeea858b8a652213a6`  
		Last Modified: Thu, 23 Jun 2022 04:03:38 GMT  
		Size: 159.9 MB (159904036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12` - linux; ppc64le

```console
$ docker pull mono@sha256:a36a61a79a75faac96928984c885e16dc5341bae264940f42a5be34a44e737f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204233859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb0f938c8562bad3d2e08a792165c349021fcffaf26d84b85331d22b8cfd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:31:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9975e82a149a6eaee70df67907a8f1fd670cdd0ecffe8cd999f41b5074cb9`  
		Last Modified: Thu, 23 Jun 2022 08:39:38 GMT  
		Size: 143.9 MB (143883802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12-slim`

```console
$ docker pull mono@sha256:fcaa25d7d118eac8b9d66135146a0105206dd0ea7d3e23a60e9563e5247aacc7
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
$ docker pull mono@sha256:ce5fec9f6149a6202c0242fc3e649eb5232ebe605379f2d3ef37dbc7af903c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813dedd8591fe7c1f3f073914c9f7c04955ce813eca1d7f8428dc389a52d13af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8c29be2f9d245b365d8f8336ca067ecafe5f7d47d5e166f5c165b4b3e1a31c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09704630f58fa24aeb180e87b94d96c3b947485ce67334a9dda1a008dc2d3c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2cca758f375964ad1c50f290c0ea0cacba46ccfbc61c6ac9b8e54430965ae443
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a08449c8b4b191ee4205a1bc99c781243a6be08d86ebb04d06e38ccf7eb08e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b912a9a3fc92daa6749d801197f3ee1737e82089072cda6a8bbd88ef81c4089f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e9bdff1be7098a2aa07d47d1c9cf8b769e2667f48528b10f39c6a8144a47e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; 386

```console
$ docker pull mono@sha256:0285fbd408e63c399e5b4e4f7267681d71acb1109666aaa483c22950356a3aac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b6b7aeb9563163ff07c47584af59c6dfa008a13fbbe44752ae829ff5a2f27`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0fdda7fdadd09e05567be879251f26eca1b603c6017cf1f6cb128f29257cd27e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cdd98bc63a5f7ad37871b875331ad1005ce7b20ee0ef05652786fb64439bab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0`

```console
$ docker pull mono@sha256:6c5d93f65380b6439d832cce0210b220aa6f881a57f9409e896c2b540a78500f
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
$ docker pull mono@sha256:20cd1f6970624d00c69b114e95b07676ccc6759b4bfa96d87d2d316456851640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254417452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95165788dbeb36ffdb7a7d8071b13c8aa2338ba749946ac19e68ad93cd748feb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:57:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaae8abfcf8730ac3b34c9af2e194c634d79ab358331c72f2fe28b50fe5e4dc`  
		Last Modified: Thu, 23 Jun 2022 04:04:32 GMT  
		Size: 159.7 MB (159726737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v5

```console
$ docker pull mono@sha256:8aa046ef67f31390b606aa89317cf7f4ba20acd26033d954295baed80353e0a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa301c44b356146dc040190aed33fd0cca784625d0373c0d9ef9cbe574bdd304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:54:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07364fcd207cbc719207643ef95f8aeafc3a0f9e643868b571e5727f07e0c4f`  
		Last Modified: Thu, 23 Jun 2022 03:02:40 GMT  
		Size: 141.0 MB (141020175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:55b20826ffcc17aafa45701264c09278d7a2973cf733b9ccec05665c2943c207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188781499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ffec2694682ff07163bbea623875ce9eaec1eea0ad55ad7e1f2005d03c10b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:34:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c98ca037e20a62b0cced06c13b8c6fc9e9ba64fbaf561f4fa8f5406a0bbb6`  
		Last Modified: Thu, 23 Jun 2022 06:41:45 GMT  
		Size: 139.9 MB (139877601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e0e44f68f1a2979ca2068876ae7da5a1f0c01714d6a956fe663f2f28f9ede37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab20306c5069132bb06b29329268f9ba198476d019e87d892aaf3ce2734e132f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:59:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bb1c55b3452215fbd3c902191776c8056a40d8b981530a4760c718eabd1fb2`  
		Last Modified: Thu, 23 Jun 2022 04:03:16 GMT  
		Size: 158.0 MB (158015895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; 386

```console
$ docker pull mono@sha256:6b9f0c5a13b0df94fe37120381befa7a7a838da47809cdd7e61750ccd374aef6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259078850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcfcd03261e069b509d727d927c7c3055a9bafde656ddab4d91cba67eddae6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:00:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3889a12c50905383ca7c05ea29c70a6570224a3d3c598eeea858b8a652213a6`  
		Last Modified: Thu, 23 Jun 2022 04:03:38 GMT  
		Size: 159.9 MB (159904036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0` - linux; ppc64le

```console
$ docker pull mono@sha256:a36a61a79a75faac96928984c885e16dc5341bae264940f42a5be34a44e737f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204233859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb0f938c8562bad3d2e08a792165c349021fcffaf26d84b85331d22b8cfd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:31:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9975e82a149a6eaee70df67907a8f1fd670cdd0ecffe8cd999f41b5074cb9`  
		Last Modified: Thu, 23 Jun 2022 08:39:38 GMT  
		Size: 143.9 MB (143883802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0-slim`

```console
$ docker pull mono@sha256:fcaa25d7d118eac8b9d66135146a0105206dd0ea7d3e23a60e9563e5247aacc7
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
$ docker pull mono@sha256:ce5fec9f6149a6202c0242fc3e649eb5232ebe605379f2d3ef37dbc7af903c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813dedd8591fe7c1f3f073914c9f7c04955ce813eca1d7f8428dc389a52d13af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8c29be2f9d245b365d8f8336ca067ecafe5f7d47d5e166f5c165b4b3e1a31c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09704630f58fa24aeb180e87b94d96c3b947485ce67334a9dda1a008dc2d3c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2cca758f375964ad1c50f290c0ea0cacba46ccfbc61c6ac9b8e54430965ae443
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a08449c8b4b191ee4205a1bc99c781243a6be08d86ebb04d06e38ccf7eb08e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b912a9a3fc92daa6749d801197f3ee1737e82089072cda6a8bbd88ef81c4089f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e9bdff1be7098a2aa07d47d1c9cf8b769e2667f48528b10f39c6a8144a47e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; 386

```console
$ docker pull mono@sha256:0285fbd408e63c399e5b4e4f7267681d71acb1109666aaa483c22950356a3aac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b6b7aeb9563163ff07c47584af59c6dfa008a13fbbe44752ae829ff5a2f27`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0fdda7fdadd09e05567be879251f26eca1b603c6017cf1f6cb128f29257cd27e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cdd98bc63a5f7ad37871b875331ad1005ce7b20ee0ef05652786fb64439bab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.182`

```console
$ docker pull mono@sha256:6c5d93f65380b6439d832cce0210b220aa6f881a57f9409e896c2b540a78500f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.182` - linux; amd64

```console
$ docker pull mono@sha256:20cd1f6970624d00c69b114e95b07676ccc6759b4bfa96d87d2d316456851640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254417452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95165788dbeb36ffdb7a7d8071b13c8aa2338ba749946ac19e68ad93cd748feb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:57:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaae8abfcf8730ac3b34c9af2e194c634d79ab358331c72f2fe28b50fe5e4dc`  
		Last Modified: Thu, 23 Jun 2022 04:04:32 GMT  
		Size: 159.7 MB (159726737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm variant v5

```console
$ docker pull mono@sha256:8aa046ef67f31390b606aa89317cf7f4ba20acd26033d954295baed80353e0a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa301c44b356146dc040190aed33fd0cca784625d0373c0d9ef9cbe574bdd304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:54:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07364fcd207cbc719207643ef95f8aeafc3a0f9e643868b571e5727f07e0c4f`  
		Last Modified: Thu, 23 Jun 2022 03:02:40 GMT  
		Size: 141.0 MB (141020175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm variant v7

```console
$ docker pull mono@sha256:55b20826ffcc17aafa45701264c09278d7a2973cf733b9ccec05665c2943c207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188781499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ffec2694682ff07163bbea623875ce9eaec1eea0ad55ad7e1f2005d03c10b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:34:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c98ca037e20a62b0cced06c13b8c6fc9e9ba64fbaf561f4fa8f5406a0bbb6`  
		Last Modified: Thu, 23 Jun 2022 06:41:45 GMT  
		Size: 139.9 MB (139877601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e0e44f68f1a2979ca2068876ae7da5a1f0c01714d6a956fe663f2f28f9ede37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab20306c5069132bb06b29329268f9ba198476d019e87d892aaf3ce2734e132f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:59:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bb1c55b3452215fbd3c902191776c8056a40d8b981530a4760c718eabd1fb2`  
		Last Modified: Thu, 23 Jun 2022 04:03:16 GMT  
		Size: 158.0 MB (158015895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; 386

```console
$ docker pull mono@sha256:6b9f0c5a13b0df94fe37120381befa7a7a838da47809cdd7e61750ccd374aef6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259078850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcfcd03261e069b509d727d927c7c3055a9bafde656ddab4d91cba67eddae6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:00:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3889a12c50905383ca7c05ea29c70a6570224a3d3c598eeea858b8a652213a6`  
		Last Modified: Thu, 23 Jun 2022 04:03:38 GMT  
		Size: 159.9 MB (159904036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182` - linux; ppc64le

```console
$ docker pull mono@sha256:a36a61a79a75faac96928984c885e16dc5341bae264940f42a5be34a44e737f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204233859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb0f938c8562bad3d2e08a792165c349021fcffaf26d84b85331d22b8cfd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:31:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9975e82a149a6eaee70df67907a8f1fd670cdd0ecffe8cd999f41b5074cb9`  
		Last Modified: Thu, 23 Jun 2022 08:39:38 GMT  
		Size: 143.9 MB (143883802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:6.12.0.182-slim`

```console
$ docker pull mono@sha256:fcaa25d7d118eac8b9d66135146a0105206dd0ea7d3e23a60e9563e5247aacc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `mono:6.12.0.182-slim` - linux; amd64

```console
$ docker pull mono@sha256:ce5fec9f6149a6202c0242fc3e649eb5232ebe605379f2d3ef37dbc7af903c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813dedd8591fe7c1f3f073914c9f7c04955ce813eca1d7f8428dc389a52d13af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8c29be2f9d245b365d8f8336ca067ecafe5f7d47d5e166f5c165b4b3e1a31c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09704630f58fa24aeb180e87b94d96c3b947485ce67334a9dda1a008dc2d3c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2cca758f375964ad1c50f290c0ea0cacba46ccfbc61c6ac9b8e54430965ae443
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a08449c8b4b191ee4205a1bc99c781243a6be08d86ebb04d06e38ccf7eb08e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b912a9a3fc92daa6749d801197f3ee1737e82089072cda6a8bbd88ef81c4089f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e9bdff1be7098a2aa07d47d1c9cf8b769e2667f48528b10f39c6a8144a47e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; 386

```console
$ docker pull mono@sha256:0285fbd408e63c399e5b4e4f7267681d71acb1109666aaa483c22950356a3aac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b6b7aeb9563163ff07c47584af59c6dfa008a13fbbe44752ae829ff5a2f27`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:6.12.0.182-slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0fdda7fdadd09e05567be879251f26eca1b603c6017cf1f6cb128f29257cd27e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cdd98bc63a5f7ad37871b875331ad1005ce7b20ee0ef05652786fb64439bab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:latest`

```console
$ docker pull mono@sha256:6c5d93f65380b6439d832cce0210b220aa6f881a57f9409e896c2b540a78500f
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
$ docker pull mono@sha256:20cd1f6970624d00c69b114e95b07676ccc6759b4bfa96d87d2d316456851640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254417452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95165788dbeb36ffdb7a7d8071b13c8aa2338ba749946ac19e68ad93cd748feb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:57:29 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaae8abfcf8730ac3b34c9af2e194c634d79ab358331c72f2fe28b50fe5e4dc`  
		Last Modified: Thu, 23 Jun 2022 04:04:32 GMT  
		Size: 159.7 MB (159726737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:8aa046ef67f31390b606aa89317cf7f4ba20acd26033d954295baed80353e0a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa301c44b356146dc040190aed33fd0cca784625d0373c0d9ef9cbe574bdd304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 02:54:46 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07364fcd207cbc719207643ef95f8aeafc3a0f9e643868b571e5727f07e0c4f`  
		Last Modified: Thu, 23 Jun 2022 03:02:40 GMT  
		Size: 141.0 MB (141020175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:55b20826ffcc17aafa45701264c09278d7a2973cf733b9ccec05665c2943c207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188781499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ffec2694682ff07163bbea623875ce9eaec1eea0ad55ad7e1f2005d03c10b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 06:34:14 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c98ca037e20a62b0cced06c13b8c6fc9e9ba64fbaf561f4fa8f5406a0bbb6`  
		Last Modified: Thu, 23 Jun 2022 06:41:45 GMT  
		Size: 139.9 MB (139877601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:4e0e44f68f1a2979ca2068876ae7da5a1f0c01714d6a956fe663f2f28f9ede37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215904592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab20306c5069132bb06b29329268f9ba198476d019e87d892aaf3ce2734e132f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 03:59:39 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bb1c55b3452215fbd3c902191776c8056a40d8b981530a4760c718eabd1fb2`  
		Last Modified: Thu, 23 Jun 2022 04:03:16 GMT  
		Size: 158.0 MB (158015895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:6b9f0c5a13b0df94fe37120381befa7a7a838da47809cdd7e61750ccd374aef6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259078850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcfcd03261e069b509d727d927c7c3055a9bafde656ddab4d91cba67eddae6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 04:00:38 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3889a12c50905383ca7c05ea29c70a6570224a3d3c598eeea858b8a652213a6`  
		Last Modified: Thu, 23 Jun 2022 04:03:38 GMT  
		Size: 159.9 MB (159904036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; ppc64le

```console
$ docker pull mono@sha256:a36a61a79a75faac96928984c885e16dc5341bae264940f42a5be34a44e737f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204233859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dfb0f938c8562bad3d2e08a792165c349021fcffaf26d84b85331d22b8cfd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Thu, 23 Jun 2022 08:31:16 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9975e82a149a6eaee70df67907a8f1fd670cdd0ecffe8cd999f41b5074cb9`  
		Last Modified: Thu, 23 Jun 2022 08:39:38 GMT  
		Size: 143.9 MB (143883802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:slim`

```console
$ docker pull mono@sha256:fcaa25d7d118eac8b9d66135146a0105206dd0ea7d3e23a60e9563e5247aacc7
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
$ docker pull mono@sha256:ce5fec9f6149a6202c0242fc3e649eb5232ebe605379f2d3ef37dbc7af903c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94690715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813dedd8591fe7c1f3f073914c9f7c04955ce813eca1d7f8428dc389a52d13af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:55:13 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:55:22 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:55:40 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3589152b6523bbb0d77bc8d51521b914e69de07a3e616f39912aaeabcb7d42df`  
		Last Modified: Thu, 23 Jun 2022 04:03:19 GMT  
		Size: 2.8 MB (2777590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca9c48df2a21a216d9428c812c0f9242c5e1a847aee974c1c50ef02e538f9b9`  
		Last Modified: Thu, 23 Jun 2022 04:03:28 GMT  
		Size: 64.8 MB (64773082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v5

```console
$ docker pull mono@sha256:8c29be2f9d245b365d8f8336ca067ecafe5f7d47d5e166f5c165b4b3e1a31c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51861264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09704630f58fa24aeb180e87b94d96c3b947485ce67334a9dda1a008dc2d3c6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:48:21 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 02:48:52 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 02:49:41 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1928693720fa8f45d5c2a7b5bd9c626537e86bea2d614737cadcc209640d9`  
		Last Modified: Thu, 23 Jun 2022 02:59:51 GMT  
		Size: 2.5 MB (2467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1895d8cd1362df3c2cf6d14227bbe350252bd89da43c6ed23eefb3c2c365a6d2`  
		Last Modified: Thu, 23 Jun 2022 03:00:08 GMT  
		Size: 24.5 MB (24503512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:2cca758f375964ad1c50f290c0ea0cacba46ccfbc61c6ac9b8e54430965ae443
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a08449c8b4b191ee4205a1bc99c781243a6be08d86ebb04d06e38ccf7eb08e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:28:17 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 06:28:42 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 06:29:26 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6c97083c92d0336db0f420054535d459a59f67557ff2bb20dd373ec47819f1`  
		Last Modified: Thu, 23 Jun 2022 06:38:59 GMT  
		Size: 2.4 MB (2366974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2464437aa6946d005aa7325e15236ed48e4c876e16cd89689e4bde87a8770e`  
		Last Modified: Thu, 23 Jun 2022 06:39:15 GMT  
		Size: 23.8 MB (23788924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:b912a9a3fc92daa6749d801197f3ee1737e82089072cda6a8bbd88ef81c4089f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57888697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e9bdff1be7098a2aa07d47d1c9cf8b769e2667f48528b10f39c6a8144a47e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:57:33 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:57:41 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:57:57 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b465b23b404592bcec4f22096ff3b87aead20242b44fda057d36ca097e48da30`  
		Last Modified: Thu, 23 Jun 2022 04:02:07 GMT  
		Size: 2.6 MB (2641221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e70f21f27d3d23ed773e000db41507cf8f0ecac9447d75e0acd5b10b6fc45`  
		Last Modified: Thu, 23 Jun 2022 04:02:12 GMT  
		Size: 29.3 MB (29333447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:0285fbd408e63c399e5b4e4f7267681d71acb1109666aaa483c22950356a3aac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7b6b7aeb9563163ff07c47584af59c6dfa008a13fbbe44752ae829ff5a2f27`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:58:18 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 03:58:27 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 03:58:49 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91472903337356acf68250820a4b4f41c9d74247d43707024d22d8f87983e93`  
		Last Modified: Thu, 23 Jun 2022 04:02:20 GMT  
		Size: 2.8 MB (2789301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5b1872642938071444396e61da6437c9cdce36e754eb153f64e8707e78418f`  
		Last Modified: Thu, 23 Jun 2022 04:02:30 GMT  
		Size: 68.6 MB (68585971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; ppc64le

```console
$ docker pull mono@sha256:0fdda7fdadd09e05567be879251f26eca1b603c6017cf1f6cb128f29257cd27e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60350057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cdd98bc63a5f7ad37871b875331ad1005ce7b20ee0ef05652786fb64439bab`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:22:22 GMT
ENV MONO_VERSION=6.12.0.182
# Thu, 23 Jun 2022 08:23:15 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Thu, 23 Jun 2022 08:24:15 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c5e74ddd7a50265c26382df8e6d39f1275c29ebc1710420f1a8de23ad6022b`  
		Last Modified: Thu, 23 Jun 2022 08:38:24 GMT  
		Size: 2.9 MB (2892723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc549645d7f42d930bbcfad7b0dfad17c219dc5b38c2d6b5ff362ed0cb7d8cd8`  
		Last Modified: Thu, 23 Jun 2022 08:38:29 GMT  
		Size: 26.9 MB (26897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
