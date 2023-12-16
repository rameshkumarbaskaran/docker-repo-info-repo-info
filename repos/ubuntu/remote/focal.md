## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:2776e04192ee13ecb3a6e8499d9e7d31ef183125210ddcd765a624300e066a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:fe8a36445d3d850960d6a24554f2cf4e19d82ba1e611e3e8713bd7b76989623d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27512563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a4bf3bb050e11e0f3bfdcfaff38eeb1dd851b7a362d930cd590dd97b3b1687`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e8d1b4432e4a0f42554de1276c83035ec085ffb6a77561ea193e0604b9ff550d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23621780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566b072c3e69fa5ebc000bae5a62055d981e2652df2a50fcc51565dcfa749007`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:27:44 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:27:51 GMT
ADD file:043af50602b163e71a05aa02ec03cbbb2659582ffeea29004c4477939cf448e0 in / 
# Tue, 28 Nov 2023 05:27:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:660a040f0695558e8e4f973f3f254741778f545a610346e00560a582305c6f02`  
		Last Modified: Tue, 28 Nov 2023 05:37:31 GMT  
		Size: 23.6 MB (23621780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:074f14759aac23ee1f3ec318fbc1baa83f309ff78ad4448d63f79d2c8bea24c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25975507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51abb690a3439f2dc40cd5546d184a849ecba847491d2acbaebaec01d90196db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c083ada488db06e4b75cf31d279946b478acfa048e2f0aca39f8ef90c2006386
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32075270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1aa8372f4210a7209e1250808d562df02be12280f883289c22fcf4e62d154`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:36:32 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:36:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:36:35 GMT
ADD file:b7dcee8fbada51f19b857a4a8ef334aab211090abf4247194ddfeb1504df7420 in / 
# Wed, 13 Dec 2023 10:36:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d20838a29743bf51a2def4bf0d3bc0cb24f5287a64cbd5d90d451bca5da0626a`  
		Last Modified: Wed, 13 Dec 2023 10:49:17 GMT  
		Size: 32.1 MB (32075270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:e3a8fd652ab4f3349c1c1e872ce5dc8f904ee5e702da67a052de21ba1a73bdfc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26363432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2100e7bf53362df619b569b29c7edd960f4091de1b47ad8838c16444b53b0d5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:20:48 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:20:50 GMT
ADD file:d9d0513ebd111f79b38e6a84389a13bff0ea39811a455d2bf83565e10a32040e in / 
# Tue, 28 Nov 2023 05:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1baa125247957ef5c6754c3e8f1d9b1a6a073bc38c8f3f5a37d3bf31b377f6c0`  
		Last Modified: Tue, 28 Nov 2023 05:37:46 GMT  
		Size: 26.4 MB (26363432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
