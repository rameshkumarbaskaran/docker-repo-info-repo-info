## `debian:buster-backports`

```console
$ docker pull debian@sha256:7439a65321f1c373d372e485b6b044a477bbd1710af86cf806a6457838c91ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:26a606c011d44136a2960d367c232be6227ee6b4a87106d6cac3dc9f559ec395
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50497824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed18fcd49a5c98840283476d5f7884fc71c257ac00a31d7e19adc29fa3eae53`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:23 GMT
ADD file:d9c3e291731c1f06d615709ebc665a41f6d6355607d87ae00768e3be4b330bed in / 
# Thu, 07 Sep 2023 00:21:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:21:28 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:311da6c465ea1576925360eba391bcd32dece9be95960a0bc9ffcb25fe712017`  
		Last Modified: Thu, 07 Sep 2023 00:26:22 GMT  
		Size: 50.5 MB (50497598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035ead669a593978375a90546ea8b82dc83afd38965b870ac9928db9cca0c988`  
		Last Modified: Thu, 07 Sep 2023 00:26:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:78c86ca7e392731017dab4e721da3d1fe4403e4c15f9e9f39805ddd7b722cca2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad61c68827529faa7cf644d0fabe588715b448bf833e61a68de505a0eee0ff2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:42 GMT
ADD file:9ad3ed36bade2e2cd71bd8f66dc47946e90d205f1846692ae9c240560758b4f4 in / 
# Wed, 16 Aug 2023 00:17:43 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:17:45 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ed63aeb0ff951576d398ae0e8de7a2dc582157c60523055321f47ef26ce88e00`  
		Last Modified: Wed, 16 Aug 2023 00:22:28 GMT  
		Size: 46.0 MB (45966229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039b059e7a5a1927d1ecefa082e44f93fca431a863f62d121f7a11e49dfae8ea`  
		Last Modified: Wed, 16 Aug 2023 00:22:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:5422ba891ca0aa6a2124429e9cbc4bb5c9406097861cf83b2744d7a09867b9a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b6f3d7d6116c12cbab27fd3395b9106507995bca1dcc7cfc90fafb140f10ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:18 GMT
ADD file:366546a703fa234d38591d2a54f10fbced83cc0e407775ad31751f0111c348c8 in / 
# Tue, 15 Aug 2023 23:40:18 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:40:21 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:745797452665e0b4d6f5d0f9b05ae67a86bccfea4ec3a2cf7c6dd89cbfafdd37`  
		Last Modified: Tue, 15 Aug 2023 23:44:16 GMT  
		Size: 49.3 MB (49290964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bb2112ab93a3ca3073fea05e09c61383d1c06fb7b5440677020a0dc273fe99`  
		Last Modified: Tue, 15 Aug 2023 23:44:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:8447a872370f08a5670e392f97732f16882891ccd9ded231504c542f279982fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc075613b014d7620825cf2cc2b71eef647d0f94547a289f58d00f5cca3e9477`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:39:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc590a6fb1b46b620ed8a7555de264489a7d5875f527ba8ab2ab21e677fb1da4`  
		Last Modified: Tue, 15 Aug 2023 23:44:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
