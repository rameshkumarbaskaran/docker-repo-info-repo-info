## `debian:stretch-backports`

```console
$ docker pull debian@sha256:ec42feb6ca63049c200e6634444cd70242b9b8b4b5d059be93676503965bab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:c35a5937a4fa6d7a8d44c8f8b11740aa72e05dcfcbc9d544c4e0e5665c6a741c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45379876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69f5f0f46ba80a182d0518d0a41e569da25b19dd8cdde6641a44d4e88e271d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:41 GMT
ADD file:084c8b3d38d578aa3910f3786b67b058962dbfdfd4a49d6e0201f2e91670873b in / 
# Tue, 12 Oct 2021 01:22:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:22:45 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2f0ef4316716c8b8925ba3665932f8bf2cef3b072d82de1aeb269d6b8b61b84c`  
		Last Modified: Tue, 12 Oct 2021 01:29:27 GMT  
		Size: 45.4 MB (45379651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662ad9244d2f850a79beccfd1fdf3ff1bb3f42b8be81321be606afbc8c35d15`  
		Last Modified: Tue, 12 Oct 2021 01:29:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1d099ae172650b017f420eb12be11288219c4d564b2f47a717df8b6e045d900b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70ebe5186a5a6e64d9dbea6a6aa35b76a4a1ad09e01a1cf33ed5c7eacdf0db7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:55:37 GMT
ADD file:eb65cc31f82e76c4ea5a8f21e4cad1372399517ee41a759740ff91d1d23b9e44 in / 
# Tue, 12 Oct 2021 00:55:38 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:55:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2f67fd5897d122073fc9ad347c1fb9faec31555c47b3ee6ff64ca2b553034ed`  
		Last Modified: Tue, 12 Oct 2021 01:13:31 GMT  
		Size: 44.1 MB (44091932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f43c270837fe20d1e49d63cf41a173e30c15fb5c4746779b9123416dbf09fef`  
		Last Modified: Tue, 12 Oct 2021 01:13:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:686113d851c9d39fcb0db5c2a7dcb52aba5edbbfc7b75a4236ccc114def1c692
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42119648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a5220b1a4c819d5fd592a824051615ae562537edcccb71692bce03d04015fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:07 GMT
ADD file:eb5955ccd54a486767e85aeb1c03ffc6d8667b5476d0cf17b892ca407f1c8853 in / 
# Tue, 12 Oct 2021 01:34:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:34:23 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e9db3616ec4491d75e6c28254ff2376f24900797e7c4cc464f36a0c502b111f`  
		Last Modified: Tue, 12 Oct 2021 01:51:20 GMT  
		Size: 42.1 MB (42119423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebb32228f3f8b248d3f58e4e383e8be69cc128322f049c40a635ce5e5daf964`  
		Last Modified: Tue, 12 Oct 2021 01:51:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1e101fcbcec8666a214cdc2209c5ac4debb03512e352f9ad9b8173fedebe2eeb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43176920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22611f3a72b517527aba51e21ea8290353ac16ca953986a081584566177b108`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:16 GMT
ADD file:33c2886dff8a69edd550eb69499bf01658d58e2eff405d4b5d4cd5d5be535faa in / 
# Tue, 12 Oct 2021 01:43:16 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:43:22 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd2a530f50c2591d61de58d0e9cf724f6c5a2e1112456f38562e289732464c0c`  
		Last Modified: Tue, 12 Oct 2021 01:52:05 GMT  
		Size: 43.2 MB (43176697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658cf5076d7bc6461714d5f9258cf0c5f5fc2c1b6cce9569b8c0d50234792789`  
		Last Modified: Tue, 12 Oct 2021 01:52:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:44e38d9e14af0799348138b3247afcf774782ee6c3ad832b64ff564cdc9f72d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33807633aefce93cbfef044203994c10de859717557b4b1ed247eaf4b645a575`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:42:19 GMT
ADD file:5a6f08cc731f24357c3702231256fb05eb0a97733779b2ace406ba3c9bf64baa in / 
# Tue, 12 Oct 2021 01:42:19 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:42:26 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2ef4e90cca7406b4907a34e3571153fc56e3ecc9b2b5fdbb7787f22877cfec5`  
		Last Modified: Tue, 12 Oct 2021 01:51:58 GMT  
		Size: 46.1 MB (46097164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71bcbb0d3021d47e1af8a7d9a478e4045b72d0efc0109f3ddb4047dfda10869`  
		Last Modified: Tue, 12 Oct 2021 01:52:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
