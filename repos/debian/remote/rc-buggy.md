## `debian:rc-buggy`

```console
$ docker pull debian@sha256:7d87cbd50db0fc98ba1c92258b11da53c53c56c7052a4501e4ecfd008f72c7b9
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
$ docker pull debian@sha256:44263d20df1fc634877f59256459bf6ac75502a1e17da3a99e0229be04b11fba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56112788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96b6ea729e5e4feca37bbd1123cd9d51b5024a3907505f027ff059ec1f566b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:44:37 GMT
ADD file:859abf2d579747b132742454ad96e32dc879955afff8af84fab63dc41312a0e0 in / 
# Wed, 20 Apr 2022 04:44:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:46:10 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:212be0dc3a8ffdc400158a5e3a9812f7413dbb5a86269ff50e41b84b37fdb9f7`  
		Last Modified: Wed, 20 Apr 2022 04:50:51 GMT  
		Size: 56.1 MB (56112566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dd6831f9568bd76d2215a05bb28aeb4f27d47c57302f6f79005a3cca616fcc`  
		Last Modified: Wed, 20 Apr 2022 04:54:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:11dd601e6cf9b92dd2b1b9bd1a3bac7255dbbf6e9087488f5ab62151f83bdfd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53206691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503b1738ccfed6cfc9ae2e6b9caa241899a4f30f09c4317b4519ec36e0b6f6f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:53 GMT
ADD file:8fcd736cc488ae6bc3f8a0a57f5454dbd34b0c05fd62d2bf748eeb34723c2a85 in / 
# Tue, 29 Mar 2022 00:53:53 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:58:18 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:07dd120b73b0ec25351ce0c0743306437c1d81e0ee7e06f053f28a0e58bfa81f`  
		Last Modified: Tue, 29 Mar 2022 01:09:52 GMT  
		Size: 53.2 MB (53206463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49f068b998206c6769e1559923f59236db7f962f81aad7f1a4d1002396a49b3`  
		Last Modified: Tue, 29 Mar 2022 01:15:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:eaebc6b06d1c4b3481f15967c6531fc2a23b178e4160b757fcbac1dcbc6b5c6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50813569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957fbfbd3ad31332b8d8a81193bcf1db2e2f263cad7f6173dd38257f84f649ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:22:06 GMT
ADD file:c6f82841459351fabc9a42dbd56f6622b4374e2c684eb76537d4f31022fe8774 in / 
# Tue, 29 Mar 2022 02:22:07 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:26:50 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:20059c5e4ca7052150ded6116965ea89f37bd64493315e1aa29821f6adc82ee1`  
		Last Modified: Tue, 29 Mar 2022 02:38:27 GMT  
		Size: 50.8 MB (50813342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc60f13238f0b35f72a3e59e46562e4bc7fe7dc619acb8bb99ebb4f1608b7303`  
		Last Modified: Tue, 29 Mar 2022 02:44:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f2c882c8c2fa7ca3e90ae4d4330e68553c48c42043e5537c185412bc31895fa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55064030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15628421858686cee7f25a0ec8d68dc32ffccf4706c58be07f6ca579e7029de8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:30:37 GMT
ADD file:21175f4b5f80ba5d755041ff362152a8991b53f89e3c6699275e0c99f6ff6acd in / 
# Wed, 20 Apr 2022 04:30:38 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:32:30 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:414d522b7454847f294a8c61536f57f36cb195df33ab1fce8c838de3d5ae109e`  
		Last Modified: Wed, 20 Apr 2022 04:38:18 GMT  
		Size: 55.1 MB (55063805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0618986ec147bd863b6a8cea7ee692a66f12d587dd47d451895ae7c0ab65baf`  
		Last Modified: Wed, 20 Apr 2022 04:41:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:8c94f4a4573b40f6e6aada86b8b76ae5ff6455c22160d6836ee0304de91af170
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56838738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07098a914f2561368939d23f9d2aa3af0ab3fb4cc7899c1cd9dcd6a1e0c8da8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:25 GMT
ADD file:a09b15a232ef12356f8a381e48ebbc75da16b46600e0cc9849189196595b48b3 in / 
# Tue, 29 Mar 2022 00:43:26 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:45:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0847c00642d4fc3cd086952d88bb1c62b35fc1592abb8bb98b5f2580cbdf5cc5`  
		Last Modified: Tue, 29 Mar 2022 00:51:53 GMT  
		Size: 56.8 MB (56838514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1909f39ed16ad9f78baad06fd192ab1aee614759874ec48ce0c8f2973d4a37`  
		Last Modified: Tue, 29 Mar 2022 00:55:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:85b7dca648ccc4eb71e265768da1f1fd2fb96752ce24ce7fd481f06567714da6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54453699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4301c00afbf7eb736c97acfc8c4e5ee32c9dbf6cbbfcc5a8a149a8991373530d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:45:15 GMT
ADD file:8f554d1fa0414c8c5592687851c7ff4646547038f7d464423b75f57ecade0e16 in / 
# Tue, 29 Mar 2022 07:45:20 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:49:36 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:024c5d1fff33205caaf39b2903eafbff594af3ca19d825c46db9f726a37cdcd1`  
		Last Modified: Tue, 29 Mar 2022 07:56:21 GMT  
		Size: 54.5 MB (54453471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cda226572e359177f0b24505d16e51c4eb6540796bb0b6465dcfe9f3ddf0d2d`  
		Last Modified: Tue, 29 Mar 2022 08:00:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:036d5995f0fe37456f1a835f7f84ec0f3df2d372b88f1b3d556adca4a44b7edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60217491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662cb550d87bb4bcab693949c91ac75748f26aa5c7ef2b31410beb467d928ade`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:04 GMT
ADD file:a3e83f143a1077db22a0c3474af3e1641c2c20856ea005f45b8cb6abc754cb26 in / 
# Tue, 29 Mar 2022 00:24:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:27:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:836a00544655c89c89efabf058adfe305cc708f5259ae1a48e4f895cb836a2b2`  
		Last Modified: Tue, 29 Mar 2022 00:37:55 GMT  
		Size: 60.2 MB (60217263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d135952d05ab8fce78c42c34b40a55fd5cb25572c58ef3c4c5bd84a060d9ec25`  
		Last Modified: Tue, 29 Mar 2022 00:41:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:58f0ab0654059d92993cbb7d48f309941d00bc661cabcad318204d91c859fe6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54056676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f810bfa8f6ac4e0d3cf63705077fd64f5f3ef948665c84c87c8ee337d8574a2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:06 GMT
ADD file:5143c5815a4282433726df7dd89926b3676994be1b8575d259b8fb48d6a6a4de in / 
# Tue, 29 Mar 2022 00:53:09 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:54:51 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c86b61bc0bc235576e3d7696ce7a1c21762146f539dc6eda8173ad30b9a4ad20`  
		Last Modified: Tue, 29 Mar 2022 01:16:39 GMT  
		Size: 54.1 MB (54056452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9df048f60ab1b9c1a3c05648e74da20cafa20ddeb40719aae6967c38d65ce7`  
		Last Modified: Tue, 29 Mar 2022 01:32:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
