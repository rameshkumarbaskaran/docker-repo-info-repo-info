## `debian:experimental-20220711`

```console
$ docker pull debian@sha256:6833073fba14eb926ab78fee9485413359733769cd263356e6f77036ff5f4b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20220711` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:81fd676af9929faaa800503d087b1a9eaae82ff048820ac853b761784af68e2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9135fc74e637077431fced62e66ababec5d338aea2167502a0a75fbccb8278`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:50 GMT
ADD file:1a940d88f62561651e40db55ea36a74594ec8b86da92a88afc099114961760be in / 
# Tue, 12 Jul 2022 00:42:51 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:43:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:53c4770665de01f88f5dc350b92ef44a1033377fe101fa00ca5bf012a1aad442`  
		Last Modified: Tue, 12 Jul 2022 00:50:12 GMT  
		Size: 52.3 MB (52331762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d292dd7ad4a0a24bf800c9a8a48c347ba4724f7cf05c95a2f579cfed96746a`  
		Last Modified: Tue, 12 Jul 2022 00:50:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220711` - linux; 386

```console
$ docker pull debian@sha256:ee517901fa6a6fd581bdf1eff3fcea9ddef0d8602a6cc51aec353b88c8e1a583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54207825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7b43623170770dcd956beeaa5555eef78b3b8d26afd39a07932db25c5b8573`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:45 GMT
ADD file:878426d87119dba8a22324e8c538357940c203ba90bc15912d0485b2267af353 in / 
# Tue, 12 Jul 2022 00:41:46 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:42:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:16053bd732f64321af8db68e64a8f71bd4687a00c0722bf8cd08a64a6576464a`  
		Last Modified: Tue, 12 Jul 2022 00:49:18 GMT  
		Size: 54.2 MB (54207605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7166d9c296c16421eaa66e6d6a8dca6975a387c20cda22e63ceb329ac35bf3`  
		Last Modified: Tue, 12 Jul 2022 00:49:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20220711` - linux; s390x

```console
$ docker pull debian@sha256:d1cc6bd803a00acadccec4f8ca720ee3f5be342c512a269f0db1a77c62cd0967
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51757607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1950c450da9d06262726b33ed9a00d21dfdddb046eeeb19a7fac82807a8d00b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:48:58 GMT
ADD file:ad15fe4787e44ec9dfda2d969c0adbbe98fa7cf5febddfd596b0e114a84ad120 in / 
# Tue, 12 Jul 2022 00:49:05 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:49:35 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:954d58d5c4ede279df1f24864d0cdbbb65d80c4803bf85a6c6ff55312899fbe7`  
		Last Modified: Tue, 12 Jul 2022 00:56:41 GMT  
		Size: 51.8 MB (51757385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808ceeca4a72efea3ac7ed35751f97654344af3f4058c9fafed2175952391f64`  
		Last Modified: Tue, 12 Jul 2022 00:57:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
