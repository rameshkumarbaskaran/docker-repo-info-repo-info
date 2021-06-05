## `photon:latest`

```console
$ docker pull photon@sha256:749b6f0d4f53e2f8547480328ad7c0976519d1157a1e7ea2b5fa22444e34a558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:e46f431d424e75b9972af16dcdd8d321db7ce1ec2eb3a379864e626c8f5fd2a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15778046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad468f6cc283a828fd111e76b2b679ec7769fb1270bf2fdb7c64fb0f5782e741`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 05 Jun 2021 00:34:59 GMT
ADD file:1275565c3c5afc1888ba5cc1947a3d35a5d52b1b6144db5c4e5aa43c808ab4d5 in / 
# Sat, 05 Jun 2021 00:35:00 GMT
LABEL name=Photon OS x86_64/4.0 Base Image vendor=VMware build-date=20210604
# Sat, 05 Jun 2021 00:35:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ec05e6a2d8ca596be25819b5630f9ac671c0acdd4d1f5adb7fcb0aedc9a7595`  
		Last Modified: Sat, 05 Jun 2021 00:35:49 GMT  
		Size: 15.8 MB (15778046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:be3305419f87c3906c52c768f189642f1bbc1ea29820a114227a780e167f4db7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14811614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b4b554bdacd727f5fd3ae3bd36941f27779ee5814251b86e841189a613ce09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Jun 2021 17:51:23 GMT
ADD file:564aedc8c2b63162a87dc1077419c60ba1d2e112879aafca58dae55a8f2368eb in / 
# Tue, 01 Jun 2021 17:51:23 GMT
LABEL name=Photon OS aarch64/4.0 Base Image vendor=VMware build-date=20210528
# Tue, 01 Jun 2021 17:51:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7411be4436a42639f1f62ff752bcc56d5ef61dc848e812b53ddc84698c0641c0`  
		Last Modified: Tue, 01 Jun 2021 17:51:52 GMT  
		Size: 14.8 MB (14811614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
