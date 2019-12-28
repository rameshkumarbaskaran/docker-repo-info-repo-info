## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:e817bb0e980c675750ca18e1b3ec7149b38b24757c9af2952e1f6ffb4ccd81ef
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e88faaf0f731aa49940a5e7de16240423ff037a2ceb0ec04d8117dea8fa25314
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070c37207d0da76df5f5e081d97c4e04059cc2331f86a21883d175700ffa9cf2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:21 GMT
ADD file:5c22ce9b2949a415a880c9feffa2026f414445fb76f49b181d941535edd4541e in / 
# Sat, 28 Dec 2019 04:22:21 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:22:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:51ec2ad88f35eb32a81f6492a70dcd25f5e97ae3b049e2f71518ee15bd8555fc`  
		Last Modified: Sat, 28 Dec 2019 04:26:54 GMT  
		Size: 45.4 MB (45380720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a14846cebcee07d6f237857adbd33b576ad65576c7068bad83377d4437281`  
		Last Modified: Sat, 28 Dec 2019 04:26:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:54ce27baa70c88cbd882ce5d71eda1a5c9edb0d7be56a91ef6e922e033f223e5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44073205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391a4d64c08e04d945662d38af8871de8b3cfadb918ce90531462eb0d8d75fdf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:51:14 GMT
ADD file:54f5b2f84944e63a12fc306533376f61aabb5aaf07d67af5e9c5974456c492fb in / 
# Sat, 28 Dec 2019 04:51:16 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:51:24 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4dd9502091a60f6a7c89d93407e28b838876ce124e74afeb6098cd0121152e94`  
		Last Modified: Sat, 28 Dec 2019 04:58:09 GMT  
		Size: 44.1 MB (44072977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e5a8c4543fcdb197b08af2c95ee7706981d7ae084657c21dcf7d8f7b51711`  
		Last Modified: Sat, 28 Dec 2019 04:58:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7a9b6617179a5083d0296565d8ec4a68dc1df0b70d1b759eb1d07c5885106cd3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42108316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603064fc3f1561ed462b38773a104d40601057b5e9773905893a9d708820abc1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:00:44 GMT
ADD file:a1cd192730787c1a4ac3b244f5b5219f4fee785e449dfd3b62a6b5470ee78a9a in / 
# Sat, 28 Dec 2019 05:00:46 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:00:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4aa2232c0fa1caf12713cc1f972f715ad9191e0b35767afdce8f458e9e6a7532`  
		Last Modified: Sat, 28 Dec 2019 05:08:56 GMT  
		Size: 42.1 MB (42108088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1991da9234918a5cce8ab08fcf140c00c0741e8359bae542cf42bd9aeb11d2`  
		Last Modified: Sat, 28 Dec 2019 05:09:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:43e916b204bc06ca887916edf16da76fb15b7334e05e7151bb77eb4549206fc5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43166644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f07aaa59480bbcfc4456cce817d3ca9876f90ad2e1469195881b362430a96b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:25 GMT
ADD file:e97de48176704e16bc642406081c2830bbd6be671b596335e35a9353bbabbda8 in / 
# Sat, 28 Dec 2019 04:41:27 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:41:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b926f85ca5016ad8c548b06055d147be480eb52e8cbe4b8cd82d0b083fc4adad`  
		Last Modified: Sat, 28 Dec 2019 04:47:17 GMT  
		Size: 43.2 MB (43166416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbcc675e1bd7e4d3b8ecdef6f55136db6b2439e2ab1d349503c25f0cdbac8c3`  
		Last Modified: Sat, 28 Dec 2019 04:47:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5089c8caa6413f9e5659e988e262a37c8f056acbabbcb9147127ec92f299a5fc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46100423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a3be864b513b3f4e55195ccbd5ff446e58051a97b65139cbb9706abc238836`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:40:34 GMT
ADD file:89720e3946a126dac442237e08f7e2dfc99d0f5cb1423990b8564f123a3592a8 in / 
# Sat, 28 Dec 2019 04:40:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:40:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:37681181366e2b59125abfff27a04948d8677dabf4b11632983151971ce52ac5`  
		Last Modified: Sat, 28 Dec 2019 04:45:44 GMT  
		Size: 46.1 MB (46100198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aea5eaf7f458e13ce760e25c993b587e8aa85c9cf4288cf27321db059bfafd`  
		Last Modified: Sat, 28 Dec 2019 04:45:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e64a5be0d522ac9a5856b960effd0ea5b8b0c02c1b2a319a81ca377206078b59
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45652749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e7a32c1d9cb8de4e0b89ee495fbe8c02b45ebfc2c8131be05d0b8163e0e5f5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:57 GMT
ADD file:de172b74ee4facd433c9afd60686bbdfdb83b94677c492c351ab95d59c62fd39 in / 
# Sat, 28 Dec 2019 04:21:03 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:21:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e12b817e531054427277b26863bdf5514dd4eb128412f1559c6a2073415bad31`  
		Last Modified: Sat, 28 Dec 2019 04:28:41 GMT  
		Size: 45.7 MB (45652521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967b8e36bcfbbbc995750a8b74adb2feff3242544e127f8a4f55f03450c657e6`  
		Last Modified: Sat, 28 Dec 2019 04:28:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bf13d1cd29f62c56c79fecd6b7b7610167f2ee9e2a4006cfdcc922eeb9b51258
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45241898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db07ad74e2ed94a15c7597885248f27720a22a1ac3f6c3c4a8053ae9d8cda0e6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:12 GMT
ADD file:dde32a0ed56a840ea499c640e91a51ba8a757277d38f02e4eb977ccbe869d4c6 in / 
# Sat, 28 Dec 2019 04:42:13 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:42:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a7634dc03391213d5cb9b1d60f6455dfa8b6d0ed3bb7a3205cc81eb367ca448e`  
		Last Modified: Sat, 28 Dec 2019 04:45:20 GMT  
		Size: 45.2 MB (45241673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb1b5634720b87496c6ca611fe4910990b40f9b0274e3c1dd3ed31aa0b2afce`  
		Last Modified: Sat, 28 Dec 2019 04:45:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
