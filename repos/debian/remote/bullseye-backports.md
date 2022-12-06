## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:b8ca66e146f435fab1695c839102b2d3e650ec2eeec7b750840ae1e20b243e26
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:f6714b86161d1aed4e4d33b82be30a890e856725c404ad473b32a3cdb6e1135b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55041566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5469bc2a392ab2540b73bce3d37260859a265987ae4d88e99410a8eee3e0eba9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:41 GMT
ADD file:553d20b03d45305e58cde07e0c259421bba044155ac90b4559e5cc0b69093347 in / 
# Tue, 06 Dec 2022 01:20:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:20:45 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f2f58072e9ed1aa1b0143341c5ee83815c00ce47548309fa240155067ab0e698`  
		Last Modified: Tue, 06 Dec 2022 01:24:48 GMT  
		Size: 55.0 MB (55041342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf5828a979d902a48febc8177aacc67a79ba8120aacae287bea852baced560f`  
		Last Modified: Tue, 06 Dec 2022 01:25:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9fb09e09bc3793aa8519381fd302fd13cb1b27e8140a7f3f2fc723d48c1f22df
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52542520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba215961ef8cf765fd73a485b9e29b89eb01b7a42678ccc379eb55d0f32ba4d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:01 GMT
ADD file:1301cc1a3eec72236eb8cfb02c81a3e956e32a32025a89995435b641e1d9330d in / 
# Tue, 15 Nov 2022 01:49:02 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:49:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0655cdb20ead0094190060645bdf853e9427b58a64f0c7d92ae439b80ca81fdf`  
		Last Modified: Tue, 15 Nov 2022 01:53:55 GMT  
		Size: 52.5 MB (52542295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7646676f8fc5e5c83e9a64c0aaa7289c05d742948e936bc08bc7efa1bd2dca9`  
		Last Modified: Tue, 15 Nov 2022 01:54:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:797f3584d9ec626697449ecd80ac1e69a2d3c01a54b5814e2174fbd0db3f8f88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50207313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a8b8754e8218b2c637773a13fb06218e0f4668bbb6853ac1a80f19b6b86e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:30 GMT
ADD file:72eaf12ec65c98e9cde1654b6adb2b3d19f7d81c13b12801c198f699252b7503 in / 
# Tue, 06 Dec 2022 00:58:31 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 00:58:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:58e27900c24f1f8f5b6b5eacbc073583f2372b58e9f5678dfe171b496b9cd71e`  
		Last Modified: Tue, 06 Dec 2022 01:05:33 GMT  
		Size: 50.2 MB (50207085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7c2b05534a97f44daa31087ab617829c0cdd24887dad490c696fdbaa01474b`  
		Last Modified: Tue, 06 Dec 2022 01:05:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:eb26c00cb1dd88a43de92b36b982dbb80aded5e00c88675c4e88c7381fc6cfdd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1631b56987264ce8b5892505c98b1d3a190fb58b7746e12049cec0b36b772de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff3399ace4b57961bdc4c0a0ad4d7c15c9d337b4ddb27ae2c30f8feeb908eaf`  
		Last Modified: Tue, 15 Nov 2022 01:44:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:8498464b18213f835dde0f525b63a6f2db9467721c35478194b257be29e1312f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56020950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612a9351c8eda6cd19cfa3553677429b62e9220ac939ab63076d658d60412b3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:11 GMT
ADD file:2962b9f6c2d1271d6b4d04e8eaf82fb990726e0593bbe685576851ef47447301 in / 
# Tue, 15 Nov 2022 01:41:11 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:41:19 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9c6907f3cae53506b5149dd6542c3e51b750fdf5adbe19d7e949974888503c1e`  
		Last Modified: Tue, 15 Nov 2022 01:46:36 GMT  
		Size: 56.0 MB (56020725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747b7732bdd92395272c7cbd9bfa752720bc45ecc10fff9e56a4e840fe2a0bd0`  
		Last Modified: Tue, 15 Nov 2022 01:46:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:268c7c906c3a072e7f5ff25c9bc754042f50a134a6353692818ebe8a622ae80c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53260590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20f608d681f3a45c16537ac518f1ffa6534b239749aed47cd0911be7b8191c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:13:08 GMT
ADD file:65d4d16b7aebde0e13c3de84312e229b51904d161ba4ee74a427b6fe7c6dc6c9 in / 
# Tue, 15 Nov 2022 04:13:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:13:22 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec4356bce7812bc703a76dd14989fc14f03913b2da506e0bdcfcecde9d90e7c3`  
		Last Modified: Tue, 15 Nov 2022 04:20:33 GMT  
		Size: 53.3 MB (53260363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea09d00cab6fbd5c35726418a54ccb05ddbca3327042cad23e5899b1d30f83a`  
		Last Modified: Tue, 15 Nov 2022 04:20:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b54d16d026045414e22e9c1d9ec064d385544866b820db0f70bb41eb4951be10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58913361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bc30eeb0bcdc30d4e778538ffb7ce4c45ace1b98eeea9a9fc54fd7448cbcea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:17:38 GMT
ADD file:1a9427ec1dc5ca60bb760d16d5d76760f730c0c0eda8382a1d28a5e50535ad7a in / 
# Tue, 06 Dec 2022 01:17:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:17:49 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ff7c811b7837034ee1579672c45bccdf29d765e735d05c933d69b7a21769ff65`  
		Last Modified: Tue, 06 Dec 2022 01:23:42 GMT  
		Size: 58.9 MB (58913134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368ffc71bd73feed1556bc836fad1a05d383a37c6772ccd02b50e5ceb02e08d4`  
		Last Modified: Tue, 06 Dec 2022 01:24:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:36a37a8bc17b49959efda401701e165d2d6a79b47aeb0ec1e44ceb22c63b6af2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53271881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf2247b63c51eaa08162d1ea8a383497abb486e4cb2b2d5ea239bc9993d6669`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:23 GMT
ADD file:85bcb55b71ee57dffe1ea720e85546e314d2691e98658779a6f732d13e2e1038 in / 
# Tue, 15 Nov 2022 01:42:32 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:41 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4b50a7f3d916ceefc2228edab7fc6bc3e2fd142f385b7a04544973edc988c99f`  
		Last Modified: Tue, 15 Nov 2022 01:47:12 GMT  
		Size: 53.3 MB (53271656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258c2305c1d8dbcab1f996ef3ee4b0f85ec804252a0a2905be3302c1767115a1`  
		Last Modified: Tue, 15 Nov 2022 01:47:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
