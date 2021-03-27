## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:18044b01c29d009e0b6544c1cfd0f64f89e4bef26ba763df3fd4072a68ab97c0
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
$ docker pull debian@sha256:dc818dffb3d22de04368e4ebf1b0edb01f32ff0b4f80d9158b566e7096ee8d73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45379830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7a0526849e16a39ff5275d57b3737120ff87411875b4a398ebabdbb111f768`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:08 GMT
ADD file:ade1e17a38e573b55d9e245968a4f952fbf51fba7018685a96c66c7d0c684c81 in / 
# Fri, 26 Mar 2021 15:22:08 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:22:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6bac2f17c66b135683cccbbe7912d91fb65791cead1d08dabee1b77e6d611fb4`  
		Last Modified: Fri, 26 Mar 2021 15:29:53 GMT  
		Size: 45.4 MB (45379607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5fb4a60569c5a59114d6e69e9de7ee9d62371b97219d05081d6e00925b092a`  
		Last Modified: Fri, 26 Mar 2021 15:30:05 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:090931d65f037f87f0f7e8ab18643feea24cb1b6dff1134a885cf6b0728271f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43176692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e3ac2c393eeb7a60f3f2ceed15639cb4dae8a28102de49f662ade7a6c018e0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:42:12 GMT
ADD file:1e0b664ea8bf886b05af5adee61759e64161b4eb7ba9b7b6f8c74191410351b6 in / 
# Fri, 26 Mar 2021 15:42:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:42:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2bcabda98f87fa6223421d86949e775216ca93d7387a17f83bc3a2a5ea8940df`  
		Last Modified: Fri, 26 Mar 2021 15:49:07 GMT  
		Size: 43.2 MB (43176466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fbd2daa0abee1b432ef0615a6acab90067c2b44600f0ee9636b73873ed1d3c`  
		Last Modified: Fri, 26 Mar 2021 15:49:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:9f6d0c32844fc482d07468c4611a59253958b24d2fd8522b5661a5ac126f4477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308175688740a9f7b42ac4c3d7af38f931e55e42eb89dcdaa1a721d2fa2a46e0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:54:21 GMT
ADD file:d9c3ed66c49b9aec06e15e187a7825c709b185357cd5b62e705b20791b623604 in / 
# Fri, 26 Mar 2021 13:54:26 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:54:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8758b8797ac698605a3cd4da1b526f46f4605470541036d33dd980e76fe79797`  
		Last Modified: Fri, 26 Mar 2021 14:03:53 GMT  
		Size: 46.1 MB (46098526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f0068e63bd3b36a9908a82151c04c6816d72c5ca1fdd8220c1c17f19fb629a`  
		Last Modified: Fri, 26 Mar 2021 14:04:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
