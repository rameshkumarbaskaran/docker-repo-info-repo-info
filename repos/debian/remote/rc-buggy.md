## `debian:rc-buggy`

```console
$ docker pull debian@sha256:3984a8bd37b594c9918ffc535eae0394387e1f92f2ba666c7004782186dcdcec
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:eaa8e10270cd01f9d20d204f56861f97139ee5820227f3fe01ef864c5549979e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51976439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18db9c29413932ffeb33d49f9e7327e2b1489103ae18d9ef34829230095435c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:25:32 GMT
ADD file:2496494632885054452c6f15317aaeace67145465fe0f719da9d3b5c95e6c8ed in / 
# Thu, 16 Apr 2020 03:25:32 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:29:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e4396830990ba6684412015e660aecabd027170dd4336124dd128865a6a81898`  
		Last Modified: Thu, 16 Apr 2020 03:33:46 GMT  
		Size: 52.0 MB (51976212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14448fc556731a66b3161afdf5526adb7f8d887fd588a6d5585f6aa08b9317f`  
		Last Modified: Thu, 16 Apr 2020 03:36:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:dcf26ec00ebaf3e582fd60b161f02ff14f43b0567a7c78fa1959adf5ab9f397c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49930977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749255c4e4e9d7b5f3ca5f1ab53657c6e663bec0e2ceb98943eded4f8164a9d6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:52:56 GMT
ADD file:bd1d9af70dc12dc4f17f2b7768c241504faf686b41fc7a690e618f93048fde8e in / 
# Thu, 16 Apr 2020 00:53:01 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 00:56:35 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c1a8f9f50766a877cfcad4d61e0db97b4f5cc37823b5af730a9b1e2a867d6410`  
		Last Modified: Thu, 16 Apr 2020 01:00:47 GMT  
		Size: 49.9 MB (49930750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5a08e0a72f6bfdffc513b2e2b6dd5ea3eb668ee7e77f1aac4d36c25dddd0fc`  
		Last Modified: Thu, 16 Apr 2020 01:04:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:5599b08fd45f8ffccdafd58c4e90254703ecb5e45f43c72d9568b7aca5f4eec8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47655645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6928af2aaccba746d4cdb4ec313eb495cee51e310ee81ff6c6428436fa803830`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:02:49 GMT
ADD file:5de6dfe62ae35545ab2dc195cdc7ed6211867d4583f721d08acfff371bc7cecd in / 
# Thu, 16 Apr 2020 01:02:51 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:07:12 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9d58ce8574bee4c2429ae80f47b2650443254f3f9a0dd9fc1c8d64277895520c`  
		Last Modified: Thu, 16 Apr 2020 01:11:11 GMT  
		Size: 47.7 MB (47655417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da7d91e5c1ec36b1ee0d05011506444062aca7d3c7dcdb1ce5e2087ecfd831e`  
		Last Modified: Thu, 16 Apr 2020 01:13:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2a46c5910c3679e374a6af8380b203a6399a47fa40f87ef8f15570a26db737a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9833de3e1ad8a6a77a1bdd762d7589d7d2b16eaad9e775eb943a5b65975a40`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:43:10 GMT
ADD file:ff8b5c2517d26b49a4c8114e515f5413a0c64b28ff1e5d3fa1bd70603aaadff6 in / 
# Thu, 16 Apr 2020 02:43:13 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:47:18 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2f361d4eae096128866baf55f9d19448df20331f319ad8df0f05397bfd2fe7fc`  
		Last Modified: Thu, 16 Apr 2020 02:49:55 GMT  
		Size: 50.9 MB (50910038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739460fdccfd5e56d180db795788aaa154e5e15a24bc61535c35dbe5d928e191`  
		Last Modified: Thu, 16 Apr 2020 02:52:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:08cdce11c288f76ce25493698b72b2e6d7f4f0c045f81a5e6d85119b97ff2724
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53130267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60989f9c1deb61067396eb902bbe729db47c557ddf2f146b4d85045552effeb4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:41:56 GMT
ADD file:af11f81927371cc0ed957aa36f4036c71c73a0b79ab27523cf0d49d8e0260041 in / 
# Thu, 16 Apr 2020 01:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:44:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1cf4ce40baf558f42709af03658907805f477c72b1b1a39869aef429cd35cd3c`  
		Last Modified: Thu, 16 Apr 2020 01:48:16 GMT  
		Size: 53.1 MB (53130042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfcd8282e43dbf1cea77e28bd5ad700b732bba316fba970acb53effe0f23774`  
		Last Modified: Thu, 16 Apr 2020 01:50:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:59a3e899e8b2328255dd29acff7e3d032b0cd9f440d1d33e4797102c5df37a89
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50691784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fb0c09103d43b150d2c8189b2e6275dc3205a57744ed78926fbcd87f7a3bb0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:31:58 GMT
ADD file:4c8da98109a760f1d6fe331f6b242401bd519a727c19c13f3f490f0bcb3158db in / 
# Thu, 16 Apr 2020 03:32:00 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:35:53 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6757dff0382d5411b1004ff5edeb85cdd1f3776f5d3176d7d12e44563a4577ab`  
		Last Modified: Thu, 16 Apr 2020 03:58:56 GMT  
		Size: 50.7 MB (50691556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d03655f4ec7dd6b0b1840c321cd4fbf7aba870a3c3cf99dded9e6d883c820ac`  
		Last Modified: Thu, 16 Apr 2020 04:05:25 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:67a66bf0b745f030a537eedc2d43aca5026f7001ba8935b4f77973ed28ec2738
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55860722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691c0f3a71b70cfbdf9507774b3f02ac3014d101a17161849a5be4505715eb69`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:40:28 GMT
ADD file:68afd6d0e23ee44127b8e1f922e1a6977efc12c46c7aa7afff807e146187d870 in / 
# Thu, 16 Apr 2020 01:40:38 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:47:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2b17b1afa1bd62e539e75bfdf0ac70297d76a76fc7df9fcbbc67ef6c31717636`  
		Last Modified: Thu, 16 Apr 2020 01:58:42 GMT  
		Size: 55.9 MB (55860496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471b39a9eaef3316ec47d72bc88b0ca7ac8cdb6ac7819b763b7ff74102c21fb6`  
		Last Modified: Thu, 16 Apr 2020 02:08:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:9aef58a1d00eb649e5bd82086947bf1911acc6269d87d3a0fff0ea294852db65
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50576768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0c5ea939294cf7e6b580171d09df588bb9ea7823890fc4ece66a1e14a7135`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:56 GMT
ADD file:1d96a73c9c03d31b0a60aa6b4e0215085afcdee6dc39954655798110c12c223f in / 
# Thu, 16 Apr 2020 00:42:59 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 00:45:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3633d30b569d7f8e4addec62b3bb5c460572eb82d6568a9bc40a9f189dc4bdcb`  
		Last Modified: Thu, 16 Apr 2020 00:47:02 GMT  
		Size: 50.6 MB (50576543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaca0a3bce5169f41f3ac3d87cd12d99b2642f25d43b674bf973ad8ff65ef79`  
		Last Modified: Thu, 16 Apr 2020 00:49:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
