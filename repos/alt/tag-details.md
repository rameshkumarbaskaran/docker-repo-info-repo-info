<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p9`](#altp9)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:91fb07c6ffa050c533c8815d0e6a663238422f5f0d1f1d46c198babfd4fbc625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:83f8136ab6e2b1383d1ee43b5991793e82b610eea65528d119c4aa131c03662d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43934590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e6d6a199f6749e553a9ae97a432c340baae824198658533f486c63376bb7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:20:10 GMT
ADD file:f1220163c72ab8047c3c533f2eaa5a74a08c1da089d78a351b0fb8eda5dd4792 in / 
# Tue, 26 Sep 2023 00:20:11 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:20:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7f9ddb17769baac9176302cefb1b0c74d945d68f11f54a4204fa94eff7e8b4ac`  
		Last Modified: Tue, 26 Sep 2023 00:20:46 GMT  
		Size: 43.9 MB (43934399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7be41dae8bd019a921685a2e5f2adb4bbde52e414a485787266e8061c6c83c6`  
		Last Modified: Tue, 26 Sep 2023 00:20:40 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm variant v7

```console
$ docker pull alt@sha256:1c59e77d911e717d6730df713cba11241fb78a79eac162b22177a91bf3af53f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40169888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a077c79aeeba81e9624572e8794da9b9a3eb9748a6d15810b9c9979f74982d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:57:22 GMT
ADD file:a311881d32f36eb465f0c4d861c96e900a3a670e9a2d6bc5dcfb56207777be15 in / 
# Tue, 26 Sep 2023 00:57:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:57:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00a9dbf753a7bd9a8c0c19b8aa1dbba1d03ebc9fdf1a1fc365ceb857593050ca`  
		Last Modified: Tue, 26 Sep 2023 00:58:00 GMT  
		Size: 40.2 MB (40169695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ddaa2053142cb3f63cfdb596357a1bd13c264738bfa4550740caddc1edd6ba`  
		Last Modified: Tue, 26 Sep 2023 00:57:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:bb47bf55b4326fdc17b1790a36fa6f6909e70072835f3f889fcd4697176bac8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433bb2692d853baa1540c1e1dd36e703e63b37e45a238e29efc6c3ce30c633dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:19 GMT
ADD file:cf3d15a8c8367f7b11f2f919df70622531c4e505186ac74cef25fd6278435be6 in / 
# Tue, 26 Sep 2023 00:39:20 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:18b7af9e9dc5b8f6137f54a934e5e96fcb854eeae947176613644d15a3d47def`  
		Last Modified: Tue, 26 Sep 2023 00:39:46 GMT  
		Size: 43.2 MB (43166192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c420f2edbfee1eae121f2064b6216ab5194df3d888003c6eb414791f0be95c`  
		Last Modified: Tue, 26 Sep 2023 00:39:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:634f0b6f91dec963463c1efe7d049b7d1d1a2cb96c687f0a89b58dc98a577820
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44616420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a676c0c2ea30a8399c558e02c1471770db47c72ea7e477bda27d444f4bd73b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:38:50 GMT
ADD file:27876d998eb510e342fb882d7f52ffc853e2c3f8be4bb5fc06dc849bc771b533 in / 
# Tue, 26 Sep 2023 00:38:53 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:38:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53ad182393cc445f9cc01f60fe83e0e32a713ae008eed39659dd006ea63013a6`  
		Last Modified: Tue, 26 Sep 2023 00:39:33 GMT  
		Size: 44.6 MB (44616229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a017a4d6457905cb693950d9bb3b31b886c943a4d0c2f0d0dc9699fdb854af20`  
		Last Modified: Tue, 26 Sep 2023 00:39:23 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:latest` - linux; ppc64le

```console
$ docker pull alt@sha256:da9c4ceb513de3babae6868eadefc252e3b0f73171a96204f9e374b43acdcef0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b76df1382fcf0d198810a312588be00843a4b01ed11cfa25ca4f24c3aaa717f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:16:32 GMT
ADD file:21a0ec565025314f699a3097125c75f2f91355d7b307f51af72c07704d376c18 in / 
# Tue, 26 Sep 2023 00:16:38 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:16:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03d2e543e29e2128160b5eda1e443f1cee3eeb7ecd5fc3ab426836da7507cf04`  
		Last Modified: Tue, 26 Sep 2023 00:17:40 GMT  
		Size: 46.9 MB (46883843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c56b5f9faedca40968d8ed71a8164577966f9a18ce2ef377efbdad3dd3ea55`  
		Last Modified: Tue, 26 Sep 2023 00:17:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:p10`

```console
$ docker pull alt@sha256:91fb07c6ffa050c533c8815d0e6a663238422f5f0d1f1d46c198babfd4fbc625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:p10` - linux; amd64

```console
$ docker pull alt@sha256:83f8136ab6e2b1383d1ee43b5991793e82b610eea65528d119c4aa131c03662d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43934590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e6d6a199f6749e553a9ae97a432c340baae824198658533f486c63376bb7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:20:10 GMT
ADD file:f1220163c72ab8047c3c533f2eaa5a74a08c1da089d78a351b0fb8eda5dd4792 in / 
# Tue, 26 Sep 2023 00:20:11 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:20:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7f9ddb17769baac9176302cefb1b0c74d945d68f11f54a4204fa94eff7e8b4ac`  
		Last Modified: Tue, 26 Sep 2023 00:20:46 GMT  
		Size: 43.9 MB (43934399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7be41dae8bd019a921685a2e5f2adb4bbde52e414a485787266e8061c6c83c6`  
		Last Modified: Tue, 26 Sep 2023 00:20:40 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; arm variant v7

```console
$ docker pull alt@sha256:1c59e77d911e717d6730df713cba11241fb78a79eac162b22177a91bf3af53f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40169888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a077c79aeeba81e9624572e8794da9b9a3eb9748a6d15810b9c9979f74982d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:57:22 GMT
ADD file:a311881d32f36eb465f0c4d861c96e900a3a670e9a2d6bc5dcfb56207777be15 in / 
# Tue, 26 Sep 2023 00:57:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:57:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:00a9dbf753a7bd9a8c0c19b8aa1dbba1d03ebc9fdf1a1fc365ceb857593050ca`  
		Last Modified: Tue, 26 Sep 2023 00:58:00 GMT  
		Size: 40.2 MB (40169695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ddaa2053142cb3f63cfdb596357a1bd13c264738bfa4550740caddc1edd6ba`  
		Last Modified: Tue, 26 Sep 2023 00:57:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:bb47bf55b4326fdc17b1790a36fa6f6909e70072835f3f889fcd4697176bac8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43166383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433bb2692d853baa1540c1e1dd36e703e63b37e45a238e29efc6c3ce30c633dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:19 GMT
ADD file:cf3d15a8c8367f7b11f2f919df70622531c4e505186ac74cef25fd6278435be6 in / 
# Tue, 26 Sep 2023 00:39:20 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:18b7af9e9dc5b8f6137f54a934e5e96fcb854eeae947176613644d15a3d47def`  
		Last Modified: Tue, 26 Sep 2023 00:39:46 GMT  
		Size: 43.2 MB (43166192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c420f2edbfee1eae121f2064b6216ab5194df3d888003c6eb414791f0be95c`  
		Last Modified: Tue, 26 Sep 2023 00:39:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:634f0b6f91dec963463c1efe7d049b7d1d1a2cb96c687f0a89b58dc98a577820
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44616420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a676c0c2ea30a8399c558e02c1471770db47c72ea7e477bda27d444f4bd73b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:38:50 GMT
ADD file:27876d998eb510e342fb882d7f52ffc853e2c3f8be4bb5fc06dc849bc771b533 in / 
# Tue, 26 Sep 2023 00:38:53 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:38:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:53ad182393cc445f9cc01f60fe83e0e32a713ae008eed39659dd006ea63013a6`  
		Last Modified: Tue, 26 Sep 2023 00:39:33 GMT  
		Size: 44.6 MB (44616229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a017a4d6457905cb693950d9bb3b31b886c943a4d0c2f0d0dc9699fdb854af20`  
		Last Modified: Tue, 26 Sep 2023 00:39:23 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p10` - linux; ppc64le

```console
$ docker pull alt@sha256:da9c4ceb513de3babae6868eadefc252e3b0f73171a96204f9e374b43acdcef0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b76df1382fcf0d198810a312588be00843a4b01ed11cfa25ca4f24c3aaa717f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:16:32 GMT
ADD file:21a0ec565025314f699a3097125c75f2f91355d7b307f51af72c07704d376c18 in / 
# Tue, 26 Sep 2023 00:16:38 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:16:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03d2e543e29e2128160b5eda1e443f1cee3eeb7ecd5fc3ab426836da7507cf04`  
		Last Modified: Tue, 26 Sep 2023 00:17:40 GMT  
		Size: 46.9 MB (46883843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c56b5f9faedca40968d8ed71a8164577966f9a18ce2ef377efbdad3dd3ea55`  
		Last Modified: Tue, 26 Sep 2023 00:17:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `alt:p9`

```console
$ docker pull alt@sha256:6e22e9d79d1e1329e9d4817a4f03fbf9bc651a0a3f1691c751031379722c29bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:p9` - linux; amd64

```console
$ docker pull alt@sha256:f221359928d06fbd44e68a41d6e350d3bc8ed9e128bf11f720e9bc9ed7453392
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43153381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358e918635f9514343d7250ab41954e0d679ed9deb112e0f204c4a65cd08cb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:20:20 GMT
ADD file:d8242110452bcf5ddab4588a7f08e599d097a1a7c895878121f4f05ce7b98cc5 in / 
# Tue, 26 Sep 2023 00:20:21 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:20:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a71abbdd5e26300bfc77703fc0298a0dd33562d0d2fa0170006aaefc80249f1f`  
		Last Modified: Tue, 26 Sep 2023 00:21:01 GMT  
		Size: 43.2 MB (43153190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c413b96361246a5033686233d189b6f4553f8797382550a1586bb1927427288`  
		Last Modified: Tue, 26 Sep 2023 00:20:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; arm variant v7

```console
$ docker pull alt@sha256:12ae5d23a0959833292fe7c45d5636254421b2862636463ac3c7de53b2b700c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38635105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06e79101beac990e5fa088fdaad4116e132bde82ff3d5bfdf4f5f2d87055ac6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Mar 2023 16:13:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:57:33 GMT
ADD file:50b42ecb394014f2e3cb8098382fa5611a228210496bf4c8c5a6c3135b658c50 in / 
# Tue, 26 Sep 2023 00:57:35 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:57:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:69277cf044c1becb541c51054ea4e419f530f20bb8839f83163f9d4f590cc674`  
		Last Modified: Tue, 26 Sep 2023 00:58:14 GMT  
		Size: 38.6 MB (38634913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49baa735343f2f32a662eea00106b89e744805f2768449de5844aa919106004e`  
		Last Modified: Tue, 26 Sep 2023 00:58:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:f27d9e4e6a8596ab300613684df7d3fae8dc89ee3d16b78de3f94bc841b7660c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41947315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b1b9226a6f580e989dd3d2cb9eefc5461f3221f00182e0e0bc3f7e964c1a35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:26 GMT
ADD file:ce5d1f47adde45854462ae072d9cf9bb93eabc5e84a8c7206aa646dce73dd243 in / 
# Tue, 26 Sep 2023 00:39:27 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f12633f1b989acb82780f56e4b2dd7571242a5862224d94d1b4ef41c51403bde`  
		Last Modified: Tue, 26 Sep 2023 00:40:01 GMT  
		Size: 41.9 MB (41947125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327fc42bf1c6d792ae368f63a11f606819cdb57aefdde8c3a531f098d5b5b59`  
		Last Modified: Tue, 26 Sep 2023 00:39:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; 386

```console
$ docker pull alt@sha256:520bc632e10f7a16cb0b9d505939b1d9975f5a368e2728412819cc45ff41ae33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43289880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f30f1536732b1be662aec8e7de070df630e9fc24b9daffd8d14d9e49302d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:39:04 GMT
ADD file:c235c6b804723addec4fffbc791c26c3b42437c836e2dd57c235a057a13f101e in / 
# Tue, 26 Sep 2023 00:39:05 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:39:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5a059694dc47ce9a1816aac59118833bce316d8cc8241bea58ee3bb227685fc9`  
		Last Modified: Tue, 26 Sep 2023 00:39:49 GMT  
		Size: 43.3 MB (43289689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111454471b31627c091a876e28ba9015e00448ea2692adacdd3c537600123649`  
		Last Modified: Tue, 26 Sep 2023 00:39:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:p9` - linux; ppc64le

```console
$ docker pull alt@sha256:bab06b7a9a7566cdc23011b5925d0175d765421c04be8a645dab0bd7b4070255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46885044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b600fe3a3fb201d584e18534e93b2439340007a132153fb0d5c78537ca9a0ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Sep 2023 00:16:52 GMT
ADD file:683d80ddf5044790ee282736c9f246568be2ed3990241a8977d55eae1bfbc511 in / 
# Tue, 26 Sep 2023 00:16:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Sep 2023 00:16:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ff179bec0aadb6a0ffd3675589552330df52bed4aa2f97c485cd66fe87f9a93`  
		Last Modified: Tue, 26 Sep 2023 00:18:02 GMT  
		Size: 46.9 MB (46884852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b59576dcf664fc874bdb1af5e4e689f3eeb0e04c871b4bd41107754b79a368`  
		Last Modified: Tue, 26 Sep 2023 00:17:50 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
