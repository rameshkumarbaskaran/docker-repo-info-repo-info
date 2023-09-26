## `alt:sisyphus`

```console
$ docker pull alt@sha256:91fb25415cb9d252b5fd19c735e0f0a87bc0d181a263e8e1b3d1ad14c40ee969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:aa52ebd4ac57aef3cdadca1c5f2d8ae88baad0ceef71823fb984f392b9acf06c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40570107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c017e88c3162ba53400289e51b0b1cffaa4b96d59b78416ce6937c5a0a51663`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:20:29 GMT
ADD file:e3d12e982b2f94e23ff65300398bce97909fae0c3107acd5c48426d841f876ff in / 
# Tue, 26 Sep 2023 00:20:30 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:20:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22cd25f8be30cea71c63981ea10feee347a1e9fc72f3a909dc6da930ec2bc504`  
		Last Modified: Tue, 26 Sep 2023 00:21:14 GMT  
		Size: 40.6 MB (40569917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05024898935c069b9731b620ebd2dc7862566cd856467fcbf922c17dacc6ef49`  
		Last Modified: Tue, 26 Sep 2023 00:21:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm variant v7

```console
$ docker pull alt@sha256:e4d539a946e491e59e694e6e1fca143fd06a1b8ca0a8984d87361a8ba5b6ff18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37312895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b205692a1f02689e0983b0a7a6b7285b9a724218a294407c939177a01bc81e25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:57:42 GMT
ADD file:1b64931dfd1aa7caa0fa05126c9578f6710f7e6734e3136a6e615f32c478746f in / 
# Tue, 26 Sep 2023 00:57:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:57:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a55ed04bef5fede8ad6756a1ec9e25b26964f85b70b30fea44027d0f17d27307`  
		Last Modified: Tue, 26 Sep 2023 00:58:26 GMT  
		Size: 37.3 MB (37312704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c609fe762561cc5a661b9966588b1e57b85dfde7a652105dbb51fad294f6b658`  
		Last Modified: Tue, 26 Sep 2023 00:58:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:7bc6b08980128f32221e95001208944a661c0e8214ee83e9d45b0ec16ba17246
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2316614d825c37cfb45bdc4fef3eeca3f9d825283210d74992dd7294520bf335`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:33 GMT
ADD file:543df42528f7b362bf51455bc35cefc0a259f665e35c959bda18eb9dfda3314a in / 
# Tue, 26 Sep 2023 00:39:33 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7f4458d1e85ce1e128db11d40603a0d49a4e76012648c255eaf26a3600a42b0`  
		Last Modified: Tue, 26 Sep 2023 00:40:14 GMT  
		Size: 39.2 MB (39226517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9dd65dd5a33db25a1fcd5b66c5bc45b15313eb181e6a5d5afdd68f2749f6f8`  
		Last Modified: Tue, 26 Sep 2023 00:40:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:d617039e3809907755cb19d543a4f472f8e905d2fae6eff6cdd36eefa11c6dee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40702475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300d39ac6f7431a24c271330f93101f13029323985c6aa4b0001a011f3ef09c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:15 GMT
ADD file:1559defa544d370bbb68358c687c080bd3538b387fcafb401135ad1904726ea8 in / 
# Tue, 26 Sep 2023 00:39:16 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b4877b6a639d6c8ee34b196f6fc27ee8e11fb3bd1f038bfdc4d8189284649893`  
		Last Modified: Tue, 26 Sep 2023 00:40:05 GMT  
		Size: 40.7 MB (40702285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e8299ef54b083c2177fe487a10d46eec8adab884074fc8bef65cb890f1d0a`  
		Last Modified: Tue, 26 Sep 2023 00:39:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:ecd82e1cbbe68ea2fc535b585cd0a13566c38f3db9e7cfa8f2fd96e7a20676c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42804906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbda21305cd14797cafa9f02c714b7fa691842cd83779c38a702ffab7314a4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:17:10 GMT
ADD file:bbb30f86ba7aa34fe741558299bc6051b46273957b9eaef5fc7adf1828145f94 in / 
# Tue, 26 Sep 2023 00:17:15 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:17:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:35963790a4f89a75f5e8cfe9c08053d3e8fdb7f377517cfb5c40a4cb5bf9de49`  
		Last Modified: Tue, 26 Sep 2023 00:18:20 GMT  
		Size: 42.8 MB (42804713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca5ecb31b7a8acf6d12e461a302ea257dc2396053d92f09b621c487f9c3d748`  
		Last Modified: Tue, 26 Sep 2023 00:18:09 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
