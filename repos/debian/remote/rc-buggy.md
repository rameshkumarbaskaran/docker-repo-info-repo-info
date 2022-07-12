## `debian:rc-buggy`

```console
$ docker pull debian@sha256:d08ff1c1cb881c3f0dadafb3c26bd53c54f5a488a142328a398d4a6f4847fb99
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:9839ea28855b0df5a334c56a9b41378f68a698a0db9506dd55aa877261b34a70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53219198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bf87037386eceda932fcd95b807291f1af077021f5a98087a45b57b7be03ec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:33 GMT
ADD file:5d253befef9729db59927d6e0d60fc3d68d46edea7e014babd24f72ac3a437bf in / 
# Thu, 23 Jun 2022 00:21:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:23:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d3673f28ea1768e72855620961143c989d7f371e6bca9954aea151e92c37b180`  
		Last Modified: Thu, 23 Jun 2022 00:28:29 GMT  
		Size: 53.2 MB (53218973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5348655b56344c114e4782c93d7780fec46a31e31dbc7a81686c2a6e8b3beb7b`  
		Last Modified: Thu, 23 Jun 2022 00:31:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:f7582f9a710ffef4e324f2332201f8c92df2b6bc805c1439ea198847baddf170
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51028180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128bc58cc49cdfac1325480fb6e13ba1c83ec6614641cbb86a9fc05e5acf82b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:53:06 GMT
ADD file:d09e1e4b772f7be41e6f5adcb5a71d86548e6099876e8d5d1bf8eb816a2d8cf9 in / 
# Tue, 12 Jul 2022 00:53:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:56:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c8fedff5488db39c94b1a6e628f1dd8a8718a76f0b9f0a65f57e06652448e9f4`  
		Last Modified: Tue, 12 Jul 2022 01:06:36 GMT  
		Size: 51.0 MB (51027952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63182a9db60951bada2f33097fe39ec224f032c377457e389140b66c67b7cd0`  
		Last Modified: Tue, 12 Jul 2022 01:11:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:d0d0db9fb42010b71fdda0d1cb58fccb8180d2f247558efcbc38140c9976c96f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48734937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e1b677d2d8a7fbcec86365ecd7609e18badc7da4f0e573f19f35165c0ee694`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:03:16 GMT
ADD file:51a321e16e02701a4130fcd4804ef7e14f5facfab8a82cdef3c2fd228a4ba034 in / 
# Thu, 23 Jun 2022 01:03:17 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:07:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2391a5c3a80e9c0555d4b398df748ee8be95db129c7c16e82cb7755d493118a7`  
		Last Modified: Thu, 23 Jun 2022 01:19:50 GMT  
		Size: 48.7 MB (48734709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e95ce7105909d93aa2d9d95467bd91d9c31065a2786e0b8d8bfe8f9523aa82a`  
		Last Modified: Thu, 23 Jun 2022 01:25:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:18334fb443f09c5635b1f42e68f506e34db31e8a307b0e30c911b4f54af024ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d64b2acd31b4ed466c32b9156729368b0a37972f543aae872a84e14773586d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:40 GMT
ADD file:0f18dcfe7e502abae9dd7f72911dda640e4675306760d63f467092f962228ad1 in / 
# Tue, 12 Jul 2022 00:41:41 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:43:12 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d3ef27d3c918a6321957a64c33268d09a01ec18590cce79a144625d9c0c8599a`  
		Last Modified: Tue, 12 Jul 2022 00:48:17 GMT  
		Size: 52.3 MB (52331756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f24de8cdf547261c03d6f6812060c7d8d4ac1fb5d8b0b094a09cc9ef14489c`  
		Last Modified: Tue, 12 Jul 2022 00:50:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:51d0fe0e8a16073344660f96f26ee43d9779406da8a97e6d2a12620bc4883e34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54207821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d3f0be7d444b474d47386bae6f66e297c65e7cf7b7d782213ea03d8b367131`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:33 GMT
ADD file:f76df7d0d2c0977290a0183cbc4f62656ab20d04eb0cae4d075fd31ddf9df8b4 in / 
# Tue, 12 Jul 2022 00:40:34 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:42:05 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b7f5437d02adf5c6ebc8b31ebf7b4950c58003a838e1f6591ce754472a3bae43`  
		Last Modified: Tue, 12 Jul 2022 00:47:20 GMT  
		Size: 54.2 MB (54207595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b223df6f2fbd218c1f4eaf806055411d1ae4709d9081e010486178750e8307`  
		Last Modified: Tue, 12 Jul 2022 00:49:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:22ea0d57898d2d35a132c1ca7ba4e6415bab414283e935fda8231ef4384acb7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52302830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6343fd6e9198ad27bcb61b45e2dee1e8508ee7ff937eebbd986d07f2a63c6dc4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:13:03 GMT
ADD file:ee6af73e7954397e332676cdf91fcc81e58c7039ee0e6b28c76a45bbcd35f878 in / 
# Thu, 23 Jun 2022 01:13:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:16:57 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1122351c74d1f54ed8c97871bc43b5e9e533e877516d1335d49d0b35a135e12a`  
		Last Modified: Thu, 23 Jun 2022 01:23:42 GMT  
		Size: 52.3 MB (52302602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fad516cb32977c66cc4d69a1d964363fe6515f751a1ed35364c343572fa20`  
		Last Modified: Thu, 23 Jun 2022 01:28:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:abbd915497bf0030b5c235d6898ea404989c8544baad28489732866cd6e393c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57413939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d9abfa3f7bb12e66ef70995de8655d42acdcf2f963474d6d8616e4127b7cce`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:04:45 GMT
ADD file:c9757ca75462d85dc4d76c948caf7c9441b1f94311712aed484424049dfa236b in / 
# Thu, 23 Jun 2022 02:04:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:08:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e03a908039ec9067867d0cfb4e2137913335e7055a4de7caa5a17b06fdcfc936`  
		Last Modified: Thu, 23 Jun 2022 02:21:32 GMT  
		Size: 57.4 MB (57413710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fd7c439305d961abcba0d92d72ab16b6bff3ee878546d26bf2156eca8ec7c`  
		Last Modified: Thu, 23 Jun 2022 02:28:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:e0df12e4c4cedf649dfa285d0d586557e71967fd0414c3d2ee1793c5196cca68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51757629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebe072fb10f802ec65c7b7b83741ffec4f3fc60ff56e24b99a70b28b367ee5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:46:07 GMT
ADD file:160fd6ac1dd96abed2e1719ac95e75e8a8eeaeef9e04a353e0ba4a23cbd1c1e4 in / 
# Tue, 12 Jul 2022 00:46:14 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 00:49:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a4ac3f896d9c36c21fdbee9a7ab2637136d4d09ef6db30c3b2b4ab10c48abbe7`  
		Last Modified: Tue, 12 Jul 2022 00:55:11 GMT  
		Size: 51.8 MB (51757401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec8f825735627d1d7ecb12c443aa547b347644761328a4ef53a0fc4baff8a3`  
		Last Modified: Tue, 12 Jul 2022 00:57:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
