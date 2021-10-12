## `debian:stable-backports`

```console
$ docker pull debian@sha256:188b9834d350fe721985e5d2b688d4f6501cf969e3abbd7debf743fa378df05b
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3572883be4989594ccc7737690dcd8d6bba9f216624eb6b648df88e1b878e3e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54917768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23781c8e12e1ea8e99519ca57dccd36b12af9ad1b22a1e22c346ce72205454d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:19 GMT
ADD file:5b20fa1d06a2543173c0349037f3cc0daf6865433bd0078294f56a1ad74eab99 in / 
# Tue, 12 Oct 2021 01:22:19 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:22:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:55cb80d281932941c15ecf1f22a0a0d3aeaf0cd54b119a2c866dc63f1a19d34b`  
		Last Modified: Tue, 12 Oct 2021 01:28:51 GMT  
		Size: 54.9 MB (54917542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426cff2beeb71a8c45114968349c6bd5120ae688450ed98175ac73964c5ea2c8`  
		Last Modified: Tue, 12 Oct 2021 01:29:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8411f1b98fab95365868dddedc49f257d8bd34f8cfd09de362fb07008e198874
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52452469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335d4735d05973b97cf063a64d828fead3f89a833b3259afd28f36f3265cebbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:54:40 GMT
ADD file:cf95c47a44c6429c9b78a21a77a25de617d7044ceac8f34076e0e4fda02a1d9a in / 
# Tue, 12 Oct 2021 00:54:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:54:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cafc721d7e171ea8a3201aee9d49e7706edf5e50c628667efd8de159f25a2be5`  
		Last Modified: Tue, 12 Oct 2021 01:12:13 GMT  
		Size: 52.5 MB (52452247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66dd91a34f1246a22d3d26701d91d8ee7141d8d53ee27146fe37c64e149e748`  
		Last Modified: Tue, 12 Oct 2021 01:12:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:af18ebd8fc6a3da1c9ade8a3f05be8ba7643840480ae0b255a6b6ab3503ad492
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50118886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4633dda5ca89d26db462165084ad1299493a0d6912c7282d5c5f138690e8d105`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:33:06 GMT
ADD file:49cf5edfc79e4e3ee46774cffd5252769c7920d2dc27fa3913bad6687620d64c in / 
# Tue, 12 Oct 2021 01:33:07 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:33:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:440069d8324183357e1261418d3a9a960b29f433ad2a633e70d73a72fef163a8`  
		Last Modified: Tue, 12 Oct 2021 01:50:11 GMT  
		Size: 50.1 MB (50118660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c8e8a191ba872b26eed97b664e9be91b114a1cca80f1397f8836caa3d81de`  
		Last Modified: Tue, 12 Oct 2021 01:50:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0c19b0a2e053c6e4abaf059483c30fbbba7c2bc12198b2ce94d0cb24bf9d1c03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53603219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5409ac2454f89fc067771e71d15bfd83fe7ba9802bf760f6888088b14aca980`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:42:54 GMT
ADD file:804ef9b2fc9c5b697d59a7a917482886a55807bbd36490892c70b3b629517d5b in / 
# Tue, 12 Oct 2021 01:42:54 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:42:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea317fc754dd760ba835f4b130dfe44ad680eb7b1fa5e5a46c133b48946f0dff`  
		Last Modified: Tue, 12 Oct 2021 01:51:25 GMT  
		Size: 53.6 MB (53602996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d0027defdc8ae6475a265cbe6d65920cbdb99bcd1c4d3b5d6dcf55ebcd2799`  
		Last Modified: Tue, 12 Oct 2021 01:51:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:dd72ccd21610dc89eed62726fa0b0574b66c0f7f28ea62045f77822c786b6e38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55923640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6478a10e09e58eb4f314f09b57f0c35acc1dc42911c28ee342d50a5a82fd73`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:51 GMT
ADD file:24d67f7b5641ca3ed5b97d965f8ce4f5f4c0387342825f51e77004fbd64dc739 in / 
# Tue, 12 Oct 2021 01:41:51 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:41:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6dc2525540e90f643ce691e74944f7fb377c97243f1d150666146756bba0ec27`  
		Last Modified: Tue, 12 Oct 2021 01:51:13 GMT  
		Size: 55.9 MB (55923414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9bc894e964fd63a277f3371167b7bb8f5dbb8679a12863e2afd665131f1b0`  
		Last Modified: Tue, 12 Oct 2021 01:51:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e575729f9c56135dd9fa0ffcc393f8c6f84a57635a8ba5d3099c15c1062c159b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53170037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b584bb19c57defea2c77e3b442be778bbdeaac41453d020adaa31521c4d03d83`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:14:15 GMT
ADD file:0e49a2741eab1dd61adf85a42a5f7b1e7b8a801d17e5925ce71a962dd9436843 in / 
# Tue, 12 Oct 2021 01:14:16 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:14:24 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c643a33bbcb2443773c1a3a92228130d1cc6d19d74fe3ed68787c4024751ff66`  
		Last Modified: Tue, 12 Oct 2021 01:24:52 GMT  
		Size: 53.2 MB (53169812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1482b2dc356490d54837ff1a99d9b0fe904f804192af6cb7b49c315ea681d137`  
		Last Modified: Tue, 12 Oct 2021 01:25:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f9d1a613941ab711d46f651e2bdff5dfb03990319e2862f183b23d7f0be49d02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58809102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2cc8c6a11ac4da588195f52aec612546ecebdf7035b94a4af27f1cd2a3a5d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:41 GMT
ADD file:50a64f2cbd267a73c297febc1aac2d0a0ff0966d105e37c199477a326aa29e76 in / 
# Tue, 12 Oct 2021 01:28:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:29:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2a063c91861196790fc45eaacac95fcbb278654c161c3397bc453aafb71bc96`  
		Last Modified: Tue, 12 Oct 2021 01:42:23 GMT  
		Size: 58.8 MB (58808876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eddd7aa238ee81fabbae668fbfcc0a525fba6c00d486f0d622a00a6347a06a`  
		Last Modified: Tue, 12 Oct 2021 01:42:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:b0970adb961d3c3c3ee3809bd8fc25e8939d8bde9b683ad3dbd4261df76fa550
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53193109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8e2621d2336c802aedaefa842c5219cbf7ef7df1eee5e8664ded72053c7beb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:43:57 GMT
ADD file:edc453c86c89f128b79c20c971b4b63e822f652a01b62cba93042f5ab3a41c22 in / 
# Tue, 12 Oct 2021 00:44:00 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:44:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2f41532c0354f964b59239357dc1211cd22974215e0e805b74bb664ecd5eb1de`  
		Last Modified: Tue, 12 Oct 2021 00:49:54 GMT  
		Size: 53.2 MB (53192883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef84eea5d79a082c54dc169326ce1c393691cdedc56c0c304ce7fa1e6a96cc`  
		Last Modified: Tue, 12 Oct 2021 00:50:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
