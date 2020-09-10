## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:518e1a32206260edb621d5ab6c4882059d12b98719145142bc7434007b5900c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:56b98d5e7042bd5e63bb0b9b92ec40e459cc2c78e97a39c2df403a35b25269ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45366992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e595da487bba44d8b1a2b36be10b7b530e1d041bfc34c3682fb4b626585143`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:26:56 GMT
ADD file:4214b144f02c0ad7503157ab5b61b68e31920aef3671aa3ac95ff2f3038c0290 in / 
# Thu, 10 Sep 2020 00:26:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:27:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c36d0b8b3f4fa6af0d33862d77b8d5e7f5f0c19c3927b7f2a45fd3ace66b4c75`  
		Last Modified: Thu, 10 Sep 2020 00:35:26 GMT  
		Size: 45.4 MB (45366765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea86d66cc04a929824854474797ad9f862d41dcbc4cbb586a0af2cd100b29fd`  
		Last Modified: Thu, 10 Sep 2020 00:35:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8c5ea2e3f7df81bd6f6f3f4dd46b51a441e4a542a75935163f8842648c90e119
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44081543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4f37af6a66ee596521a43c4c60cbcb48ad779b7ef873cce6d078303b425439`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:55:49 GMT
ADD file:93bb3eb3e53a244029b7ba6a67213be7ac3f4da1dcaa235823142712bf3d234c in / 
# Wed, 09 Sep 2020 23:55:51 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:56:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:75566b2708f281f0ce78cc6be89345d6eb808e7b6f27b28b0c1d99c0897bf691`  
		Last Modified: Thu, 10 Sep 2020 00:04:36 GMT  
		Size: 44.1 MB (44081315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1420a76315279011f0f29cd7f53b0e8ae65fe5372d66dd56d388d58f8116359b`  
		Last Modified: Thu, 10 Sep 2020 00:04:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f3392f24ba59786ab51d73f617719a2fef1e87ddff2cce79c0c269380b20cda9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42111654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bf35e40fa50eb83bff987cb8764c28e1947ffb05df9ffb76dc64cdeb425558`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:10:26 GMT
ADD file:080bf4a61af9edea3014896af2f594a3a01595d3fad22cc4396722e5e1e81a72 in / 
# Thu, 10 Sep 2020 00:10:29 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:10:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0a3d7c65b55a7c1d1ee5254b50b11fd6c11b6619d760c12ac0854d5d5d32b85`  
		Last Modified: Thu, 10 Sep 2020 00:19:27 GMT  
		Size: 42.1 MB (42111426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735049b0b161b2663f7ad175b1b8194b47d0258aabeff5da6d702e9ee596266f`  
		Last Modified: Thu, 10 Sep 2020 00:19:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:868ba9cbdcfadfefb1c3faa0d2b48e0b2f267b64065ef72a19b9983d0fe224fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43171911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7558063c9c1f1ea6472cb23e7512ef15c316e1b6c672991cdb8babdbc7f64e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:51:20 GMT
ADD file:fa033e6d5014b93ba73e6088beb0f7a6e48a610b0be71847e4670d5f2ae0eeb3 in / 
# Wed, 09 Sep 2020 23:51:22 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:51:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d57b20e7774200f0d9f70ba7b8c3df90dc87948fdfe1f18e1d668baa02451e1e`  
		Last Modified: Wed, 09 Sep 2020 23:59:29 GMT  
		Size: 43.2 MB (43171684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904a491213ebeaf21f3f0b757994409f5c2d224408a3fb61cf9f682a1fa759de`  
		Last Modified: Wed, 09 Sep 2020 23:59:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:64efdf2874a1fddb98f53fab776acd563185ee21648146369bff93f2d8a22084
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46086994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c393c7fc5756b000b8b102c747e47da39593b84a7390c5bf6a70490607d6e062`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:41:44 GMT
ADD file:b045bcb8bf3e5b24c5ca4e82ed73ae670fb72405069cde9cb4163912e9b641d4 in / 
# Wed, 09 Sep 2020 23:41:44 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:41:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b226091edde2a0422758105948e9861e61c157aa0d8ada24405269c8693d2f1c`  
		Last Modified: Wed, 09 Sep 2020 23:47:41 GMT  
		Size: 46.1 MB (46086769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972dfbb9cc92b93d7b689316f19da2148d37189e7dad0bfe8f646ef46f87af6`  
		Last Modified: Wed, 09 Sep 2020 23:47:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
