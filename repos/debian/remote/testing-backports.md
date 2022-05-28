## `debian:testing-backports`

```console
$ docker pull debian@sha256:d492694f5e7d2ec53d567b7e3073e5c2a52a43a9f81148078d2ebb92796ea572
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
$ docker pull debian@sha256:677de9f2ef1d43f8d93b75b5d14f8d07f2a16edcc961c58256eab4d714694b34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52944708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c0814c963b217a22ce6b70dcca2577f0470417239bbcac86427af77b6cee05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:22:25 GMT
ADD file:281fd73718c53fc59c1102594f7f1e885886403980fd1b7ca7f5c96a97f4332b in / 
# Wed, 11 May 2022 01:22:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:28 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bb3baf4f16d6f037d735d8dffacf29da8066f489b61bffeceeda9f6403aadeb6`  
		Last Modified: Wed, 11 May 2022 01:29:18 GMT  
		Size: 52.9 MB (52944486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940979c6fab92898d082563010fb382d0b1457cd5d8a3b4e2d0240ca7f3a6320`  
		Last Modified: Wed, 11 May 2022 01:29:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:00e270b63d602b8e07db5eaa7a45c6851249f5076a82f32ae9089052aed255e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50737668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2974c48c2c4bbae176be7a26dfd0e5dfef698104042716efd661ea5e4996484`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:56:34 GMT
ADD file:335e5d916082436e2ae0ecb67efce63f983ef63c07c914bbe30f28b6978345e1 in / 
# Wed, 11 May 2022 00:56:35 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:56:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:01866b086b60cccf118ed98e37131a03befcd6038523a4965798d5958be62b2d`  
		Last Modified: Wed, 11 May 2022 01:14:30 GMT  
		Size: 50.7 MB (50737447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1245b9c44cf9f29296f26bc7f68ba0f5eda840bb995aebc768da9d7159e21f0d`  
		Last Modified: Wed, 11 May 2022 01:14:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c7718476870a96a4e21a4d01aec1360770d9c822419259c0315bc40c261d265a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48476256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fd6f9b0b5e09c67d81bd50d9482a424b7ca9a8d0bc672ed3c3a11b07064fa5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:55:38 GMT
ADD file:e892137ccc12253ff7fe503eaa143fdc1532681748a46013e48aa30f0cebc35d in / 
# Wed, 11 May 2022 01:55:39 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:55:52 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:50ac47297fc08924760b8c77903f950294c9eedeffddb645affb4662a283a04a`  
		Last Modified: Wed, 11 May 2022 02:12:41 GMT  
		Size: 48.5 MB (48476034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff70124eb62b6c2d232c5672794f904f655b3da75ac318429ea28108448beeec`  
		Last Modified: Wed, 11 May 2022 02:12:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b29176c47112ec1fba9289ab151aba958a6d3e698f1cc88bb285dbc66711a733
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52043058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950a47f33636412fa6a179b1de08a035c7cb5195eb34741cb2abf700bd965d75`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:11 GMT
ADD file:936ad327dc97009e77bbb7d1d1874d55f3d251b8a641269356e5caabe860a8cf in / 
# Sat, 28 May 2022 00:43:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:75fd77c03641c04273179a599ef54dea600d22da8b30160003b50fa90a397f43`  
		Last Modified: Sat, 28 May 2022 00:52:12 GMT  
		Size: 52.0 MB (52042837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d8952cace7dcdd6d22b67b71e408cb84aa441d311a79d1b659efb863a8a511`  
		Last Modified: Sat, 28 May 2022 00:52:22 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:2ae20ab0c719dd94075e09656f3d4f70c7725c44d3cdb8d5dfdf82fe3f13ed8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53948783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66072ecee508b09e5ec57f70131493d1f1bda79ce51fe984f99d5336c1b10f3b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:18 GMT
ADD file:ab2acf453e0f28f32503a483bbda0e5e5d09513add50fe39f591bf33810a4be7 in / 
# Sat, 28 May 2022 00:42:19 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:42:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fd2231baceb33fbf6629c80839b9f9e3d4d4c20d0adb42b699791bd018f52c4c`  
		Last Modified: Sat, 28 May 2022 00:51:24 GMT  
		Size: 53.9 MB (53948561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e976480a8fa0fa79af4d6edecc9226f5d87d94b720993356bd214da6566c34e`  
		Last Modified: Sat, 28 May 2022 00:51:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2c00d1a08cc332199b8aa05ecf5fede7f24e5f935e3ddc452c1642d27403b613
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52067186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc04d57d474b720f948d354ac12076dcaa279e47c03b9c2fe37d46f9370b3d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:28:28 GMT
ADD file:37fda70781a49d4154509c2895569ee7a38d574f366495db43ec4f4d55639795 in / 
# Wed, 11 May 2022 02:28:33 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:28:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7488653e85c57f013670e78d75d507ae30e3fbe8942874871a14bf56ec6ec160`  
		Last Modified: Wed, 11 May 2022 02:39:21 GMT  
		Size: 52.1 MB (52066962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160a120f6152b2b6d53a64e6620f1b7e6ccab304230009c0f8d2ed4a17657c05`  
		Last Modified: Wed, 11 May 2022 02:39:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ca29a19b25e38142042896509435f4e572910301300545c7d1fc69419073274e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57150795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89059d2da2e0e437b2edce152dacd5c0282d0f3efc9646bf7a7834e3986b55be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:36:50 GMT
ADD file:8824d2629598c6f5c70db2488623b2873dd8496f2765f9a16b931e62ebe1d2ca in / 
# Wed, 11 May 2022 01:36:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:37:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f847dd78355ff75879dd0f1ed43325b24a1351e2cb0038f2cf60d5e061b5b866`  
		Last Modified: Wed, 11 May 2022 01:46:57 GMT  
		Size: 57.2 MB (57150570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4d191f38db43087a2ff949abdee0615ea5a9109676284fbf8ee24d58af786a`  
		Last Modified: Wed, 11 May 2022 01:47:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:b543eb0a4ae55dc75224231cf2452658471b34c9b0a0a93aaa8c2255e424a0d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51490491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea2b9a1a4faa45af4ccd1fa6dec287de4c597e3f302da04f20edeeadc3f66c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:45:48 GMT
ADD file:430aae00218790907570f298b5f5c4e47453d9297090e8d006c5169e5e9ee56f in / 
# Sat, 28 May 2022 00:45:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:45:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:33ada038def02ed9f3f9762c43feeaf3a66329f979154e6d3dca5e1ac4f04893`  
		Last Modified: Sat, 28 May 2022 00:51:52 GMT  
		Size: 51.5 MB (51490267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1406700fa9997a58c70749575703dc4eb92cff73a6f738556df67a17ae55ca76`  
		Last Modified: Sat, 28 May 2022 00:51:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
