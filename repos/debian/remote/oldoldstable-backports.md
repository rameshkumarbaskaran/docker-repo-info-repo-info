## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:608eec6a8267663f290e43f81e73840c2366503835e6de177120cd76f09b3f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2826d85a3a1461d057104dbed17a212d0b2e15f3e4f5d5f29f4ab67dbfe9b8ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f0334078bd9a3d3a5805fba265a93a02c60e9eca5b80c011a7a914ad205d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:59 GMT
ADD file:3b029f3178b5e1b4334c6406617e14df5bf0ce15ce935acc2cb2dc51b6f151aa in / 
# Tue, 04 Jul 2023 01:20:59 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:21:04 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6b44c60b4ef8f05f0a7be874cdf80559a40b3584e9146bcef80caf7c3bd47f55`  
		Last Modified: Tue, 04 Jul 2023 01:26:40 GMT  
		Size: 50.4 MB (50448681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78762e368694aac5183db60432839840fd36b2b774681232bda6ea38c0cc543`  
		Last Modified: Tue, 04 Jul 2023 01:26:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:27705c3287f2a99db1dd0812f2cf7f07c6f10f338559136db7bf2b984f1f747a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c3a89bed79b89b80de79c9612e1da0c327516081357c9562157ecd5f960aab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:51 GMT
ADD file:fb0d0efa496216eb4150798e9acf6220f344ec01a00121d2ac5eb8efb61344c5 in / 
# Tue, 04 Jul 2023 00:58:53 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:58:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:003d12612fcea91fa985efa292e97219fbb80e0975883488634bf9f8193e765b`  
		Last Modified: Tue, 04 Jul 2023 01:04:36 GMT  
		Size: 45.9 MB (45916479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da294ea69efbe031e32997ebca5cce08305ed429a659b96f9b5e05ac2dac2480`  
		Last Modified: Tue, 04 Jul 2023 01:04:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4931dad40b1a622ada730d6ff26d6dbf2c16e1b39feec3c65b8b3b3de84bf67a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88963793bf0695df5d56b2cbd07befd8d7f95bee13dd2024639c722b2f727853`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:58:16 GMT
ADD file:fc5434a757b40bf7ac5f064c4580674f3f844b4302b8bfb607cbc595c92c9efa in / 
# Tue, 04 Jul 2023 01:58:17 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:58:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:551faad51851c8a8fe8e9faacc89d609b82713385126737d5f6a56acb16ddac0`  
		Last Modified: Tue, 04 Jul 2023 02:02:57 GMT  
		Size: 49.2 MB (49238607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5034f9f1eaefaa9cb076b68782eb1c922ccd111129a07e041fb44701bef13980`  
		Last Modified: Tue, 04 Jul 2023 02:03:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:621e9ac6a4b4e781a7437ddd09926a1b6061263ed30629c0c2778a2ca7422c8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25277bca6ad77c273623c6d9a92643c5e9f98be0bd38d0ae6d448dc2ad636b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:39:33 GMT
ADD file:a125727a859efc0078fd6104c2d5add32d60bc44caafb60b95835ebdca850b6c in / 
# Tue, 04 Jul 2023 01:39:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:39:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ea65c1e207f0f923cefee5466d92585f5e03f36a470e46a88d80c4bb768818a4`  
		Last Modified: Tue, 04 Jul 2023 01:45:18 GMT  
		Size: 51.2 MB (51206313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9728bf419556d019fcbc6f6a562f2d76219f5cb4e934d02036c8f8b514685fd1`  
		Last Modified: Tue, 04 Jul 2023 01:45:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
