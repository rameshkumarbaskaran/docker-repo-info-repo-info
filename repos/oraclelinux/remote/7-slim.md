## `oraclelinux:7-slim`

```console
$ docker pull oraclelinux@sha256:a926a3e7a5f94d881a71c3d27afa11147040f9bffcf16a0671a11a4c1e3dcdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `oraclelinux:7-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:5e0bfb4a9c75dc62119e4ca05d84cdfb2989c02490ac132926aca67ab53383c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48257477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dfc9a16f3b6375fc6dc7dade077efee1f898475d65219dd3fae0aac6a4a3fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 21:23:41 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 18 Nov 2020 18:16:17 GMT
ADD file:fbc16b85088aeb16b00035f95c6e08678b18cb8a31a4034a171a84b878f95cae in / 
# Wed, 18 Nov 2020 18:16:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:245e9951308ef864ce941f4383344a273da57264b763e6f5aba9347211cf7a40`  
		Last Modified: Wed, 18 Nov 2020 18:17:21 GMT  
		Size: 48.3 MB (48257477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `oraclelinux:7-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:2cc543549a4513afb508187bf3df1277e6031793a32135e356e75cf0e1ef1b16
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48865849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb40521c5b22b0a1a1ca5d524b4d18f0b6bd10606078d0f7bda05b9e06c41f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 18 Nov 2020 21:39:27 GMT
ADD file:f4a327657a328a670e79dc5abbe14d34c0f6083bc105b04205bb7b6007009f5c in / 
# Wed, 18 Nov 2020 21:39:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:436adcdab5ec3071ba37753f4a768eb644a6d3b209b6c68878fbd4ff8f133edd`  
		Last Modified: Wed, 18 Nov 2020 21:40:29 GMT  
		Size: 48.9 MB (48865849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
