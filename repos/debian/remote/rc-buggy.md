## `debian:rc-buggy`

```console
$ docker pull debian@sha256:e60a653e91928537ed40b0e710b40652e2d84eb6983dc30564cc7b6048abf6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:3a4c3cd5c45f6725d6e0b15e200ef0fddea069c6f3435e1e6acda6da063b2caa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea445cd8a5977acf202de4a5dc3713b702db04de630e3d5aa27e284432b501a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:21:50 GMT
ADD file:4bfda8f11e59383c37bfa6038bb5d22f58b9724d249a62568a2e7d2908821cd3 in / 
# Tue, 04 Jul 2023 01:21:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:23:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6efa412d16b908043ec01c4ac9ff7323c0f488dd5d7ea4b9b086f1e80350b9b3`  
		Last Modified: Tue, 04 Jul 2023 01:27:46 GMT  
		Size: 49.5 MB (49475944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5938779f7041d2eed56d07a832f8b26100c8c792d5c70dbd81ee104db155b96`  
		Last Modified: Tue, 04 Jul 2023 01:30:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:8431f23413f063c89ca1c5c6bc53816226370f5d807f28478533251d83a23ca3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47322701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31435e717296b9e24b2c39649540a77f07be5b3086d293441493344b7841809`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:49:11 GMT
ADD file:e6181e27889c016519d8d701345aafff7138df96a76fb6a29403c8a33a3365fe in / 
# Tue, 04 Jul 2023 00:49:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:50:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:667272d8fe1bc81ce33874dbc84976c86d6b95f50198465a6ab672c71d87f666`  
		Last Modified: Tue, 04 Jul 2023 00:53:33 GMT  
		Size: 47.3 MB (47322473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2190885d65eb97f69c0c7c0c158851e72bdf60e2cfdb2b1136c8de3f6dd6c37f`  
		Last Modified: Tue, 04 Jul 2023 00:56:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:7ab5870e0bdbdeeecef461a5b5fbb2906ea9ee2ef4c5da1c1b8998deed1c8a18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfc027409f8fba31974738384e2dfa1f2a1a243b3f73b6fd5e1b69f93300462`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:59:44 GMT
ADD file:5be8eee7722dc860882f26018d8a0de49a4db6fcaa0f35d1dfbb74eff22929cb in / 
# Tue, 04 Jul 2023 00:59:45 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:01:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:42cc2becb0b735f0260d9f678fb1201bbe47c438212c5faf04879fab6a2dd73f`  
		Last Modified: Tue, 04 Jul 2023 01:05:43 GMT  
		Size: 45.1 MB (45123975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce68afc01eaea6b552daf2fa88d7caafdad8a2a5bd322b779b58e945322376f`  
		Last Modified: Tue, 04 Jul 2023 01:08:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:74c35a88542099de6bc301d5b0a41b91f478e0a136693a73b6b828c07870f328
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49482793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7dc11db86b8fe46faa58399faa8901211dd196a273b814306fc856887243c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:49 GMT
ADD file:2c2c0588b93f9af7d93f19033795edf9e61a692ff56e65d9e9500915276782c9 in / 
# Tue, 04 Jul 2023 01:58:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:00:05 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d1b52151d5bb774f3680f8697c343bae1b64b7308354db57dc6bbeb7d65d0964`  
		Last Modified: Tue, 04 Jul 2023 02:03:59 GMT  
		Size: 49.5 MB (49482570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40b228ca99236a2bb77881dfde126d9e56af64935e3319b6656cb719d0eee3f`  
		Last Modified: Tue, 04 Jul 2023 02:06:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:c959765e87be9a204eac6d8182448e6bba3f6609eb0400c88e076fa894e29e19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50506052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ad128766c27fb0dd4f93bcb68388825c995b17b3ad06da40fc6b11fdd05f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:40:19 GMT
ADD file:565f8487c71b5de967f1bf16d4bd86291107b68f4152a61e35a8ab86e9f83b7b in / 
# Tue, 04 Jul 2023 01:40:20 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:42:05 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:46685592106ba6554716942e180f6b4cd8a73f1ec934554b40aee89b47118f5e`  
		Last Modified: Tue, 04 Jul 2023 01:46:32 GMT  
		Size: 50.5 MB (50505825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74b547e670384f06e7000b09b5fc6ab9f25571d708e00fec2c351140f5d3b4`  
		Last Modified: Tue, 04 Jul 2023 01:49:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:e22162bafbe5ff7e199da64bdbb05a5e1a9d73af060a0cec82099bc3e314584e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49455626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551188c58f26c946df80410bde70b326be018cf165af6aaa6c09ab618459e2ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:12:32 GMT
ADD file:ab2873cb088258c79fab5dde2d754d1967ca11e58adcf6a08811206759a323d5 in / 
# Tue, 04 Jul 2023 01:12:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:18:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:796c2f1009ce9a433d10a1f4708cbb79ef733dcb0ca992041a6aa621e85d8410`  
		Last Modified: Tue, 04 Jul 2023 01:23:15 GMT  
		Size: 49.5 MB (49455398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619a4904f147ba7ddbe54aa9fa10e34000a998f58d5372d5f112bd3a1bbdc738`  
		Last Modified: Tue, 04 Jul 2023 01:28:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:7f4da65286d7e5db96f60b1cb22b5c07676ee5b56162370fe299912a934f2d1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53474639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea78d3f7f329c36df0d2b483eda4e8cb72aed603a61fd9a9408b594257a6e396`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:33 GMT
ADD file:4c1d6f76704d32b9b503bd61c4b485555ec28037fb500403ffb5cbb102cf4509 in / 
# Tue, 04 Jul 2023 01:19:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:22:43 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3e4e6efa69b637e0e8ca00ddcae1aed23aef874a92a2904bdc6c9fa5b3212b8a`  
		Last Modified: Tue, 04 Jul 2023 01:27:02 GMT  
		Size: 53.5 MB (53474414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7222666516418e1bc453a1d0aa1c322401427d980c317645d0ced94a082bcf88`  
		Last Modified: Tue, 04 Jul 2023 01:31:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:ab30641b065b5a26db630781063daaa6bee194f8a3d62c163f1f05dd6ec5780a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47890991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5e583fbbb5738a6f1ec6510b1001913887d33ac5540dbdce71a8a1d000a762`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:33:27 GMT
ADD file:9c12086273bf86ac1b3f72beebd17cc357bb749a95ac64d0f5ecdbbe7631cec4 in / 
# Tue, 04 Jul 2023 01:33:29 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:35:49 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3dcb3b9eb8abea3e1994db2e9f2073832965384334d3e204d1df1e3dcd09cffa`  
		Last Modified: Tue, 04 Jul 2023 01:38:16 GMT  
		Size: 47.9 MB (47890767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2e9a34da129975469d0fb165471084cb9ad56a688067ce780bfbe786020397`  
		Last Modified: Tue, 04 Jul 2023 01:40:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
