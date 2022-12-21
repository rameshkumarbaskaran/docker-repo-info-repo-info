## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:efb94247be8c74230a65fe8dd8b52c125d367609212f46df84218ec48f618c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:0b9eae254f0260b41445b1eef4e0007acadceeb754764bd72cda816aa5745480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b690b953983462eb2f35ddc27c5a60aff34878c46377d16ebdbf7408e6f157`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:21:01 GMT
ADD file:1bea2b449a4ce132efd49fc55676c9345122a3e6bf2fd8d222973421e97cd543 in / 
# Wed, 21 Dec 2022 01:21:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:21:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c345612f93e3101d36e5006b7f417ee9fb655c3fc10e30726108dcebc0b9c0d`  
		Last Modified: Wed, 21 Dec 2022 01:25:36 GMT  
		Size: 50.4 MB (50448879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc204c1ab4ce867ef76c493801ea75a00b95d5990d37f9a6217429ba64d17eb`  
		Last Modified: Wed, 21 Dec 2022 01:25:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c29bb79da4c76639f1b118763f24bf816ce9d7d692994cbac50717b5e5473098
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcc27f830af2b9d3aa69579cfeff5095c5749ce443734d90ae258b8c0e17d19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:59:03 GMT
ADD file:670ca80d5b8d1c8ab5dbfe37fcfb4cd28df09c9ceaf2179cb29208e4bf101010 in / 
# Wed, 21 Dec 2022 01:59:04 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:59:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9033e9146b3cce0177082213ca1e89bdca91ba3e423a9f93907f1b240bb8771e`  
		Last Modified: Wed, 21 Dec 2022 02:06:27 GMT  
		Size: 45.9 MB (45915615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4579800021deba21255f86cccb8c86353416ad00ca51bd2da5525861ea2e9c9`  
		Last Modified: Wed, 21 Dec 2022 02:06:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:79fe3cd5a34ad5035005c6e45eafb375702e3475e0d392c84c3da3688cb079ce
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49234021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d47ff0df6694d7fa55df756b3f945e3cb7efa4709a4b2e5bad82bcd54f8b2a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:08 GMT
ADD file:6ffc6c9e38b7b5a000e988c062d6a9d546cfc457d983bfd819634f0d402485ab in / 
# Wed, 21 Dec 2022 01:40:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:40:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:348e6bd6ec9ff182c52e76cc70eb4cff6396fc0fbad3b7ac6122057770f70094`  
		Last Modified: Wed, 21 Dec 2022 01:44:09 GMT  
		Size: 49.2 MB (49233796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e805d8c0ba303803d77cc77691e312b4c118bec63f1f8623e74270a062a99be`  
		Last Modified: Wed, 21 Dec 2022 01:44:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5821cd12ad8870c9528993868c23fa074493dad074d8e5fdc1ba328001f266ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0a7068f816adf744210a3ab573711bca31457441d1ee2c4e0f4232da26ace5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:56 GMT
ADD file:264487fddadb6e53d2a6c99dd6b0e860a815de8a7bd9e22b423dde12150ec271 in / 
# Wed, 21 Dec 2022 01:39:56 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:40:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d28244ab76f1bbf07de6120a036af5f721ecac517a3dab5a2395d9d25f2fe6fc`  
		Last Modified: Wed, 21 Dec 2022 01:45:59 GMT  
		Size: 51.2 MB (51207743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9aa19f17aa8d8f87c91fd1ecd82a9b34c264d449994db4d7fdc8e978d3011f`  
		Last Modified: Wed, 21 Dec 2022 01:46:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
