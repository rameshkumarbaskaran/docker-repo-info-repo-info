## `mono:latest`

```console
$ docker pull mono@sha256:ea2e5fce7163b2143e13b9924e33b4c37bbb909f9bd1f515d1a0ba9c2361248c
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
$ docker pull mono@sha256:383d4fe1653514976ea995575b41ee170c3c8eccde87fedd81ef03519b5fc150
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254416514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5114070326330f05ab9898e3312c089765218e21d724ca2289cbc1da8ed9f8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:46:10 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 12 Jul 2022 04:46:19 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jul 2022 04:46:38 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jul 2022 04:48:28 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f189b1d9187b09576424edce83f47e92588caef3a71d9beef58e599db808b452`  
		Last Modified: Tue, 12 Jul 2022 04:54:31 GMT  
		Size: 2.8 MB (2777600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aaba05b89bfb7aa4a752f16b6d1be39ea8f923ab47f0d33363b586afa0eca36`  
		Last Modified: Tue, 12 Jul 2022 04:54:41 GMT  
		Size: 64.8 MB (64772860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43458412e336b06b838ff702f957d051ed1515759967732d2296dad7b5a08b5d`  
		Last Modified: Tue, 12 Jul 2022 04:55:44 GMT  
		Size: 159.7 MB (159726204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v5

```console
$ docker pull mono@sha256:37225829a6bdde7b997951ce73dd9a04b0c0658f00c45dc9ffde56a9aca34819
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192881656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03aa84c02bb651bb9a7afd203df46d03e6f4448937b44076e4578b44499ce9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:51:40 GMT
ADD file:ae02bb368b4b8ce35a4d250031394d4c6d9e5be3b02168f34922bd87dd2bc726 in / 
# Tue, 12 Jul 2022 00:51:40 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:34:51 GMT
ENV MONO_VERSION=6.12.0.182
# Tue, 12 Jul 2022 02:35:18 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gnupg dirmngr ca-certificates   && rm -rf /var/lib/apt/lists/*   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF   && gpg --batch --export --armor 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF > /etc/apt/trusted.gpg.d/mono.gpg.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && apt-key list | grep Xamarin   && apt-get purge -y --auto-remove gnupg dirmngr
# Tue, 12 Jul 2022 02:36:06 GMT
RUN echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official-stable.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
# Tue, 12 Jul 2022 02:41:17 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:e0c9a5e64041e18deb764eddbdc6c3d20b76797d8c2e2eb4c60d4cba21dc486e`  
		Last Modified: Tue, 12 Jul 2022 01:04:31 GMT  
		Size: 24.9 MB (24889765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76de0e77876daa6a97d104c5c9f00ced96370f3b3cdf164cf91f2bb3aff45eb8`  
		Last Modified: Tue, 12 Jul 2022 02:46:19 GMT  
		Size: 2.5 MB (2467737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eaaa9dfc40b8234b095a6c964c082d62afa2aeea8a1073add374a342ff3b82`  
		Last Modified: Tue, 12 Jul 2022 02:46:37 GMT  
		Size: 24.5 MB (24503508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a64267ed6955d2eb1c8f874cb86523ac523e28ef52b2a98bbe5d82d6629073c`  
		Last Modified: Tue, 12 Jul 2022 02:49:10 GMT  
		Size: 141.0 MB (141020646 bytes)  
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
