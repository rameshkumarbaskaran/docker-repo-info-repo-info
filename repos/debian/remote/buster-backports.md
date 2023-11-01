## `debian:buster-backports`

```console
$ docker pull debian@sha256:8e501bcf59d4738e713f4d8dd4bfffe964a75f221657813c908f319186d5b901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:c48a3dc26fbd9466b3fa6a5e10173ef99ba80e33d850d22272d0d97b11b6b88a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50499349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed915fcce32a4f87f10889f53f912bf7efad437f51e4062d7f90a286f102818`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:21 GMT
ADD file:e12306e266f3e237ff7df5ea95bd339c3eb4a539f31be801afd63a76e116f522 in / 
# Wed, 01 Nov 2023 00:21:22 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:21:26 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:711706b827bb26857b90ceb32b653a05be0e06459342cc05124da0f97f9b6ad9`  
		Last Modified: Wed, 01 Nov 2023 00:26:31 GMT  
		Size: 50.5 MB (50499123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719cfa30b293999a15a04944ed23ca9ca25ca7ae83ebf500092664bae8344ff4`  
		Last Modified: Wed, 01 Nov 2023 00:26:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:166fb6d2eef8a4ca1c48861d3b522b432aeb42965fffd48eb7f0d7ce0dacc39f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8f848dcb9303fcb781ac4600a0b591116f170a2e53267612c4bd3314644822`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:20 GMT
ADD file:ff8efe260318f1cfb8bfc8aaaa6d6bb15c878689f7edea37d776cf111c30fefb in / 
# Wed, 01 Nov 2023 00:58:20 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:58:23 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:608341ab24b1ec00c021d73e16dbb8ca54b2437a4a3f5ae09ca58578603a32bf`  
		Last Modified: Wed, 01 Nov 2023 01:03:18 GMT  
		Size: 46.0 MB (45966058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f78ea97a81ee05e67b098b056a611504084b198aaae6e8940895d6b5be099b`  
		Last Modified: Wed, 01 Nov 2023 01:03:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5cd0f773316bbf970a5926b8da98b72500d714a70a644bb5c11f32807a79e5cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5117898925d196031ca65736e6ae3d373130f7f334cb48be46509b402bba88c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:02 GMT
ADD file:e3f63671dca138b2b525b60f1471241941cdf4dab7f0c17cd91124978716bd93 in / 
# Wed, 01 Nov 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:04 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3db7215fb502c5873a81db7c6fd3214f199f6a1d8034da9d90918ac3220b20b`  
		Last Modified: Wed, 01 Nov 2023 00:44:04 GMT  
		Size: 49.3 MB (49291092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f888bb91f7b575111d8bd9e0ca7dfb2d781fbf84d4e0c6787e9b3021e3bea51`  
		Last Modified: Wed, 01 Nov 2023 00:44:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:5eda61284df4efa0ef563c9a44f059720eecd95ce8b7f3f035a7ce61da450e5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a262b48e17d3e814b14835a8a2493dccf30fb11502b2a3a51eaa383dd00f7f17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:28 GMT
ADD file:65beb9bd9a5ca258316260fb802c65d9c3cc4a9137e0a09a873d4404d5b24fcc in / 
# Wed, 01 Nov 2023 00:39:29 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:39:33 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2e1a1831feefb5bd8f0a9fbc43f06ac287e16d9dd672e28d11eb17f3df2c71cd`  
		Last Modified: Wed, 01 Nov 2023 00:44:36 GMT  
		Size: 51.3 MB (51255735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3382ffcc43ea4f9d87f649ebf1c382afa388325fcc4d2df33e6f6c6a81d2385`  
		Last Modified: Wed, 01 Nov 2023 00:44:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
