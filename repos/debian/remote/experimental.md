## `debian:experimental`

```console
$ docker pull debian@sha256:c4634ddf272060ed2099cebc69e15f8bade63c3f890056cdd892ac916b103e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:ee4b8c2d0a9942a34081ab933f668376bf35d3525a20cd06eed4afb0e403ac43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61ad82957c77ec101ad1f1f2dd1ddcd8ee8e2b3208954218bcf86f17ff14bb3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:23:27 GMT
ADD file:30c3621d27a742c3c20865fd70d8aa41d70be0f58eeeb81aaa9dd1298ecb1c1d in / 
# Tue, 04 Jul 2023 01:23:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:23:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:52ab46b1411e2672033a4f02a5e7df836c372c7d9366d0f10b15751b45a6a217`  
		Last Modified: Tue, 04 Jul 2023 01:29:49 GMT  
		Size: 49.5 MB (49475947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bcd11045bd376dd6392c60ec34a96bc530004eb87177deb7ed1f0fca348007`  
		Last Modified: Tue, 04 Jul 2023 01:30:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:8c0a40eb00289d699534f5b060d1c9e9bb61b508c6d5fc662606ba1f250b07c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47322694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883bff7d7307e93e117c0640650f6717d50ba33c539fecd83d3e1638c5d7f5a1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:50:15 GMT
ADD file:0d73a7183a38c56858e61e53f0c64ae6eaf9d58311df1be7af3b37f1e1769dd2 in / 
# Tue, 04 Jul 2023 00:50:16 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:50:26 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:eb46e2b513bf023b4297bc46404f96d3a604f8f913dffe3d1f9e5c5c530e9caf`  
		Last Modified: Tue, 04 Jul 2023 00:55:44 GMT  
		Size: 47.3 MB (47322476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b079d533182e62457871a1cdecd8b7307dda1c497fda642b534f1738b904b1aa`  
		Last Modified: Tue, 04 Jul 2023 00:56:07 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:8e140ce88bd505eebe36c6aebac98f5303b50a067126409f0fc4831ad06b5bc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e332aa22a3f6fe878a99005e2a42ca5ff1c89e17e08b81d9010ed364042cab74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:01:20 GMT
ADD file:a7c3220804fb0e3fd658c0492b5338ba9fc6c132f28282486bbae9622138fd0e in / 
# Tue, 04 Jul 2023 01:01:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:01:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0807315011437359206e59c75af82e26e89ba45ae9281fa33df5e8dda8de17a2`  
		Last Modified: Tue, 04 Jul 2023 01:07:56 GMT  
		Size: 45.1 MB (45123977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c69a5003d0ef8f39c11e33430cc1570553f8fa01a641e6fb1694acb22e771`  
		Last Modified: Tue, 04 Jul 2023 01:08:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:abe37a32bdce7748581b71305d7931bce1e4abd16e6375cf3c78f7723245dcfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49482796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b87baf1354ffa1f14b4908bccf3c4a3860a493a5aea93544a889e0b72bcd05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:59:53 GMT
ADD file:bf1bc62117abf0b13f8992acfed17c5505f88edece9bdb42c246d3801869a909 in / 
# Tue, 04 Jul 2023 01:59:53 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:00:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d63178d4b98b5ec11651f31157085c27b04daa9271f1b4a8be773b8ad11c4264`  
		Last Modified: Tue, 04 Jul 2023 02:05:57 GMT  
		Size: 49.5 MB (49482573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d026073039c25e9ee2a17496721f4ceac9ef9e94a28fd58dfa36d329874a2`  
		Last Modified: Tue, 04 Jul 2023 02:06:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:f040efe89db35f2e92448e942f4ab4233ef1a49a962416c604d5b930e8db2798
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50506050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0471ac8119bae30367e8fd4578fc459e80d2028f8d586be4e41431b3e416d96`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:41:50 GMT
ADD file:2f42b2e397b1e8bc6959dbfa501dddc91fd18f0d3ef0fd9ea0663092286e1429 in / 
# Tue, 04 Jul 2023 01:41:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:42:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d6a8ba1eaf3690a5e9b7f2debed87f9cfac7972349e43494cf2b7feffb143629`  
		Last Modified: Tue, 04 Jul 2023 01:48:54 GMT  
		Size: 50.5 MB (50505827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d36e6b4e6c369b3f3ab10d1e9f74b10daac252de8e79569017d2dc1415f745`  
		Last Modified: Tue, 04 Jul 2023 01:49:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:75e9871043a230eb22857b46f45c5191a6701ee9ee823e0ba9c973bd75a6a18c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49455622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeee7aeea20c741a739b5b6e2a1237c759a78b48ae5be20b7dbdafa85ec0d129`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:17:08 GMT
ADD file:20580fa5e83e1873d44c46cb2f9ac1fe39a42c62c9d4e3756723283f13add821 in / 
# Tue, 04 Jul 2023 01:17:14 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:17:54 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:78d3f505f592dc293a56dbf6460a5f68fd63cf76766388835e32dcbc804fc180`  
		Last Modified: Tue, 04 Jul 2023 01:27:58 GMT  
		Size: 49.5 MB (49455401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b5720ed9039a06c54aba388df180e92b4c556fb4ba1c2f5f088a9a43bb3ce1`  
		Last Modified: Tue, 04 Jul 2023 01:28:36 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:70d80edab92dc523ddfd8c6b98a75b5e774696097575f336ae3d38bcef02c508
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53474637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4711487b2be5f72a8d3521f4b1c7e786104d126cb169b7004b4accd52543711e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:22:15 GMT
ADD file:d5d2b24ead06183959c90a6751c80a887c556ca4f0fdc7d287812576eafb1a60 in / 
# Tue, 04 Jul 2023 01:22:18 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:22:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:af5bbdab36f44ac3e6bea7dc4ed1c8b357c4862d3c25a3ec040d72e425ef159c`  
		Last Modified: Tue, 04 Jul 2023 01:30:28 GMT  
		Size: 53.5 MB (53474416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d118ef2a0ad933e33a89e18d137c4a8285f20f4c4e78b17f17003ab68b62e6`  
		Last Modified: Tue, 04 Jul 2023 01:31:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:fd8164a7bd9565294d8f433d478adcc1f7371e0ad3431c78beb30d80bbaf2aae
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45695712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db54503fa0f89e6f3eee133d4dec5dc6027fdaf9f340fdb7affc4e93354b751`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:32 GMT
ADD file:bacf5c7bb4f9db293679962e5936b1037a72a2e667da59236cda267c866ad8e2 in / 
# Tue, 04 Jul 2023 01:10:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:11:21 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:892c64510625aa4b95222221c8d62ebbab44da937d39c14956f6e6697a5c4c80`  
		Last Modified: Tue, 04 Jul 2023 01:13:59 GMT  
		Size: 45.7 MB (45695485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58595682130886a8914b61a3a37dc1da553893a9cf3815062133cff2dfff8ee6`  
		Last Modified: Tue, 04 Jul 2023 01:14:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:aeb5c42953c63cbc5db2e38bc861b5d763d6876b3ef94393d7d16063d22239bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47890989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda98194a8a1698694a72384adfbe1278c95e996163b69b2fbe80c3969745370`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:35:23 GMT
ADD file:aac2397e3a90e63ce8e13930d00bcbee000d5f021a613a196e495f1c36aeeef1 in / 
# Tue, 04 Jul 2023 01:35:26 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:35:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4385878fa0020ea8459bcfa951b29983c0576d085fba63f0b00e83da8014aa50`  
		Last Modified: Tue, 04 Jul 2023 01:39:52 GMT  
		Size: 47.9 MB (47890770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897be0a75f527f567bcbd09694a659cae32e79ab2be66f4dcc6110a9c3d665f9`  
		Last Modified: Tue, 04 Jul 2023 01:40:08 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
