## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:c2b194338df93a7c56f5734415a1affd7497c92aa81adb92db0fabd7e8a47f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2bf3569eece4adff200b7b5c4a04db91caefe6835bc7c71d7cc6cea0fd44a55d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ab00a15b108d6451b5f8d546dd1375f34f4c7068b145e7dc22afb3aab8f468`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:43 GMT
ADD file:9a5f9d2fbf4e8ff77289cde86e300dd0874dc73356d69ea45519a99f009e99dc in / 
# Wed, 01 Nov 2023 00:21:44 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:21:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d32eed0415310f14276202887b8e6edc2ea9dada5fd5f1c0584d59040bb20eec`  
		Last Modified: Wed, 01 Nov 2023 00:27:16 GMT  
		Size: 50.5 MB (50499127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6608e23ca6d71ba0644db02b975f47921f00478fa335151e11ae0e5ee3182262`  
		Last Modified: Wed, 01 Nov 2023 00:27:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f9cf5df20392586689e5f15975648b0e23316926aa8a5a0e3ec61931ef5b2ad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcca76429faf453761704f233431fdb2bca68bb8089b52ea6dd627feb43eb144`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:38 GMT
ADD file:17de67415e1e99e7c354ded5afe9201605fc14f99758063ce4cb90518a22d6d0 in / 
# Wed, 01 Nov 2023 00:58:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:58:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5bdb77f923bf70bea8be1016fd4aa1eb54657ee9b8ec2297f3e8609f103159e4`  
		Last Modified: Wed, 01 Nov 2023 01:04:04 GMT  
		Size: 46.0 MB (45966071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cca7d4b5099141bea486c1c9a27e98bf946cae05f90ea7b68a03ad7dce46b83`  
		Last Modified: Wed, 01 Nov 2023 01:04:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7cfc6ffccdb0b1035f209ccd43df5bddddb6572ef76ab0add3e8ba7c7a149706
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6435d18ad66707d003e6c2207a40453ae0e8bcbbbb9fc1e241d05090f1f0f6fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:16 GMT
ADD file:067322df328f58025784b9686a4644e51c8f916021db33c8d3c1ca825d08a7ba in / 
# Wed, 01 Nov 2023 00:40:17 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8b24c39ded2c8ab2a51da2d9f95c90b25bc2f243c3967c3abb056d2ab71f1f8b`  
		Last Modified: Wed, 01 Nov 2023 00:44:43 GMT  
		Size: 49.3 MB (49291089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297f107a08a0a3122e166ad996c5f258afbeb11e37e9cae95ce84dff8d4489c`  
		Last Modified: Wed, 01 Nov 2023 00:44:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:f619b1b7c1be6c880e78fee696f46fb55229922b3c1247314eb9212a97a402e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7fb20d1b90d9e19108253cbd145a1d4b34db3a94fea0a28687075a0c9b95cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:50 GMT
ADD file:719e8e1adb350076d6d94cf4a9d9aee4cbf29a10d35bde7ba859b36d199e21e9 in / 
# Wed, 01 Nov 2023 00:39:50 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:39:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad734a3f4acc2a601edd93b5e1694b2a9a95a6d35b970ceedeac80dbdd08dd89`  
		Last Modified: Wed, 01 Nov 2023 00:45:22 GMT  
		Size: 51.3 MB (51255728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0e861861ff69b292be15e8aaa6f778b2b8a7272e3c71029751ed3f574bd705`  
		Last Modified: Wed, 01 Nov 2023 00:45:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
