## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:97aaf71d5fd2be0d489dfbba53c4c14c46a09ab1dc76ddcbdeba28e23b6af6e0
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
$ docker pull debian@sha256:42f80bec45c438e7ab3cd6cc7c573aeeb577875e3594640f0aa9f5e55b21097c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ead06e63092da1cd29cb0d8da9a25507e38c10bbdf02306c36facbe4482c86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:21:29 GMT
ADD file:66a3c6c69d180deb58eeb9304c5993525431c79605a6972911cd0fb9c84e055f in / 
# Fri, 12 Mar 2021 02:21:30 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:21:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:af2fcd3ed59171fb41a7682292361b44af7829492e944d9dee2b162db1f862b9`  
		Last Modified: Fri, 12 Mar 2021 02:27:51 GMT  
		Size: 45.4 MB (45380182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28848dfbce005200f2d4f9efbe8c2220ab11e57eef92bcfe47aeb78d20125fb4`  
		Last Modified: Fri, 12 Mar 2021 02:28:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ccdc73a3104eb5221f9fb4d680af689e53b88791ac1d770f68a0e379965cfda8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c299d5ce050a4e3b0cc190b5b44c6f7cf3453f29e2fb20ed3511087531aeca10`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:53:29 GMT
ADD file:7554d0c81e5e1d3e54b83a099e8cd1f9da2e6de5db0f444b9145148552edea0a in / 
# Fri, 26 Mar 2021 07:53:32 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:53:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:826816ed9e9ae31e48238b0103a0d184bad49e73a0bf05a1dfc44053264da84b`  
		Last Modified: Fri, 26 Mar 2021 08:02:09 GMT  
		Size: 44.1 MB (44091959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ea490077181446b6acd825f96e00501db94731645fbffb71734dfaeebed6e7`  
		Last Modified: Fri, 26 Mar 2021 08:02:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cefe80c61d8437861670110cac0746617151d1685007a34518cf576f34342ec3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a202708a300331563ec770e8347283488697e233e1d13e1f03e275daa5369b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:19:34 GMT
ADD file:1d9f13a683fabaafb1147a6404ffb2fcddf5d2fe9e2a35196b14f58ba152231d in / 
# Fri, 26 Mar 2021 11:19:39 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:19:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:966d42d960e8ab8f28f53466c84902b3bbed9946f10782cba264c370dc88aad5`  
		Last Modified: Fri, 26 Mar 2021 11:29:12 GMT  
		Size: 42.1 MB (42119855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b34891d582306026ec00112ec5af2d128b8a97a4316d5d65f1e4eb34eafeb2`  
		Last Modified: Fri, 26 Mar 2021 11:29:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:78b2d69c4b5e5beed7094c3ecc6736f75f3fd9b18eb4d8f1cf6708e25116957e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7c8affe998144af5c0cb4c6f5de361f027b8d5a9d3c4ecdeb4c2df7e3be600`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:54:14 GMT
ADD file:90830b3f84b11a5305acaeaf36f5524cd5ae11d28b64b454fb4dd4775c868c33 in / 
# Fri, 12 Mar 2021 01:54:19 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:54:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4bc14244bc7f2d43e8ef422ad82bac8379d41d633b20eddaa53023aed089bf2`  
		Last Modified: Fri, 12 Mar 2021 02:01:58 GMT  
		Size: 43.2 MB (43177547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4cdec44fee3e6b9840a727f2511f29f676ffd383981270402c6a3bb599634b`  
		Last Modified: Fri, 12 Mar 2021 02:02:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:df38bceee60a01562e7eed900595f869817b2776049cbc49077748045bd48460
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2ffaa95ccdedb8ed0459bafb57d9b9e77ad947137fb1f151fa4b9ed0cd6136`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:30 GMT
ADD file:1a81ad34e787e62fbc796c04c25bbd9c157340cd5e86b2b3b13637fa984187ad in / 
# Fri, 12 Mar 2021 01:45:30 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 01:45:36 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9d62a874454e25ae936ce947090ff00c9091fccd6c1326e3601c9107d7fdab7c`  
		Last Modified: Fri, 12 Mar 2021 01:54:15 GMT  
		Size: 46.1 MB (46098170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8397181de564243a088a97e80cd0f6afe5b3cb307020c7cbe9521e751d6abee`  
		Last Modified: Fri, 12 Mar 2021 01:54:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
