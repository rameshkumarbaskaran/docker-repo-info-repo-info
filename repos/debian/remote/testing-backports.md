## `debian:testing-backports`

```console
$ docker pull debian@sha256:88d531763239518781e135b9f56ecfa400772e519a922a880b14b3a7e62c2c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:f637f11a2ff4380f65f935775cc7c41e96a32cbdb675e15635cbe101104d5da9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55579088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3480a9f7a4bca34b5b6cd26603deb0bea01bc2791686f7bca25b936c77208dfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:45:35 GMT
ADD file:fb66d619557384a14385fa7b5371be954594c4aff1700edcbd9cff422c3498f0 in / 
# Wed, 20 Apr 2022 04:45:35 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:45:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:536039adbcd59ca1bf50e1393d4c116319d1f29168898c56d21c192d219c4832`  
		Last Modified: Wed, 20 Apr 2022 04:52:49 GMT  
		Size: 55.6 MB (55578869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2954f5cd8207b7dac4a769e9a5d2bd826aef31f018a912501ee32b6244b1aca7`  
		Last Modified: Wed, 20 Apr 2022 04:53:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b56830ec5043808dae11812b9a750398e36531e667dbca2517a8f20945af6598
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52995776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744fa615c7b020d32eeec3e2724142fcd90fefdfe9c213eabf7c3737e0ad318c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:56:34 GMT
ADD file:573c96d320664803b8377e6766f4f21f97fb0788e2165a9d3b263a206b25345c in / 
# Tue, 29 Mar 2022 00:56:35 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:56:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2337fc8f6268a3faf54e9f5bd6b46ef2cd2b21fbf508800caebd209c1476fd1`  
		Last Modified: Tue, 29 Mar 2022 01:13:43 GMT  
		Size: 53.0 MB (52995551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8971e4ec6d5852dcb06e57f456599c5d1e76373621df23f06f2b757d1c1f0e68`  
		Last Modified: Tue, 29 Mar 2022 01:13:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:aa3101b785d5c5ac5d9d0ec46c628f5b5e1eca7ea8a72396311971c5423fbbb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50609932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d357eba0f4ad2900cf46f2e64c4229430c0e77d6471da51e71b47b61894290d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:25:01 GMT
ADD file:b3e85f1474d193b977ab578a548dec606711cbc5b6570c8c0905fcc4b9252882 in / 
# Tue, 29 Mar 2022 02:25:02 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:25:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:87d7eb8842f0400851261593da9adb00f4ecfb155e1396dfcba71f1890de3293`  
		Last Modified: Tue, 29 Mar 2022 02:41:58 GMT  
		Size: 50.6 MB (50609707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ccf580b46bc760c2daa8df9382aa5a32ce6132e8bb10b62c9cf75a7f4cfdd8`  
		Last Modified: Tue, 29 Mar 2022 02:42:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5268989e7331d9b0996eccbb735bbd8e604f70430511f83f31eec32ae4591e07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54493560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489d522af0e00f742c3ffaddc107729942676665752c2284b9d972f13579ecd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:31:45 GMT
ADD file:273f985806cb79b6f6b619ba5b9db50ba151174fde33bffc81c25187b0999170 in / 
# Wed, 20 Apr 2022 04:31:45 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:31:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3124af2dc12fec2edfce6b676869cb7dbcea85f39bf473efd3b5674765b68351`  
		Last Modified: Wed, 20 Apr 2022 04:40:29 GMT  
		Size: 54.5 MB (54493338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeec0554206fe7d868b12cfaff256babefc48ca0d621611263220d3124283725`  
		Last Modified: Wed, 20 Apr 2022 04:40:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:9afd9fba556b08dd32a844057bb4ca66e25212b1ba31f546d50fb9635ce988c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56628521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fbb6e94990b8d6eef45c43983b0cfa683c762a59c2443ab77ef86e9afa1aae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:35 GMT
ADD file:04c7a3673259ec46457c82e0627de245152b1a5914d5f33f54a4124b2e4baefe in / 
# Tue, 29 Mar 2022 00:44:36 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:44:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:74cebc6ad2db83c170de3f5fcf9e261c4c2d9a5b7195ac97aadd71dbd0c36820`  
		Last Modified: Tue, 29 Mar 2022 00:54:04 GMT  
		Size: 56.6 MB (56628300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6d918c14cb1fb830b10f0d53e8ed11b2fceb90baaa0bb80ccf47fc0fa3106c`  
		Last Modified: Tue, 29 Mar 2022 00:54:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a4b0dc4649f5a934e9c29eed98303f1d885376e2256cab6ebbea6650192fdb6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54240403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e2109bea6f18f9ef024529c2d611bf31023588a94e0c0512e3525c3704735e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:47:32 GMT
ADD file:024d3880d7b57925a179be264896b146d4cfeac87003866bb0e336c33400106e in / 
# Tue, 29 Mar 2022 07:47:36 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:47:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:246ac5e155c140a71ba5195b835c78579b686fb0d9cbe2cf062e39583ddeac22`  
		Last Modified: Tue, 29 Mar 2022 07:58:46 GMT  
		Size: 54.2 MB (54240178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09255a198d562b80a7f219aab7d72c19e26b492ba0d9b5107b45640f913a4a8b`  
		Last Modified: Tue, 29 Mar 2022 07:58:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ac46ff5702145f41da190f624700889c1dea69e48719435d34b3ad8b668b8927
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59999581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0a8e456600bd71956df9954c25be3055e6c550a291b9058ad571e6c675d729`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:25:37 GMT
ADD file:8974d32898b791c51a9fab708550a07b9a517c5d9bd6db47acd59606984b81aa in / 
# Tue, 29 Mar 2022 00:25:42 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:25:55 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4b9bd4aec57ee466c8fe8d1c7e0f4e5c7e7604e860d3e58360a2dcf666c0b516`  
		Last Modified: Tue, 29 Mar 2022 00:39:35 GMT  
		Size: 60.0 MB (59999357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c044eb47ee027e16c96c45f545f4fdb93bf34bda31903b020d8da1c93b47938`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:8d05e841fca28485a23ddb01a2b92ec19ebdafc996f9e2ba0fbc23a23faaa638
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53839069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4780a43c2570e5af595f31825dbc7f116da4b468a37333a2c9bec9bbbf8bba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:57 GMT
ADD file:923d8b991f14b65ad1dd12a880ccd34f0f6a517d32736abd46b5f3b4dfd767d9 in / 
# Tue, 29 Mar 2022 00:54:00 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:54:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4b047e7b46b8a2d7592481c4bae7396a7669fa7dc3667f8cc1a2cf9adca2837f`  
		Last Modified: Tue, 29 Mar 2022 01:24:45 GMT  
		Size: 53.8 MB (53838847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c8a0ad7423fd413de1371c3d462a576b0debd53789bc0cd2808f0741107ea7`  
		Last Modified: Tue, 29 Mar 2022 01:26:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
