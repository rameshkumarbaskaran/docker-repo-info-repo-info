## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:a87483b4362596443d9696db6e07c9635dfb878f19d86afde9a8c643b3c9e04b
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
$ docker pull debian@sha256:39cec427dc9f3fb9dbf3fac5c776d0454cbc23c1c7d7a83f9efc0a945600c32b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45375948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20272d3e387a5a2506a0a178983da66c0dd9d231bdf4d6f8d3c86f38c9d401bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:00 GMT
ADD file:b577e57e3a2bf0163b97a4cf9e6b0083207bd14d640c6e532a9dda841a4adbe9 in / 
# Tue, 09 Jun 2020 01:22:00 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:22:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01e263ec4a5420955c5db27ec32a88ae43edf1726715683a66a941aefc91c13d`  
		Last Modified: Tue, 09 Jun 2020 01:26:52 GMT  
		Size: 45.4 MB (45375725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3204670e7d7bf5820c35c035519a03a937fe970251842b17bb6615711f85691`  
		Last Modified: Tue, 09 Jun 2020 01:26:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8e350439894bdba7185f547a5a0ce0ec7e21fd04c137570d3481a230557bb039
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44069474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edccb49ec8d20665918ffb8a9b58ad3ace0e9875820f26ff76cf85a3127e1525`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 00:53:28 GMT
ADD file:0aba4fcdba0c4e2f8fb4b6ce1643241f7683fb2f97a91f1c728aa7344ea2ead7 in / 
# Tue, 09 Jun 2020 00:53:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 00:53:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:611b140fd33ca79019f5ef8aabb4288d071cd2441b42919659c5beb34d51c297`  
		Last Modified: Tue, 09 Jun 2020 01:01:00 GMT  
		Size: 44.1 MB (44069248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7326406d482f0584b3fb44ac44ac8d2de22667ef74d909669aa27911444bc`  
		Last Modified: Tue, 09 Jun 2020 01:01:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a31fde922849b1ca1a3388e9787e8895effce5592b1d9db3c29647126a74facb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42102728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b74af4d7bc64106b9dfd2b7c78fb48b8f928580fec288b2ad2b5098d26d22fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:03:23 GMT
ADD file:0e1f6b8583903951e6d7043a8ba279524fc474c1c1c032ae827569ff3470fc18 in / 
# Tue, 09 Jun 2020 01:03:27 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:03:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7b2ff4611db2205acdfd8765ab0567172472679779c73bb5c2eeae024b26156`  
		Last Modified: Tue, 09 Jun 2020 01:11:55 GMT  
		Size: 42.1 MB (42102502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152e0e553fc7be7a868898398a4c46bf05f3a1714bacf84c0ae81bfd807ae174`  
		Last Modified: Tue, 09 Jun 2020 01:12:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8ace90540d4a1d870e5acd505e24bb77b6331c31c46d3fbb82ed3e4cd5149281
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43161162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af3051528c8110285405818839644e0fafc2385d1f0eb7eb40203971b636fc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:20 GMT
ADD file:8a4e37011427580a48a259592be2f1943cf27205185089ac32ae32901d68f902 in / 
# Tue, 09 Jun 2020 01:52:22 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:52:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a9852e6acfd43403a67137356a293ece14912b43fbfe4fc7ae405e0fab83794`  
		Last Modified: Tue, 09 Jun 2020 01:58:32 GMT  
		Size: 43.2 MB (43160936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1735ba194435c2abc3ee9db1bff8c9622452adb561cf25f9fde12f7af5b321f1`  
		Last Modified: Tue, 09 Jun 2020 01:58:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:9b43cdf8d9169e4d4a7601ffe671b6470a4c88b65e6b687f9a8028186b4b6e30
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2a42a00039fddeac2f286c1d6d8718b5b432f7c4716b03d32dceedfadc56b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:40:54 GMT
ADD file:464aaadbed45e1b13e4098de49a719e0abf8a239fc39a9f36bfaf4007ca70f4e in / 
# Tue, 09 Jun 2020 01:40:54 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 01:41:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:30a964ea19298d96565cfc98b6fd33b068f38659121855bb2f92a84a0849a938`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 46.1 MB (46094829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f2a8cea6bd7feb0389a7ced455580ad4a3b14b14fc3baaa00e5e7d0d386b5c`  
		Last Modified: Tue, 09 Jun 2020 01:46:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
