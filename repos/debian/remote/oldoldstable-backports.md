## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:fea9b303631c3e717c26d61ec61467d8c85b470757fc22455bcccadbf168554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:d43929862a6b6197a79b5bdfb2bee8941cfd32849abbda11ff5cdce974765f07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e121bfe7a091308cd46d8e1feffcdb8cabbc24b87b015f0c58fe308e3ea0baa4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:47 GMT
ADD file:52d0354275033e0baf3ccd9b09ec48b630ea7f260f85e8b3b7aae03a9fae9490 in / 
# Tue, 29 Mar 2022 00:22:48 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:22:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a217465aef5f702a24160a906fadc19e38184b0fb9a0c71a121fa062057d34fe`  
		Last Modified: Tue, 29 Mar 2022 00:28:21 GMT  
		Size: 45.4 MB (45427490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424cd805e915c42319b12f318b80d5658821700cf0715abacadacf023538dae1`  
		Last Modified: Tue, 29 Mar 2022 00:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8b672fb3f08c9894fca2dca74766e640f755cab5c99cad325d5c47317d36a6aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef62a95f892ba73060b932bdadb285ebc58bd8747311f88508e9655747087a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:52:02 GMT
ADD file:a302deb3de42bf0b0c92ef374751f46a79f8ea2918e158ec8a6402ca17a4e3c9 in / 
# Tue, 29 Mar 2022 00:52:03 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:16 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4c20269d57718c2c71bb6ec6d7a712b2cddeae105eb89540bf43cf9b7b4ba8e`  
		Last Modified: Tue, 29 Mar 2022 01:07:37 GMT  
		Size: 44.1 MB (44123271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4e4708c48fdafe109e05e200908fe22fc85060a541b37e23e309a3ca1eb3f0`  
		Last Modified: Tue, 29 Mar 2022 01:07:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cfc203f8bc53a6cecc4bc7426e83c6b91a6e10bdbc4d31794a3f27e7f778d624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfa5bfbe36fbd5377232b3fd7c736a64d082c89e0a9b25f3b8017069a829a91`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:32:35 GMT
ADD file:273df495cce49102768b41ba8f0c94ccbc7c53623b91b8a7e31ef0a344115c56 in / 
# Thu, 17 Mar 2022 09:32:36 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:32:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:82170f35defd7dea012acc55071774a608084a9c93f0970fab860ebff21f5f13`  
		Last Modified: Thu, 17 Mar 2022 09:48:42 GMT  
		Size: 42.2 MB (42151377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aae62e28bf90b414876f104cc744b5896c69d1bf5e6fbeb5eb48ad275407f02`  
		Last Modified: Thu, 17 Mar 2022 09:48:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:025cc23040dcc53b889576dc3c2caaee80ceccb4de540f1277e4ad70964bd27a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c8c5c94999fbc52e71c28852bc7090d9fd43377f2b97dc236433060ec19710`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:53 GMT
ADD file:760bfedd0748b7234303d78bd0279020d885897d940d2e7d9748cf80872d44f9 in / 
# Tue, 29 Mar 2022 00:43:54 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:43:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:03cf148030614354020199d11a7e26e1af1028c28519a968e8ea91ec666e2fb0`  
		Last Modified: Tue, 29 Mar 2022 00:51:21 GMT  
		Size: 43.2 MB (43212831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af5d0a30751cedcec751fb310f30ef2d5f50c0de456561ad29f0ceb5c17dce1`  
		Last Modified: Tue, 29 Mar 2022 00:51:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:bfd8997421c2d1902805e6fda5888914356aee117744a49c5ba9a1d918dcacf0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46147862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89d03d487c904a934ddd953271554dc817db1675d793523e8df8f9c76a46e5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:38 GMT
ADD file:05e88221a988a6885b305a946f9fe49ce1ea6907e20e9820ebf6e4c837070e32 in / 
# Tue, 29 Mar 2022 00:42:39 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:42:44 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:77db35bd510ef164400b38c4cf9b45fec17f35d16a8058a7cdb6d5326cee1f4a`  
		Last Modified: Tue, 29 Mar 2022 00:50:26 GMT  
		Size: 46.1 MB (46147634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dd151939d46b1ee76ecf06445f76829d6cf3808a5d4f399d1723d912c3597f`  
		Last Modified: Tue, 29 Mar 2022 00:50:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
