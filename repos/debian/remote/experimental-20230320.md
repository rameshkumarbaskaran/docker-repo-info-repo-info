## `debian:experimental-20230320`

```console
$ docker pull debian@sha256:c7d064e55f19223bc4cc147c6f987b488a5363d38a89d7e3e12b212f89a6b0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20230320` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:efc8c53c7e8ec804a3fdb97e5d41f1b87b6f03c1c262411cf5f14e7930fad5a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49319208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64b496c658ef5ff8b09f4eb071f87a0192c7692fdbf8c883d0ea56c91adaeb9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:46:25 GMT
ADD file:0affcb10430712dd73055564d3fe7c0548bcc203c6e8a0c200c4b48ba52900f8 in / 
# Thu, 23 Mar 2023 00:46:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:46:33 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b400817afa0c1b0b5323fe5eb38a334172ba17ead32c49762767d869161603f4`  
		Last Modified: Thu, 23 Mar 2023 00:51:02 GMT  
		Size: 49.3 MB (49318987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4cd8709e1cb452a702dbef9012d6bb8eaae94069e7e2436cb0ac527ed5856`  
		Last Modified: Thu, 23 Mar 2023 00:51:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230320` - linux; 386

```console
$ docker pull debian@sha256:715da7bbf5f20a42f1bf9e3965de1761da0a4fb3641e8d64f11006067e9f1b85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50314767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d355426c99a7371bf868453a8ba6b543b110c4f84c4221ec52c2ed493d92e32`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:41:14 GMT
ADD file:91051a34bcb35ee9e94090f813b07bf915da58d01acb1e1a51031171a6eb0ce0 in / 
# Thu, 23 Mar 2023 00:41:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:41:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:350e50626198efaebb626c28f35f6aab6f02ce94e1bda1166f63672ca9c13303`  
		Last Modified: Thu, 23 Mar 2023 00:46:39 GMT  
		Size: 50.3 MB (50314547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562cf269bd2f25740bc81e36165a927c8907b0eb6d643c883ebf01dcc3adee47`  
		Last Modified: Thu, 23 Mar 2023 00:47:01 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230320` - linux; s390x

```console
$ docker pull debian@sha256:4946ca3720705048b10646de1f54f8721815c13b48f54535a3465ea8db6a8f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47648248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb210152ae579ea153dd4c8c32cf41606fc0c7ec5d3ec25b3bdbed57caae101`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:40 GMT
ADD file:87a1c5a697c0ce402d70710d206bfb13b0399785b6b9120109f7099c256199a8 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 00:45:56 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc794848966cb11ec8c207602b033a6a5b7e3c9334d0481e4d332bba4c4cd57a`  
		Last Modified: Thu, 23 Mar 2023 00:48:40 GMT  
		Size: 47.6 MB (47648028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efff8fb6d8c9f34679dad324583c9e11c7365702cc08af1adae4de7644503b6`  
		Last Modified: Thu, 23 Mar 2023 00:48:56 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
