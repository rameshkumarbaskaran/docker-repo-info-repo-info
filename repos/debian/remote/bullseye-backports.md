## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:71a87a5d3322200206cfbe67142c434ed61aa81b421f57e40f26966f8d7250ca
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:a0784fc79b9ff392d436efa587b5b9abf20bdb550c7c0dc030ce8e52038fa9bc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51359089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7b7e209a36959521854c135abace4f27dfbdd9356aa22d9c4f4442aa9b1d5b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:3f67740cbc1b7fefda4dc75bd2c0f0e76df9ae6b845f37b33cf8eea958403b6c in / 
# Sat, 28 Dec 2019 04:20:39 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:20:47 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3f64e5c246a10532414f3b69dcf620cbf27337d8900089f4139ab3215186e02f`  
		Last Modified: Sat, 28 Dec 2019 04:25:14 GMT  
		Size: 51.4 MB (51358861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7859e082556eddb038a9f635d0efc98e86a853808038507292a85830ae1307`  
		Last Modified: Sat, 28 Dec 2019 04:25:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2c03392889de06631507a66f8febe1537cc1e6eab03cc10463184d4e585f9c7b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49328307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682c9a15392d06229b9b9ba52ff7ab23d8212d1e57eff031f6adac6eb91fd30c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:48:50 GMT
ADD file:730d57bac91e32701978679d8ccfd9d70521397f6008ad321414c8d7ccefd937 in / 
# Sat, 28 Dec 2019 04:48:52 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:49:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a3c7b9678a433c6c2e10ed1e6dc96f81cfce99fe5f71bc8091965c137d50306d`  
		Last Modified: Sat, 28 Dec 2019 04:55:31 GMT  
		Size: 49.3 MB (49328079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46ab47804c8af4a25faea18cbdc0b82768b1d0b2f48385059db0947968db4a0`  
		Last Modified: Sat, 28 Dec 2019 04:55:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:debf8ce00aa29e57da0f6721c64dcf5c0333dcf7c0acca35b396c5f2b30433be
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47075550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3722084dd556d1e9efe7015d8a35fe2b56f742943399f084d3f39a00f2c6a8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:57:57 GMT
ADD file:ff4aac151f354dcf2159847b433d9631b254a18c30cb55390fe848c64ae989df in / 
# Sat, 28 Dec 2019 04:58:00 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:08 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aa5ecd1f9158499f6ccdafbcc35abc9cff760ff71453cf163442fd894809336a`  
		Last Modified: Sat, 28 Dec 2019 05:06:38 GMT  
		Size: 47.1 MB (47075322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639c5ced312f5fc1051f72c22380cba18b2738a911e642bcbbdae1bc1f495a5c`  
		Last Modified: Sat, 28 Dec 2019 05:06:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:335a8ab1f5eb977b1120c6540d208354312b76cb8b92eed7769e04f90965cbda
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50319545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1adb65cb9d8bb450a50a5b7c27300df6609951725165eeec96faf0b769e0e9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:59 GMT
ADD file:d8dee71c9b462c830ef0fea7e4ea281b8c8ee4f3a1e9e3252fae2401bc715637 in / 
# Sat, 28 Dec 2019 04:40:01 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:40:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9ddc6b7ca7922f46e5d77becb1dd9bdbfabf5d66b99008799facc91235201022`  
		Last Modified: Sat, 28 Dec 2019 04:46:03 GMT  
		Size: 50.3 MB (50319316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558d852c9700bca3a2f0daa1337d90dd990d892c11d38113380223fa753f7f4a`  
		Last Modified: Sat, 28 Dec 2019 04:46:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:79d2fd2d4bd504b3e85f03f1ad067f3b9858998d3b9517c01eabe917fba40629
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52628606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb25814ab643df1bb7f01a8803c4bb4100c96ff73aa6a25a7d557c548d849ba9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:38:51 GMT
ADD file:a874cf7afdd9718652025bc1f81fdb39341a41d8e4974c1271c6a60c38827dec in / 
# Sat, 01 Feb 2020 16:38:51 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 16:38:57 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eead0407ee66421148ca3913bacd0ce8efc8ec3454d91b093f8e0c7a840cd526`  
		Last Modified: Sat, 01 Feb 2020 16:43:40 GMT  
		Size: 52.6 MB (52628381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29341062c7ee4ea6ea7a8df142d6ea7be6c78816c3e04ad95e13fcb997952df1`  
		Last Modified: Sat, 01 Feb 2020 16:43:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:72c5ab35842b7d0d8ab79170da2d36706c1dd7593b9bb40105214cf1eff70469
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55181810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8a4aebe376a09b815a0db6f1260392aa750235260c1b22181235624ce6ddcd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:19:20 GMT
ADD file:b4f9e68f81c696fdc52ed16b3080552fa23e19fe66b8de9cb3ade042aac7115d in / 
# Sat, 28 Dec 2019 04:19:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:19:45 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0127e22d45eca52f3501e5b68ef14e0d3a7c0c031138b56d8f69924604af15b`  
		Last Modified: Sat, 28 Dec 2019 04:26:06 GMT  
		Size: 55.2 MB (55181582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd5877e16bee1b36f6756ef6acaac2536fee2642fcf537492d63bc7e73140ed`  
		Last Modified: Sat, 28 Dec 2019 04:26:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:a59eb7b88d4772b35f5f70a9f5dffabcdb453ac36bbb6e187379d2f4b09d2131
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50017882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8e45a7056061658209844c0f8458b2abf4f6c005179408ed5d7d068f577557`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:30 GMT
ADD file:ef81707ff6f9411444d40f7819b6103572f1c71599afd4c687f5262af6d30f7d in / 
# Sat, 28 Dec 2019 04:41:30 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:41:36 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6967537f6d685c8e7bce246638525934908340998b95e5baed55bd5e9805611f`  
		Last Modified: Sat, 28 Dec 2019 04:44:31 GMT  
		Size: 50.0 MB (50017657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420bfe26936725f7d255a59f0193de1f2ecafc9af3e1e3b7ce431e9a6cd6be16`  
		Last Modified: Sat, 28 Dec 2019 04:44:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
