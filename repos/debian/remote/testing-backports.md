## `debian:testing-backports`

```console
$ docker pull debian@sha256:75fc784b19ee6b137e8c8cc7280c34f3951cfd138cc0d6222f528fd696b24609
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
$ docker pull debian@sha256:dac77ef4aae9f9f109a76dcb3cfa5595e759fb529606c7ab619af0e85e638482
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec6093b45f2296271d9d9b360f460bfa69f54cf76e4ee59edfd8cd8f05357f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:22:36 GMT
ADD file:de5374a9ef9a0a868df3aca8ce7b7d50abbcf762f41fef9c58012f36d97f78ad in / 
# Tue, 04 Jul 2023 01:22:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:22:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dfc7daecfaf18ac4d0f8113f6edff692b509a3dfec300e2dc347fc813f7fd887`  
		Last Modified: Tue, 04 Jul 2023 01:28:45 GMT  
		Size: 49.5 MB (49523824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9fed4b63c8938203bf3163a65164dedb2fcb2489973aafcaf6b0dbdc8b3394`  
		Last Modified: Tue, 04 Jul 2023 01:28:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b2352720303c39a846d93cce5b5f0682c2c8ba26a65aa76707a1297e729a548e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47360298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ea8f8432e5742e56b05e6c6e5ec85af71be2862afc4793bd16a3a9c32f5a3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:49:41 GMT
ADD file:37d9b5c589e088f6abc6b26d8bf3a37c115e8539418cf66fb14b429429a8e241 in / 
# Tue, 04 Jul 2023 00:49:42 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 00:49:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dca32106e2136c2ebbdad8bd8bebe2d128536b0b1925018c65c0a100df0c7dea`  
		Last Modified: Tue, 04 Jul 2023 00:54:36 GMT  
		Size: 47.4 MB (47360077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3cb3d074c15c2f15486611dfc3adf08691b42ab68c316ae42f2b6987bb0a8a`  
		Last Modified: Tue, 04 Jul 2023 00:54:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6c16a88dca2d739fca98e1ed2e9a8fa410aee03e760669231a771e40b2cc44b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45183060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1916f5b52c41748cbe1b8296ab771f892a0ed4db5c3881dabaf00ececcbfce9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:00:35 GMT
ADD file:bb6a04281258377dba4024648f4859eb16850c1884664013cf4c68e2f64ee71d in / 
# Tue, 04 Jul 2023 01:00:37 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:00:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2dcfcdb1f06b29ac822690bc8922ffadb1885001e45609e1b1e7c951d8aac132`  
		Last Modified: Tue, 04 Jul 2023 01:06:49 GMT  
		Size: 45.2 MB (45182839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adab0aa5ce5beff54e97f4a0c85cd86c0fb45400fce6edbe1c7267c554e95463`  
		Last Modified: Tue, 04 Jul 2023 01:06:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ef3100ef4124e8d0802130ea08b95c1b661f0ccd40295dc3491758306c7e184e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96ade264ad6ef6a74e49b0e168125e0815824fed5d4ebefed655487abbf9f5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:59:20 GMT
ADD file:7c88bfb3f20f1d350105594d828661ca616d541d9efd2337a981f3da607d714a in / 
# Tue, 04 Jul 2023 01:59:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:59:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6c47644f3190914c8cddc6aa8fbe2992624219125ffe676d8186f7a2492ede06`  
		Last Modified: Tue, 04 Jul 2023 02:04:55 GMT  
		Size: 49.5 MB (49524494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbb618a03e1c123aeaa5b98f535fb6296e87cbdd574f7b331998188fd4909b8`  
		Last Modified: Tue, 04 Jul 2023 02:05:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:6a099eed248af642536848d0f579520cb1c08c956cb5d7ca54c0c3be8f5e0285
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50539612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bbc6ee51b7181b1c4bdd1cf827ee85b4b8ee1a97461be7e2d39b8e9cc597d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:41:04 GMT
ADD file:800f4f1bd5ad2906c772ce8b268570bef9103addd86518d8f307f8237a90353a in / 
# Tue, 04 Jul 2023 01:41:04 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:41:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:87b0c9e90e45a821072212b669ce2d860a42c15267266ee4d5cccc60e216d7b7`  
		Last Modified: Tue, 04 Jul 2023 01:47:40 GMT  
		Size: 50.5 MB (50539391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6004532d2d9d8cb23425e74d0c9341c5a8d65799f75b7daa853e74d98460b222`  
		Last Modified: Tue, 04 Jul 2023 01:47:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ef1d942f7ae0ab03159830456013fc125b9360020f426a1e6b7bef6f34183463
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49497209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2d2ca38aba81c88c4ade90bfdddd3d45d25e526d6fc074fdbbcf94ca28d302`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:14:46 GMT
ADD file:dcc9571f3f9ebdedc190ed4e00a06ec3448554688dd0f962e043ee5021f2ac48 in / 
# Tue, 04 Jul 2023 01:14:50 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:14:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3c1f5b710b54bc6dd95bc402e09e8bbba2eb71932091a3431e091fb6d6d3ff09`  
		Last Modified: Tue, 04 Jul 2023 01:25:35 GMT  
		Size: 49.5 MB (49496985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9394a6bbf60dc3d29dae2c4844ba91a7177b0b8521c28f3f3651ac20799f1b82`  
		Last Modified: Tue, 04 Jul 2023 01:25:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:30944a09c2e687aac8795292591ca6d52ea170dc39c3e1d1e2c23e75c9e02af2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53510693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bdeb8bae017d5fd68d82ade20d7a11b73c5169354e477e135509852d77a4e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:51 GMT
ADD file:655c8220697661701581fae778e1d70fbf0e03ef7ef1eb7d69e9fc161234d8ce in / 
# Tue, 04 Jul 2023 01:20:55 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:21:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:becb5953410e743a3e23e594ddf8545a47fd1ff0109bff6b5da8fae334557515`  
		Last Modified: Tue, 04 Jul 2023 01:28:38 GMT  
		Size: 53.5 MB (53510470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1faffff9d1c0247ac92887572b457d8ab4467225894f18e64d4003bfd206006e`  
		Last Modified: Tue, 04 Jul 2023 01:28:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:30578f954d75117d6c735a90e2c7bf3aba614fad8761c7a290930b690d740b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47950010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245f0396152c7f548c48c1dee9d35f4d1071f8ce5cd6066e4ee5c636f60450c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:34:19 GMT
ADD file:905d0d0e6d4f57fc2258b13e088f9d03967c81aa9affec0d939ac1dc063668f4 in / 
# Tue, 04 Jul 2023 01:34:22 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:34:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91571ef190c1d77037a9711c8341236d7f9955149bcb264c8c332f20daf0519e`  
		Last Modified: Tue, 04 Jul 2023 01:39:01 GMT  
		Size: 47.9 MB (47949790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63aee5761630d0c58da6ea8114d07db3d1a2024787d734933d1fc5c16fc6d227`  
		Last Modified: Tue, 04 Jul 2023 01:39:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
