## `debian:stable-backports`

```console
$ docker pull debian@sha256:04c600f0def5708a6760d2ce0e43204af3e853a3b6a5bdd7370b90b530597473
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:e48257b4c3c946ffd8e961c7ff05895eecf707a5ff53102e778e693d0976bdf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54942031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6432b06c60d3cdce30a05e1158c966c1d80fe60b2456b7b3488412599cda77f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:44:55 GMT
ADD file:70d54120d8cfb74e196d7f06205a5afbb6d666c607d98bb6fb288403d27cac5b in / 
# Wed, 20 Apr 2022 04:44:55 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:44:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7e4019cb8009a11f4d0c0305817ebafd8aabc5efdd2ccfb680768c686fbf59f1`  
		Last Modified: Wed, 20 Apr 2022 04:51:23 GMT  
		Size: 54.9 MB (54941807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fbc92289b20574efbecaffcafecd68353d8c7d8b0bdcca29247eda94c2bc50`  
		Last Modified: Wed, 20 Apr 2022 04:51:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8e5d8f5aab43beaa1f2a2dccd7918da179f8035d75b6b3d8a94b48aeabd9ac3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52476065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7845caecc0b38370a1e314f6477997e93579d93c56527d2e6a7c19f443e17446`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:54:36 GMT
ADD file:abd8aaf2c6d51d5c52c113d618cac82fa11a158ee861ae829b97d1250d0094f1 in / 
# Tue, 29 Mar 2022 00:54:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:54:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f14611b540abb650e196e4ec7510ac9ff0b5355627c1ee4ec6756cfe2fc59c7`  
		Last Modified: Tue, 29 Mar 2022 01:10:56 GMT  
		Size: 52.5 MB (52475840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f270a7d4cc6fc1c73aefd06c8ca8fb319fee0c27db0ce11b3b92027def3fd3d`  
		Last Modified: Tue, 29 Mar 2022 01:11:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fd19f8df3cf4ddd3be30a1b83a267755e8f7a7d2600f5ba2501c986f0576cfc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50134068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7720b9e200b6e69eea4690a4ecff20decdaf47496c1634311ec6ad3a2ca07696`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:22:57 GMT
ADD file:fec28b71de25ce3cf786a79457d6ee9659ae8ac861ecdd680d533c0b664045ca in / 
# Tue, 29 Mar 2022 02:22:58 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 02:23:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:192d4a3a853ea3cdc45d1b46a62cfe119b61b61c9e93ee197c9314032f7fa367`  
		Last Modified: Tue, 29 Mar 2022 02:39:33 GMT  
		Size: 50.1 MB (50133844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cb9419849c842448b21788e55d9cd1b3987376b201e32526e9797cd343a1aa`  
		Last Modified: Tue, 29 Mar 2022 02:39:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fafc23ff1c9860f1757010c16c774cea89c1456f81f9ba000f667f2f2e4a5e54
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53633323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607729f0e0eb8fc21b82823c7c5f3dcc60b24b2dc03c551a751f7b965cdb900e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:30:56 GMT
ADD file:9cb2ef4274be4c1a318ca57c12ca95f467f143eca0bac4c199e2a86f11c10eb9 in / 
# Wed, 20 Apr 2022 04:30:56 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 04:31:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f9d085fb4027d698e9010339730647a2cafcd6b562f259def78de7b561267965`  
		Last Modified: Wed, 20 Apr 2022 04:39:00 GMT  
		Size: 53.6 MB (53633103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763140a5f75386d34014d2975b6f1f53443a8cd19a9c507901afd8ea9aeee9fd`  
		Last Modified: Wed, 20 Apr 2022 04:39:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:34ed146997c107da028402e430eb825495304e0eb83bca9808fc9dd55f87371a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55940857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ed4a7d440ebf900accdcdeca00e9ce3b089497c09491ce563e6e450db95d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:45 GMT
ADD file:79f3d24ec2b208547d39927a0d3e973fd4d1bdb5926511538937943162e48c18 in / 
# Tue, 29 Mar 2022 00:43:46 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:43:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:288ae49939b3ef190048eb92d2e9d77f91b51f9527a30d3df39de493fb27083b`  
		Last Modified: Tue, 29 Mar 2022 00:52:25 GMT  
		Size: 55.9 MB (55940633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41132ee77a302b1cd51712b81b38a91107490d75b96441fecc1ffb25087f7126`  
		Last Modified: Tue, 29 Mar 2022 00:52:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4deb166e82551aab1b3db3af4fdfc1a17ea0444c80e6b6074d1ece9f78638a8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53199555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d6948bbcc454f8859ea7e1db3a470670a78e85161d36771329bbdfaa456d81`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:46:21 GMT
ADD file:0fbef85df7c69585e70b9596838509ae1c00562f24fa354eb32e872202dfa7d6 in / 
# Tue, 29 Mar 2022 07:46:26 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:46:36 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0fb4a12948a42065e860c13e45b3238ccb73f0c66e8c6cc4ad8b23ba7879f522`  
		Last Modified: Tue, 29 Mar 2022 07:57:30 GMT  
		Size: 53.2 MB (53199330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79dad7ad6060aae57a9d550ef733aa04579b3644ccf436f534f6a8f45fd7284`  
		Last Modified: Tue, 29 Mar 2022 07:57:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:02ca5404c1cb90e5f9b84c5a202ecb44b9e8912a78b0b2130363b4051f385f16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58835153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dc20fd47942b38238b1805a56487c21a5ab441f1a3bdc2e3225a94c21ea436`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:49 GMT
ADD file:9c5677819d8db26be48d5a239294edffce512138718e8e00b86d19046a2a3e49 in / 
# Tue, 29 Mar 2022 00:24:53 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:25:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3c64acf2aaabe9cf36d9fa51d66be21a1c381ca1dc4f15ab569a6794b655bb83`  
		Last Modified: Tue, 29 Mar 2022 00:38:37 GMT  
		Size: 58.8 MB (58834929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa75a73b6b790a733dd47ef58a664b685fbbc2ee0f38eb2cae2907a354462afb`  
		Last Modified: Tue, 29 Mar 2022 00:38:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:94265c31f7ee6c66e8103d7a12ea39b8fa07718341345d34b5366dabf55f23fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53210356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e324595a3c0e72f8865102f07aed330dd1f7e367c3277340dfd8c1d804239b19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:28 GMT
ADD file:9c8109e8edaf499eeaac7353760c4169d5b14f48c6cacf6000ec0bac50662266 in / 
# Tue, 29 Mar 2022 00:53:31 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:53:38 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:08559879f8bc797024b3fd393eeac6e78025b622e187a7d30c39f9c6230a3cf4`  
		Last Modified: Tue, 29 Mar 2022 01:20:43 GMT  
		Size: 53.2 MB (53210134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0866d3cada0a38f97408f15f997304672ab3b3677f1e9a07433cfdcf9b1a090`  
		Last Modified: Tue, 29 Mar 2022 01:21:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
