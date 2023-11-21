## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:e4fb98e06ef027abc0acff1b0b74c6d1604b119246d97710326ed89e8c7477a8
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:bebd18bdf6c6fb1392e424f8b8ab830d69b3d09a41af3bd74773c93545372678
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55058322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6988002241c131bf5fd8a90ba323a99dd0eada326e0d1f5911c22e6c2139f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:06 GMT
ADD file:30b9dcfcd946b137141d7c5c2edcb9d0817dbdd07b9a6951031ee071ca2e2894 in / 
# Wed, 01 Nov 2023 00:22:06 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:22:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41bc806f354b99a3f6009571ba6c37f6532fd5828fa506fd50fced3b011f35b5`  
		Last Modified: Wed, 01 Nov 2023 00:27:52 GMT  
		Size: 55.1 MB (55058095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cad93d1666898656190584faf83c3f1f4048c7f369d01c5611d678be153ea67`  
		Last Modified: Wed, 01 Nov 2023 00:28:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b15f5167803c12605c851251fa597fa5e0520e58a95c72feaad5693b3739da64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52563570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3adf2692b8bdaeea1dc119c1892725cdfb14e475918822364bfcf6ebd69172`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:48:55 GMT
ADD file:1b25954e3f7e884e4864229cfe1914d0764b988651771aab6c209fb30329b9b7 in / 
# Wed, 01 Nov 2023 00:48:55 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:48:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b5921cf78dc2c4130c15cead6b51a4c0a231734386ee14152e0604822975b7bb`  
		Last Modified: Wed, 01 Nov 2023 00:52:34 GMT  
		Size: 52.6 MB (52563345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea8b9814a49cd5665380d445b3742295130d268589216e8335961a54a0ccd6`  
		Last Modified: Wed, 01 Nov 2023 00:52:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2b9a2671906236fe840a37ee9b3399ebc9f00c53f59e3c90254e2192825c8388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4584db1db5ad37e293c8276127c0c200811dfdfdfd386837ad1da39e080b00cd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:58:49 GMT
ADD file:58f6f7f29ceab3d3aa9804f9f3b476f110673cbbc0ebd7d72d01e8b8089c585a in / 
# Tue, 21 Nov 2023 03:58:49 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:58:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9be29f3594315c42bcae957a357b11b71d9dd666d2deb5c9e9d10f669800d5ea`  
		Last Modified: Tue, 21 Nov 2023 04:04:19 GMT  
		Size: 50.2 MB (50215655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667c9c92f823a45a648189d0c653102db88bf427e2ee58d8abbbb1d0ae63cecb`  
		Last Modified: Tue, 21 Nov 2023 04:04:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b4e66de73650741994fa0a96866507ba78ff61ff62916ae88dc3e3e74b052d23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53707947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef88b7ede14f1b02981a25143b093eac9423fa6eb3b7e832fd16ccc1491fa98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:31 GMT
ADD file:b30a343af65c645e74d2553af6919092522cdc54756aba1d0adbfbd0d7d5d4cf in / 
# Wed, 01 Nov 2023 00:40:31 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb543055d2e84a942c853542b1080a71cdc776d4f28c8eafbf2e4fa1ef2759ce`  
		Last Modified: Wed, 01 Nov 2023 00:45:14 GMT  
		Size: 53.7 MB (53707722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7685f69d05bfee11937fb0a53aeb56e2868043a8847529bddf0b7b741acc33aa`  
		Last Modified: Wed, 01 Nov 2023 00:45:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:a7fac79df0ac1fa910ddd161aed8ac6020267c8d257e452debba79ba5f4e7543
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63882ea30b2f443542a249f345329134ad5c848a10f8bf269df53b3e752ceefb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:40:10 GMT
ADD file:77803db15f16eda18ab7d7f4938a7e3908e93ab76d5d1bbf37717109ac6b788e in / 
# Wed, 01 Nov 2023 00:40:11 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:40:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:938bf4cb5b04bc49da2a0995405b27fa3d635d40e5050d49a03b97dd9f387dc0`  
		Last Modified: Wed, 01 Nov 2023 00:46:01 GMT  
		Size: 56.0 MB (56046264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385dd4c5485402b3619815b7ecf8d0dc448e06abf08899ed38b379885bcb687e`  
		Last Modified: Wed, 01 Nov 2023 00:46:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:05abf1f379cd5f45399a0fd1ed99ada1e9a5e6a638e5e95cd2a0591d8f75e435
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd31a12e7921faeb73b8175d183cd8a8485bedd5e9651ca9c31b8bde9e12adca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:11:38 GMT
ADD file:343c03861fde637104bb6e0f9fe190e9a9241fd256235e98d22b6f3ecd50f018 in / 
# Tue, 21 Nov 2023 04:11:43 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:11:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01df819effd0b4438405ff3eccbb77832cee643b4bb690c24074c16314ec0db7`  
		Last Modified: Tue, 21 Nov 2023 04:22:45 GMT  
		Size: 53.3 MB (53289161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b451372d0365100d5e075c3e7955e886215372a4feaa1cb6c4963e8b0c9ceb3`  
		Last Modified: Tue, 21 Nov 2023 04:22:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:723a6e384bddf0b80c9537db3363e11c06e8aea5eecd8fccedbbaa1ce98e202f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e2807368a47550ead81037d908248b81ea9471d56f5047994f9df484443b93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:21 GMT
ADD file:eaa1db56a0b20b30b76d393ee69a4e7481d866f926db0a129dd2e15db7ffabed in / 
# Wed, 01 Nov 2023 00:22:24 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:22:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d17f706dc2e5f6d2c2df15c6a255acc0283efa6f95faedb0621adf8af6827bf`  
		Last Modified: Wed, 01 Nov 2023 00:27:20 GMT  
		Size: 58.9 MB (58929501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0346bb2356966bbb2c864a3a56628cee0bc4ac0758bcc8a9bd9f0a3016c79438`  
		Last Modified: Wed, 01 Nov 2023 00:27:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:d71c04398a7ed55593b25129bb824badea378469a9781e48e78596c1892ea6b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd48ed742efb571ca31c72527edff0f617c1f5b0f67b11c6f920256899b04551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:43:25 GMT
ADD file:b1afffd188d6c25120678ed8b7098eda71f2329df66a78b775eb68ae0a92185b in / 
# Wed, 01 Nov 2023 00:43:32 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:43:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:475f1acad7ba07c7798b8283e8092afb7948958ab94232bb3ff92fc71ca38bc6`  
		Last Modified: Wed, 01 Nov 2023 00:48:56 GMT  
		Size: 53.3 MB (53296585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb02d443259172830a0f2b3ffa919520e93b30b80f9095d9163f7c9c99e4c86`  
		Last Modified: Wed, 01 Nov 2023 00:49:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
