## `debian:stable-backports`

```console
$ docker pull debian@sha256:9495e828e114464ea80b720ad65a3f24612289656c2efbfe0e9d93bec8186667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:d1b7170190026eda5a5fd062bf19573488e653daf54e62e787612827719c8db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50382242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430b9ea1d8efc21dec9889f34b82ad4c0d086626d955a5670fe1ee116c828320`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:40:38 GMT
ADD file:7d3b1ec0cb6ffcdbb880b300eb716cafbd8a9a44c558f3b9f1ab9b4a1655dae8 in / 
# Wed, 26 Feb 2020 00:40:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:40:43 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:252ea3946b692b0b70ab430ddee87f6ebf44edb4f1adac8c56dfbf81daa7c55b`  
		Last Modified: Wed, 26 Feb 2020 00:46:35 GMT  
		Size: 50.4 MB (50382018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231a9485f104f4411cd78b8c0ed1865264e9c677a719b08c056c592ad6848409`  
		Last Modified: Wed, 26 Feb 2020 00:46:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3804db89c4a71531636dce90a36347d64dee79a0a44d6218929eac3ca3de8e3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48095880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a62d6638dd1237e2ea3d32b260c57bf4ef5a391ec0e310b1d5f55ed32a4e291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:51:51 GMT
ADD file:42d5ce181b2dea32bd3662e7bc9b647e766a4a2b51acb297776bc099ef4b90ff in / 
# Wed, 26 Feb 2020 00:51:58 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:52:13 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:211af648d3486da54c28b3c4802ed3c19e079c61c15ac268063776d9a6b31db7`  
		Last Modified: Wed, 26 Feb 2020 01:02:34 GMT  
		Size: 48.1 MB (48095655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e681f3d86d75e07185916603fa417eea9947d5b4c3bc8c7d5494aca7acbf4bc8`  
		Last Modified: Wed, 26 Feb 2020 01:02:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:86f4071b87381792bccb5a165cd1748a8999b0818165ffa8db5223e3ce5916d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45862941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0426743175017ce855978c6c8098dab9673170d04ea99da9cc65bace327973c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:58:00 GMT
ADD file:b97e6bd629a6e0b05682f6df0fe30961d66be8952cc42e7ebb18910b451c130d in / 
# Wed, 26 Feb 2020 00:58:02 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:58:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bd5606d361f8b01b969124a518bbcc6e859a642c70cd84d81e803950bad64ae6`  
		Last Modified: Wed, 26 Feb 2020 01:10:46 GMT  
		Size: 45.9 MB (45862717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84c6c0c38649110b939fcedc831356e8d8d48259533fcb96a1eb9a2b6a7ae6a`  
		Last Modified: Wed, 26 Feb 2020 01:10:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1015ffac208312e87192fdccd8de2309e8d8d03f880252290c92311b3577cbb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49170190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558b67057f08410562aee035a90a173976fa4754d459fd11dc43ec6543f8e2fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:49:02 GMT
ADD file:04dd546954ef09cef675fb50b5efd9e60ba9bf249631ab274da35f4e313a09bc in / 
# Wed, 26 Feb 2020 00:49:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:49:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f72782ac78750079f77c44288a3f588edf59fcf99af5fc06e1b578a46cf5eae9`  
		Last Modified: Wed, 26 Feb 2020 00:57:52 GMT  
		Size: 49.2 MB (49169965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f064c3f519722edcf3ca03ff067965b4115b72fe4b51249acb3feae989223ae1`  
		Last Modified: Wed, 26 Feb 2020 00:58:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:f2079b6c78f4599acc28280a88365d2b1275b1bcd5402f722e627667d93d0ada
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8debeffd3945cc7ed9ab4b923613569378e58e050868338271fe093389553c74`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:34:47 GMT
ADD file:e583a8d1a9bc51a5460811e19c7e5f1a7c7d0f7675fc3f0a736cd099c8770367 in / 
# Wed, 26 Feb 2020 00:34:48 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:34:54 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:21db9efe6497a43a542416166e47e6fe6d0599e0cc7c15b611b9ff041b8bdd54`  
		Last Modified: Wed, 26 Feb 2020 00:41:08 GMT  
		Size: 51.1 MB (51146113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc596a1424fe6fe69ee743be5ab66bbac9cfb98e9d8360afbe77a86d73a78e30`  
		Last Modified: Wed, 26 Feb 2020 00:41:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2b024aefb72da995554297276e6d03691f8a9dc830064cc06c9bfa9618f81e1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54138640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0507cf77b7bf661e3736b26cc584d1d50b0455b8f9bb7578196a4989d080e189`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:34:50 GMT
ADD file:78df2ed8ab3a22ca88cb634c14b298fc67a65d5d2738162e7e490a564edd960b in / 
# Wed, 26 Feb 2020 01:34:58 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:35:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4d12ae449bf11b07b4d9f07976cffb0c753f5fa1a81f0f57ed433a4b693ca15`  
		Last Modified: Wed, 26 Feb 2020 02:01:52 GMT  
		Size: 54.1 MB (54138415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c79e62cb499b50930fe176955a08a00262a1605c77da5713d5906b84d4e91ae`  
		Last Modified: Wed, 26 Feb 2020 02:02:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5d7baaea8a20f29060d53b07ed9b6ae705663cced75f61ef398d2954c9e8fa3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48958316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e165bb7a84ecd52d5b4693ca73c238762cd3a67ae54f150595d41f6510e18626`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:43:57 GMT
ADD file:be5cdbc6b5ce85fa7b01883858f4de3f57f49168921c7b4adfd553253075a6f5 in / 
# Wed, 26 Feb 2020 00:44:00 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:44:06 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:59726d02408e7d0cb82e910945264a18f5640d36ea5e213e36e39d33452ea586`  
		Last Modified: Wed, 26 Feb 2020 00:48:43 GMT  
		Size: 49.0 MB (48958093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb5c2be6211404dd3d7be9656b1ecf1142e4547d990274eeb2cae0695b6a742`  
		Last Modified: Wed, 26 Feb 2020 00:48:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
