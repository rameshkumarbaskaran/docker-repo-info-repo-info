## `debian:experimental`

```console
$ docker pull debian@sha256:7268a6e2fa426ee10250dde3d993d3c0d4aabe5219db3d68af7453a059b47273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:34995eaf705607851efddaef93e865492658b3bd53480ba85aa56687917e3c04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54868394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e70b2d362969f4827158a910933dfdacf806179bec392253e89a36e4ac0b433`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:24:09 GMT
ADD file:0e5e388b45fcf11e249e8872c207386a244657c52eb31b8a071558a030f7445c in / 
# Fri, 26 Mar 2021 15:24:10 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:24:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:35be82d9f1bb585df090c8b1ece3f6fa8bd3c6a8b09656b19b64d7a29fcf23b4`  
		Last Modified: Fri, 26 Mar 2021 15:34:09 GMT  
		Size: 54.9 MB (54868171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c14edf6366b8a9f46ec73c30dcaf02a61688feb572d78dff271601f107be4a`  
		Last Modified: Fri, 26 Mar 2021 15:34:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:e6a9dfb39feb4fd4dda653c0a314139016da9f96eb63ad81fb138789232b8869
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52402643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ecf2885ec922297062365506f6d406c87094025e7d94466c6c9c135ed67dc8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:57:13 GMT
ADD file:32612d584d6e838fda991bcee065f36db394c6848444220ab925641eed015030 in / 
# Fri, 26 Mar 2021 07:57:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:57:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ea6af2ab5e68178d221322a9de282a1dc71dad081d87e92a0861e9cbd6b706cd`  
		Last Modified: Fri, 26 Mar 2021 08:05:41 GMT  
		Size: 52.4 MB (52402421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa483613c27c2a61b6db5546785369669d2578b1680819499ead7e37599ec18`  
		Last Modified: Fri, 26 Mar 2021 08:06:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:32644de6b358ffe01575b9e40ef774434d110f95ab14e496fdcda14531f4960c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50071404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152ba7496a9b1df42d58cbd475bddcbab1be8810e7cc9412cf45007ed0b2aed2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:24:04 GMT
ADD file:e1d5e4c7271fc5fa55d179768a79a0c6de2e179ee0bb16862bde35ca8e55eb96 in / 
# Fri, 26 Mar 2021 11:24:06 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:24:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fada62bc534bd047cc273dfb6f0f66fb5d1475ae32d4a65bec935661d502b55c`  
		Last Modified: Fri, 26 Mar 2021 11:32:37 GMT  
		Size: 50.1 MB (50071182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c455c1fe90483c2d4575e1676d087140eda7102553a82c31700d472d6688cb`  
		Last Modified: Fri, 26 Mar 2021 11:33:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:50185f99a2d612b9f093c459494a1bd23dd9e57a0b1886ec2db3ad67e8e3c7d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53556195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19780dc253df51bc321651039357ed874a84ba96d9e56eb236b97a21c54b38aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:45:47 GMT
ADD file:13a3dda32dcf7677f42adb383c0309e1a68b93cb2af6d2b2e5742d400ba95cdc in / 
# Fri, 26 Mar 2021 15:45:50 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:46:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4ee953709f00c4d1ec53e4fe1a5289fc0e2e5a72f2f048d89ae7c7c40f949e36`  
		Last Modified: Fri, 26 Mar 2021 15:52:27 GMT  
		Size: 53.6 MB (53555972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeaabb40bd8cbe4c6f966981d59ec296afb914172547cfb2fba75b09e12a20a`  
		Last Modified: Fri, 26 Mar 2021 15:52:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:005571f0b8436ae12f3170d00c99d3e72b27bdf5bd0edb2f1dd47ad4c045d217
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55881964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e18cc5bd3b39fd21c62dc18de176008d0fe3c49054d1002e4235d3783bf68f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:57:04 GMT
ADD file:3190a0fb27e5ad69c27ae37ac99c2d5e2ef3f4ba26ba0ac19bcfc13efe794dc3 in / 
# Fri, 26 Mar 2021 13:57:05 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:57:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a2e7e9c1cd5c1ba0aee50a3a39bb6804a94aef0c896d71f0366c47ea069e1685`  
		Last Modified: Fri, 26 Mar 2021 14:08:27 GMT  
		Size: 55.9 MB (55881743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e614388bf741b241e81072d1f412a89db1c55171f258e6ff34c0c7a0b899053`  
		Last Modified: Fri, 26 Mar 2021 14:08:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:f8a69b4993283e7f37546958ca36a488ea80857d996f3f278dfb7676f2fa5feb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53127031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8367223de90e6e5ed6869860066c83594e0cf319b09af633fa8cb3bb30d322bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:12:45 GMT
ADD file:c79a17a0f871c489c33a2d475b8e5371996f90bbc7760e45557108da54e86545 in / 
# Fri, 26 Mar 2021 08:12:46 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:13:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:75c364cc452cddccfec518752d444a6600aed010f6c6fb415dd2924ecd097fa8`  
		Last Modified: Fri, 26 Mar 2021 08:21:20 GMT  
		Size: 53.1 MB (53126809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee942771ebd98062575efc7cc7107c8dc519eee1e1d12981ade8d08be4bc8a5`  
		Last Modified: Fri, 26 Mar 2021 08:22:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:2a3d2559d1f6cbc7f836fa46acf61c21676c6b318cae670c8d091018c1778e3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58782957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5595f1f92f36c9feb38868dad22fb67e1d9c4cba8670a2901e86c78f3329adae`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:18:01 GMT
ADD file:be5abfe9e637b00dcaab25c23dd05982cdd5411a56ada380779fe45812c768c6 in / 
# Fri, 26 Mar 2021 15:18:13 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:18:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f7a13c2346e072d25dcd65c1eb0a0f045d45c24fde8c9eb9a03d1f6c9795c957`  
		Last Modified: Fri, 26 Mar 2021 15:25:07 GMT  
		Size: 58.8 MB (58782734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21795ad61e64a4ef6261eae3151856a49f2a03b278245925fe28db26f7d8bcee`  
		Last Modified: Fri, 26 Mar 2021 15:25:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:67371218461743627b3d651ae87a54d278bf02302851f73bf4a3dd6edef95436
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53147631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c29905e7b765d9f00e2daa83295d56d9ce7c43212a1fae6e0e93d31c81af2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:55:39 GMT
ADD file:be0444532eac39590c141ccfa52d1b344c0d211c810693d49ca4097a2d815356 in / 
# Fri, 26 Mar 2021 10:55:42 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 10:55:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:91a464b0980fed0c0cdac10a0067b2f7fee33fca30d4b13b011215700fb80fb8`  
		Last Modified: Fri, 26 Mar 2021 10:59:24 GMT  
		Size: 53.1 MB (53147412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5aaafdce3fce4144797817f76d6dbcc3d77684dfc39c41488fc08b3e77d3ff8`  
		Last Modified: Fri, 26 Mar 2021 10:59:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
