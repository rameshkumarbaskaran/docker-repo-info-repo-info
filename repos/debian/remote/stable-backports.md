## `debian:stable-backports`

```console
$ docker pull debian@sha256:80a06a7337a98500a6be47086e17b00b998dc7de18b1dd8c3c20cb07a4e9174e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:08e99668a3ada9bc1a3642ec405a9264afab6c389bb1267ee395170a2f38d653
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50400509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c2b275ea86f4b1b9d5008ecbfc33a1d73991203e555b7d683e611a924b8378`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:52 GMT
ADD file:1d577d0394d080f5e0690fd8ec4c8d817fc2ac5e04f183ee23038c03a3062cf4 in / 
# Fri, 26 Mar 2021 15:22:53 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:22:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f1e2f6dcec4def91cdf0268bcb20addda06c2407abd9f7a3afb104dff3d19efc`  
		Last Modified: Fri, 26 Mar 2021 15:31:27 GMT  
		Size: 50.4 MB (50400285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c80f7bb387587f9cea5ed28e2288fef4436d1c887674727449b27d6f0880809`  
		Last Modified: Fri, 26 Mar 2021 15:31:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7f6f423fb920ae2c1a1cd58ae8bf09171a58c9eec7d49f849c41439c048dc6d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48111928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8e80d6c81170e65186be58f60a9c5cc1b7eeefb20b5405db7bee194d7c41e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:54:51 GMT
ADD file:a6c8f40e47f56cceaf581ce8f44c6ef882f06d12a1e5f084b445d6c67171ff8c in / 
# Fri, 26 Mar 2021 07:54:56 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 07:55:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a85d504283138f8dbc9f6e441611402a4ab846a70336785a9babbe9795a1d265`  
		Last Modified: Fri, 26 Mar 2021 08:03:26 GMT  
		Size: 48.1 MB (48111704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a7f75bf2df0db786a1ea44036349b051f9c830d1d261a19066885ea82fa8f7`  
		Last Modified: Fri, 26 Mar 2021 08:03:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c18e28e8fe79b50aaf50c69c88fd742156684900911657e3457670418e61151d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45868237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb67b34b68a050335645c20179b1d26d92b9e33fc2717c4d7f1229fa8ce8f70d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:21:19 GMT
ADD file:e6c2753f736126a2344b7c6303ff63ca35cc9a6f1979e9e9f8ed3377cd1bb143 in / 
# Fri, 26 Mar 2021 11:21:26 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 11:21:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f5c8a16a209d2ff8f288e46196d51093089adceb0faf2e107e51f9743b061a1`  
		Last Modified: Fri, 26 Mar 2021 11:30:29 GMT  
		Size: 45.9 MB (45868014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366f7fbc2283e9b1ca08cf472dd72e6deb072a9b242ec78ec64e5908769054e1`  
		Last Modified: Fri, 26 Mar 2021 11:30:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6c978451f4c7c5fecd6d7d26d0511a0952095eada9f61c0545d0a8f3e9b81cf7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49196374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91c02e7a997ed5040ea1d67cd6343f54ea510de6106072849ae80d4df4121c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:43:31 GMT
ADD file:3bbbc508311f42ff9c902e040b43c17dece5c91f82dcdca2748a6a04e12ea940 in / 
# Fri, 26 Mar 2021 15:43:34 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:43:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e40e7b16470e089dd63a3f657456fa9c3775bcf63bdfd290346955a707346a5`  
		Last Modified: Fri, 26 Mar 2021 15:50:18 GMT  
		Size: 49.2 MB (49196151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402cdff2e5acdad3f0c48393d46d92f6100f2d2ae46bfc483d5cab23ab1d443b`  
		Last Modified: Fri, 26 Mar 2021 15:50:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:3b39eb05ecd1ae0e5688e7406e5cf405d238b0090e656b407461aee3c50a3b50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702231e9ab766d5090b6ea5cb3c68eddc5e5bffbf8c3de40c71e9dfa94c188b5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:55:28 GMT
ADD file:4fa5e1a29654a520dbf701b4aab0ff0631735172578603fde9e394da7326e1cc in / 
# Fri, 26 Mar 2021 13:55:29 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:55:35 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:60ccede0ba7fa3bfc9dda23c4d79d123b9e0c71528141e965f341c9261066b08`  
		Last Modified: Fri, 26 Mar 2021 14:05:35 GMT  
		Size: 51.2 MB (51160396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6552c158fe3a23f580facd65c7ddf9df90ea76ed3b024b07bfb67314ad155f67`  
		Last Modified: Fri, 26 Mar 2021 14:05:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:96b7f504ffe30cf9874a4956fa6ac56d50b8eb1ba456e8684004671ed84b4426
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49029497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa939c308b407e202e3206462fb4c60c3c1f7b6b4d939fcbd25d272acae12291`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:11:05 GMT
ADD file:c594dbac49f9a1fadb44a691eb000b64b3acab66b618719827e70080cf9862f9 in / 
# Fri, 26 Mar 2021 08:11:06 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:11:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:50a5ed2929d8be8cc22ec80f8dc77df6d004975610ff0d7ac5339f09c6817819`  
		Last Modified: Fri, 26 Mar 2021 08:18:30 GMT  
		Size: 49.0 MB (49029273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22250ca3da298cbcb05f6e801060a60eda587f581fb83e35f470088b33c0553e`  
		Last Modified: Fri, 26 Mar 2021 08:18:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:21d8401456af25048fb597dab6787420c8adc08823513d21be51224cafa63c7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54136849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9719c851ce11729417280700b50a25db507dcc78573fec057306b972ba80d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:15:32 GMT
ADD file:d40ce72b1875252f986b37705810fe2a482294beec53f71bc4d81a863d536829 in / 
# Fri, 26 Mar 2021 15:15:42 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:16:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4d32c3342572244bac90d8a13925b4df122542cac9d151c0803aaaa5ddd09380`  
		Last Modified: Fri, 26 Mar 2021 15:23:16 GMT  
		Size: 54.1 MB (54136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28674d03324c23ead7447c723fd379ba4fcadc5c7a6bb3b621587cb544a9b6`  
		Last Modified: Fri, 26 Mar 2021 15:23:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:4c631e3c9fc00722d36b7192f494f96f75ab6b7efd2cb60154f2923653b1577c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48969134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4c69e595a22f0deb7302a70adf004e315ddd214acfbc12b8e30054801cf483`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:54:30 GMT
ADD file:222056378671925db3da1e7c45ee1f815c6a29cd8228b7a37203e0482be398cf in / 
# Fri, 26 Mar 2021 10:54:35 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 10:54:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4ed40f62df44044cce9f61f09c8195c9ebd7d38e8cdacd02aea0b9233a5d68d7`  
		Last Modified: Fri, 26 Mar 2021 10:58:27 GMT  
		Size: 49.0 MB (48968909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5105fc26402098fbbc1e49134bb26209e8e1a849330af139bdf6f21aada6fed`  
		Last Modified: Fri, 26 Mar 2021 10:58:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
