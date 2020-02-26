## `debian:testing-backports`

```console
$ docker pull debian@sha256:13e2087349ec81d0a1b9aa7fc3bfd97920d2eea07f2c4475a3f253677da91c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:1d9ea76a0070f7cf106dba2b4b714008fb707b73353f3f079d8209071f5ae260
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51852930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d3d27c9a3c9fd7d1bc6e060b3a4358a6772b49a91530becd3ddcfe5a141825`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:54 GMT
ADD file:bf9b71c3da178fa1ba282c110853082e94e9f8a90773b43b6104bdb8c9e54f5a in / 
# Wed, 26 Feb 2020 00:41:54 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:42:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1fcd5305bc72cb154c6bf3d1a204b8bcfc0d91d4811e6681dd2b7aafdaaa8669`  
		Last Modified: Wed, 26 Feb 2020 00:47:41 GMT  
		Size: 51.9 MB (51852708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd67e7a6834b1a54301feed22e9d193d7055644b9de4baa8e488285971ce3cb9`  
		Last Modified: Wed, 26 Feb 2020 00:47:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:89ec27d5bd9a255fe69b00037ad1ea0b980b730e370de6d5dcc3ed3f5aef6292
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49485275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c4317167a5ca9a56433f9bf01e7c6387e6e4b590bc7a870ecf84c985aef05`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:54:14 GMT
ADD file:ae8ba1ca1afba05a5c2e742b53e5327fc31461ce3ba6cc1d842a85616599336d in / 
# Sat, 01 Feb 2020 16:54:16 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:54:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91026fcd0d4f9301275f1dcdd3aa8601af59bbd3c9b5c0d12fbf33a12b62c736`  
		Last Modified: Sat, 01 Feb 2020 17:01:26 GMT  
		Size: 49.5 MB (49485050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0645e3f1abf50c1a6b7a43afdaec99fd3a9c3ce15ccae504d6c954071e7c4b59`  
		Last Modified: Sat, 01 Feb 2020 17:01:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d67c6774c0dad6509641599ca15536ed5ef18a132ed832d3e7340989e81f93e5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47233952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de77ecae80b2c92c47858bf833fa9c3a4a1bc30f0f6bb328b4a575c8ed8c6c09`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:48 GMT
ADD file:dfc2213b46d6288c8ba30547b950ae299bfc0c436f2e8a8d3f6376e91bb05256 in / 
# Sat, 01 Feb 2020 17:04:50 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:04:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fe08c30a3140b22ac1acabc19c0e5e86ef978758eba0be5489e35746bd43f3d9`  
		Last Modified: Sat, 01 Feb 2020 17:11:51 GMT  
		Size: 47.2 MB (47233726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98064400c58c98947e8ed18501e6eadc7b2fd49cc0eabe1a165f6e027e21634`  
		Last Modified: Sat, 01 Feb 2020 17:12:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:43c707699bf04cde0747f2dfc649cc80d5201419cfe4293e32740e3003962a08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50453225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e698da5eeaa6bf0847c016cb252fbfbcc1865692fccb31d43ec07f785807e2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:35 GMT
ADD file:db821559bc10f9e72e5927bea485644dbba15b9be5d035d29e74ff74c90eaebc in / 
# Sat, 01 Feb 2020 16:43:37 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:43:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a8ea3b8ec391d7f13575570e7881031715ff8ef67e1224726395e166f3c9ea7`  
		Last Modified: Sat, 01 Feb 2020 16:49:35 GMT  
		Size: 50.5 MB (50453000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e95db6fc964d7cd9655bb1e41e35c3bc4f86f811a7a12d9d056f508300e6e0`  
		Last Modified: Sat, 01 Feb 2020 16:49:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:963d14545f88d4a69659eb062df1e4d52643f802c373ac4b35c9acff94275036
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53002939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77a260fd035fca570df79e3184d44ecde389e00b9e2637b2b1d1abf8823e3a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:35:59 GMT
ADD file:9a37eb812440af2fa6bb9b53caf4fcbba9d6c709edc69f1fe2b2f47195abee7f in / 
# Wed, 26 Feb 2020 00:35:59 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:36:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:713e3f76a9b5faa14362eec3ae0c403aeb49a616a1003367b73392ff5eb46faf`  
		Last Modified: Wed, 26 Feb 2020 00:42:22 GMT  
		Size: 53.0 MB (53002719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c41cdc9c7e1e576985a4ee3a6265f916416bdc3f4c99d1bf6209af849b3a5`  
		Last Modified: Wed, 26 Feb 2020 00:42:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:908cd401bc546273c622187bedf03aaebd6ddd1403b15a1548bb829f45c6063e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55316543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ebcf543e1c15b7dbc4ac0ebbe4e043ec2682a1e0211922c69f019341c81189`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:21:17 GMT
ADD file:51c285746d844fee079ad0e2a25ef1f75e4c1bfcdf0f42f42342c83505723548 in / 
# Sat, 01 Feb 2020 17:21:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:21:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ca90af24fd5c34f627715eb0513e46e570af7b73a18c9254dbe592577f983ba`  
		Last Modified: Sat, 01 Feb 2020 17:31:53 GMT  
		Size: 55.3 MB (55316318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c10eb8397d055439b6bd2b4772dd63757ee122f43be5c4f408e387561b804`  
		Last Modified: Sat, 01 Feb 2020 17:32:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:a7ef9bd73a1cb632a57b78b736933c84168c26ff7af96c82855ce049e3baa2fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3c20edae68cc23f20e6f86f4412d6b3816abd1ebff400402cf1cfdb0bb1a2a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:45:12 GMT
ADD file:35c9c67c243d6ee981113893297c9f91610abc3f4f8fc695e712d1bf5e7991c1 in / 
# Wed, 26 Feb 2020 00:45:21 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:45:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aa3ec75d7f3cf53cae07836c22db68711638d2fbdb74aea08833d90eb47e6f75`  
		Last Modified: Wed, 26 Feb 2020 00:49:36 GMT  
		Size: 50.5 MB (50483673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cf34b0fbb8c89aaa6bf692b2458ecf1ea138a2b2c57c4deb710d98a1f9e3ce`  
		Last Modified: Wed, 26 Feb 2020 00:49:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
