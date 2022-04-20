## `debian:buster-backports`

```console
$ docker pull debian@sha256:8ca8661ab0e852f8a4ddcc74d4e9d6fa4bb543f0277cde4871ad467dff6ab380
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:aa99e15dabc88c67375a5bcd4b0b330678a97fadf536a804ed886f481786c096
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6737e6e3305c6605f023abed0975cb0abcceb5c222ed50e51d386abd1333ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:43:40 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bd587522a21952ca26470113c848c07d020fa048297162069cacfcc13d431`  
		Last Modified: Wed, 20 Apr 2022 04:49:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:16abc31ed326e496142e224df22113b00bcff7e47018b374e41e212db6f1797c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48158518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cdb69b067780a76b9ff0faaab853198c5ab3628c5224d497023c66d217391c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:04 GMT
ADD file:e7d31ee8f990df96d5922feb35173a364a0832e8fce2d32fd4e703aa3b66e1b2 in / 
# Tue, 29 Mar 2022 00:51:05 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:51:19 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0bbc2517bf9c8d842997ba8f85b59bfd92c5bb6bba79c39047eecda859dcae27`  
		Last Modified: Tue, 29 Mar 2022 01:06:08 GMT  
		Size: 48.2 MB (48158294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8553322fe47c91c358b468dbd0a3044575f748084ac4494eb8424c9f459589a9`  
		Last Modified: Tue, 29 Mar 2022 01:06:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9d6ae33115da8255d188a4a89f13bb7f382b6a3a855658f34df195d834494d42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45914755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74815f2d1be3573d54846109729b2f328d0e8369fcc7dd590d0f80417f1f809a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:04 GMT
ADD file:60a690e302d164c569e6f3fc29adb6686618bb728249405f90960835525b0599 in / 
# Tue, 29 Mar 2022 02:19:06 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:19:21 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0cc72482f2e040b686190f2967010d45947924353440070552a298b9f9f81b19`  
		Last Modified: Tue, 29 Mar 2022 02:34:54 GMT  
		Size: 45.9 MB (45914531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39defb05ffe267d0f557d4480f2cd810605f297261e0c3b3decb998d605f040`  
		Last Modified: Tue, 29 Mar 2022 02:35:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c221b609f44c706d88518d5afa4e25b2a389688cb437b9d52c1f373caabdb57c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49227960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae36706ec6d034436705f6490f83278531fc593c23eb4025103249c71660daf7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:29:29 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcf61c50bc20ce89acc6da83284c168f8a27dee2f04757a4d43ec7785f79daf`  
		Last Modified: Wed, 20 Apr 2022 04:36:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:3a5ab1d258b639d2405fe8963dad466e5dd0c7f819d12d7e8493664ad02d1847
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a7384c06446a52efdf2c2480bfd86bde7edaa9206294b19a61b0815e9e7de6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:12 GMT
ADD file:fb2c1bf394c39b5bf948ceaa00317518326bd846b3f6802dc39cfb7fcf404c69 in / 
# Tue, 29 Mar 2022 00:42:13 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:42:19 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b86fabf064e35595b9c8543deb0dba50a95e438387a9877ebfe189bbfce3c87b`  
		Last Modified: Tue, 29 Mar 2022 00:49:34 GMT  
		Size: 51.2 MB (51206670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfe23327dd5caba42a116df14bd4ea3760634b9a61bd595abff1f871e49f555`  
		Last Modified: Tue, 29 Mar 2022 00:49:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6d9d53e320307d3695a9a9786ddd4d6f323043acfeb826bf4c8580787bf56eba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49080115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3276a86430777e37c247fbde5dd561abadf31fbb98998459cbefb1c63399b75`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:43:01 GMT
ADD file:c86010b52f782f910842586e6abc81e64c7a659d001b89799314a59f4fb96573 in / 
# Tue, 29 Mar 2022 07:43:06 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:43:17 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e0bee9c4b9257c0ad7469830be5e890536feef4e8ffe6c2613b7e8be7e060f6`  
		Last Modified: Tue, 29 Mar 2022 07:53:41 GMT  
		Size: 49.1 MB (49079891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07dc846abd481122a2d53a26eefcb104fddd2751120eede429890fc1b83bfa0`  
		Last Modified: Tue, 29 Mar 2022 07:53:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5fd45bd659da9d3e5b8897d81fdf4b3a0f11017c01f392052dbd302ba6630b25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54094003436e79a10f102ff59d8c6291f07ea35eac8eb781d13a2068fc69daeb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:25 GMT
ADD file:a600709d679cffd058d04ba0eb0765cc870766fd5de083ada0eeccfd7afc21f8 in / 
# Tue, 29 Mar 2022 00:22:30 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:22:41 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb53bdc4c2c6ececbd424b1c643b9877934a5297a5d2db0eca1a175d7a21d32e`  
		Last Modified: Tue, 29 Mar 2022 00:33:53 GMT  
		Size: 54.2 MB (54183100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37331d5f6a5c9bab113bc51c20b3552f60051400199d23f089144d899945a13a`  
		Last Modified: Tue, 29 Mar 2022 00:34:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:ffc315a2d4d6ddcf44f3745dedfeb9ba71833cd559cf0b7981239424c14fb056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668bff84c384e478dda3ce20530a8bf0b7678cf2f1388bab7bcbec17253d4342`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:52:09 GMT
ADD file:784894d175880656ac82b485076fb224bde46d379dd634720acf7acd5eee9365 in / 
# Tue, 29 Mar 2022 00:52:11 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:19 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e3cc532be5698da8ac6589c11495b960fec83fd52aa82617e3218678ff4546d1`  
		Last Modified: Tue, 29 Mar 2022 01:07:20 GMT  
		Size: 49.0 MB (49007755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5250cfe615d62a1c3259121f77ba2c411b2c2c253d29df51feb4b5e171c02779`  
		Last Modified: Tue, 29 Mar 2022 01:09:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
