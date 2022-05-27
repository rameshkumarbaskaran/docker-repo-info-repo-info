## `nats:2-linux`

```console
$ docker pull nats@sha256:9a9a7f8cfc23b037f40e40d012e8989146c241d95f3bf65b7a3b5595706fbdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7df9a2712c9b7e57f228a270f9fdfaf95f8662890dd90719ab08952fe93cc99d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86f50672b8fb25a83d599295659904a27d366e8cad89089ddb9171c79e31c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:56:05 GMT
COPY file:8de8b0cf8e6edf54e413c112cd66aed537abed387a26ba749a9293d43cdf6594 in /nats-server 
# Thu, 26 May 2022 23:56:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:56:05 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:56:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:56:06 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:56:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:770fa9c168613edbe7aa7007d2cf8492c6570efc1ddab217fa32772c6b72dd48`  
		Last Modified: Thu, 26 May 2022 23:58:21 GMT  
		Size: 4.2 MB (4245317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d80ba54887e3752f04df58e1ab68c9805dc2aee54c543d487d8d51a2c88afc1`  
		Last Modified: Thu, 26 May 2022 23:58:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7bc2fc55c212c8368adb1b2621b9a1712ba6da1081ccc4aa1dfae50105990920
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86dfb5220f8792be44bdabccf4dc1c312e1004d14749d7d34aad9e02c1ea541`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 23:31:09 GMT
COPY file:9d84b5b248567f164f0dc7646950f5fed3ac3bd00d93c42a779ee610cc080673 in /nats-server 
# Mon, 23 May 2022 23:31:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 23:31:10 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 23:31:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 23:31:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 23:31:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b834136380f158d8f35c7a82544874f779fa05c88a5c0dd7008452a9a57a91f8`  
		Last Modified: Mon, 23 May 2022 23:33:31 GMT  
		Size: 4.2 MB (4241740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab1560f3ffaba7728404cb44977e18808c9085452d0ce82a8bdbbb775aed40b`  
		Last Modified: Mon, 23 May 2022 23:33:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:87b1afbd78a75ee48cb6b37a8522bbb01f5e9b5047b095b16cc4f241774a48d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4227885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bce5ae01237736c7e0447d8cd1b2dbe252eab3ab5ac3b05d98b646b2575cee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 May 2022 23:53:56 GMT
COPY file:2dbd94c6c11f89ceba3241f1efe469d0a06f0aae91abb77f3d79756676d0be57 in /nats-server 
# Thu, 26 May 2022 23:53:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 26 May 2022 23:53:57 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 May 2022 23:53:59 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 May 2022 23:54:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c74770da2ea808362085edd6dead652091b3e3d34c1e32c50015a6a5bb36c02`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 4.2 MB (4227378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988af7458b707048622e497d5ae818b77d3a24ed0295a7897ced8f003179f7f9`  
		Last Modified: Thu, 26 May 2022 23:55:21 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
