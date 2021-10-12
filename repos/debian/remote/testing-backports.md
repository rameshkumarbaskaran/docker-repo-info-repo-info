## `debian:testing-backports`

```console
$ docker pull debian@sha256:e7cf5ce97e192f88cc88eb8e9b8012bb65c313f71ee8b131a3a703358645bf06
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
$ docker pull debian@sha256:f071d8000941746b06552b7d86f62acb4aa0aa7be41f32b9cb6b23036e6c0c94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55446091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbf8ec476edf67f62e550d516cd4f7f1afd7d755f2c5c623c839f3522fc044e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:23:03 GMT
ADD file:7a2d92b4684fdb24b1c954a390700dbb0a50ce8cc8774b959e562a3652fb0456 in / 
# Tue, 12 Oct 2021 01:23:03 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:23:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91c31f9cd4fd949265f5532465cddce98935dcfa86015a5348b5f47c344d67e0`  
		Last Modified: Tue, 12 Oct 2021 01:30:11 GMT  
		Size: 55.4 MB (55445865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5824770af4ce48055efabe4fac2aab7542a6b709f6637eca8a1377ecc45d67e`  
		Last Modified: Tue, 12 Oct 2021 01:30:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:8620b8f705461640d885d7fd0664ec9e4c3b0869b72dba18e004d11d1002f72e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52965085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd5a09a176bdbab798d5c04d6877346c06222438d38fac0100bfe4b3a21af18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:56:39 GMT
ADD file:a0ded502d0b8dfe5e897243e08b3778f3adc2f2f41c32568ca6681c428d2896c in / 
# Tue, 12 Oct 2021 00:56:40 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:56:53 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:10d62d8715d4ae164047d47200167e5ce725ffbc04256c778e0aba73de1fd27b`  
		Last Modified: Tue, 12 Oct 2021 01:15:02 GMT  
		Size: 53.0 MB (52964860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f5e5caed528d1cd2839cb71052b6816e3eaf32635f29118816cf7ff52a6c34`  
		Last Modified: Tue, 12 Oct 2021 01:15:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:61d857d2b57d0100a9ab6b4dfd7bb920edca8704b79605786028ce80793b4f1a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50566311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c460cd1326c3c233bbf5ef02619564c276e72c79d854fd9221bff46fcfe1986e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:35:12 GMT
ADD file:4927232089e749d84b21863f4f2612c8a799f3039adcc70d971cbea78ed6a7af in / 
# Tue, 12 Oct 2021 01:35:13 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:35:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bec27cf3f9ae45321e058c161bc06cb3640cc32d6d8cc5cd5119b254da7ecfca`  
		Last Modified: Tue, 12 Oct 2021 01:52:46 GMT  
		Size: 50.6 MB (50566085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b399cd77b8cd1e9b055352793d13269844b4917f8e1a8558bcf4c1dae69e3954`  
		Last Modified: Tue, 12 Oct 2021 01:52:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b2e544bbdea33141e4ef582c7b3538ed7c6303d2968f405a7eb386c438502eb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54465248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ce844ced3881c1131de9fa4d83b8630208e2096e3cdba37222b594e2373685`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:39 GMT
ADD file:0d2781f09dc7fd32dad3f41e34a91046910847a56bf128bb53a7cad6c06c1f26 in / 
# Tue, 12 Oct 2021 01:43:40 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:43:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a75495c66c5fc986e1fa178fa94fe24ac603e1ee8a61ff4b344624e0b8b030e`  
		Last Modified: Tue, 12 Oct 2021 01:52:57 GMT  
		Size: 54.5 MB (54465025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d61c7e6ffa68075e0b3f1eea821950b0b0f59ec58f9b1b2107daf1e12bfbbf`  
		Last Modified: Tue, 12 Oct 2021 01:53:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:d4d40853641218b9a8fdaf7aa897964b8aa8ba8bccb31aea88f461fe979394ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56481075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a37d6c737feaebf9d2f5aba20c0466dc333f934d3b9d8b166ee3a842162c67`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:42:48 GMT
ADD file:15469ad0ddbee66d623cee7627f9ae7a0e09baf6095d23599c5cb2ae7493abae in / 
# Tue, 12 Oct 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:42:55 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8508f9607417ad80810488921b0ada480e2ce5d8a1cb8f2303e5d0f3a1d2174e`  
		Last Modified: Tue, 12 Oct 2021 01:52:56 GMT  
		Size: 56.5 MB (56480852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec11d340291661cf3b9cc18cbf8a40719d23c3b8bef6b61460dc6a6b1c9cc97f`  
		Last Modified: Tue, 12 Oct 2021 01:53:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:357c32bcbf0ded68b7985e474081831f2fbe727f3b736cb004deace857db2152
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54069294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6813d2a9b792085a58c0b879b70bc565953adf3999934886a6de00cc22786ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:15:09 GMT
ADD file:3d46a1b0da2f717a6fcd5a81011ddf94c751043fb103b98d488647a531fed650 in / 
# Tue, 12 Oct 2021 01:15:10 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:15:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4216a1c7f16a580bb4ab02a3c570e7f8ccf383c93ed4aebda567c184fedb4fc6`  
		Last Modified: Tue, 12 Oct 2021 01:26:17 GMT  
		Size: 54.1 MB (54069071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6959c86437187d476505fe0055d941cf0989208c989007161e291681b27a6a4c`  
		Last Modified: Tue, 12 Oct 2021 01:26:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e32c18612f213d84f9e18eac403fb57e5fe471b548de603dfb694a905bf47bd0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59660185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f312451e2735904f799ad06290dc6af80d9cd9cd83118ba35e8fe8d779e13d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:42 GMT
ADD file:2920b1ef5c61978464fc969befdade3714d84884adee006fb93d4d89bb412093 in / 
# Tue, 12 Oct 2021 01:29:48 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:30:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7695f94c27f2511cd3e23671d32882f166a2fc1b8124ec1f9d3f769e88536556`  
		Last Modified: Tue, 12 Oct 2021 01:43:25 GMT  
		Size: 59.7 MB (59659961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51001182f6335022e4749520f5736ebee1eef396f82d1d285774a66b31938bd1`  
		Last Modified: Tue, 12 Oct 2021 01:43:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:bdc41768477b3bb9beb65aeac3ca8ffab0b164d3ac05943a47792c0fa6acb6d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5083110b8c0267d1775243cc8b7798d314f86be408b00cf1aa4b0c835c3415b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:44:24 GMT
ADD file:6bdd28da982bbaaa3e5fd43949b430a741f7441a3423aea45476b602884003fb in / 
# Tue, 12 Oct 2021 00:44:27 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:44:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:16455b9c3f308b090e540412543381f2981a94842cb89496c8f0d1636c7ad1da`  
		Last Modified: Tue, 12 Oct 2021 00:50:24 GMT  
		Size: 53.7 MB (53700056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97085952c5b25aa4e803de74f56e2b96bd6940d37b732a1e7691cc829c28e6`  
		Last Modified: Tue, 12 Oct 2021 00:50:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
