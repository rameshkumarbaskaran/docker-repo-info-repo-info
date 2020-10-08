## `oraclelinux:7-slim`

```console
$ docker pull oraclelinux@sha256:2d474778d8009c9f47d633d95a7dcd0fa9040add03c083164dceabff0d7ec3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `oraclelinux:7-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:32677b1db67383eb84895e263f826fd5c8798a2daa2a49ccaa938517080123e1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48041338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e49421fa8fb6e09e8014c0a5b02c51c362bfef9867cc8870a8de874b2617fb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 21:23:41 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 08 Oct 2020 16:37:49 GMT
ADD file:b747df581cc38d6a653ccdef4b2b22a3ab465129d9b982a866cefb717a627cbb in / 
# Thu, 08 Oct 2020 16:37:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c36dbf3d26c0682385c39e59ea7c91d5d801ede8157648c145177059fca1106`  
		Last Modified: Thu, 08 Oct 2020 16:39:40 GMT  
		Size: 48.0 MB (48041338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `oraclelinux:7-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:bd722d03f2073bd8b42078b73897f4e7880c6cb9951e769cd503fd85b915ff6e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48605945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50762817df69cf806662c50ab31f161d5517e651539d7a187e6b20aaa7f30c4c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 08 Oct 2020 18:38:35 GMT
ADD file:ee7896b664af217b370300d68f776e8d7ae81958bc65f9bf27a4c9af308798fd in / 
# Thu, 08 Oct 2020 18:38:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:96e8c5ccf3b6c8a786327b651db7c9e5f2230838cbfdc5dd0b97a54c7cdbc75c`  
		Last Modified: Thu, 08 Oct 2020 18:39:44 GMT  
		Size: 48.6 MB (48605945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
