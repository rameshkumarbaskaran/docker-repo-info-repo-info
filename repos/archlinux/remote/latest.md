## `archlinux:latest`

```console
$ docker pull archlinux@sha256:345144f4b0aea995de5738475fc36785c133304a25bcb0d374ca03c3f0660573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e7fb3b7f2840a68d9dd07ad5741dd9a773fde63d870c568978dba329d01d172b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141925942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a72a6159a613919ca30f6811174598bae7c50f89d5803a5df66780d57590c5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Jan 2023 20:20:15 GMT
COPY dir:c42d1863a8894c21ad7df2ef8e80841e1d4ee7bc52129bb6c42421257045c0f0 in / 
# Tue, 17 Jan 2023 20:20:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 17 Jan 2023 20:20:17 GMT
ENV LANG=C.UTF-8
# Tue, 17 Jan 2023 20:20:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:24f427444b18bd52922792c35a34d27186ebb645bda49bc594dbb7369c0696aa`  
		Last Modified: Tue, 17 Jan 2023 20:21:58 GMT  
		Size: 141.9 MB (141917994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee5bd4dd5b9171bcd78eb3169a8d65d0cc0700b0d41bcc3b61711b00da2ee69`  
		Last Modified: Tue, 17 Jan 2023 20:21:37 GMT  
		Size: 7.9 KB (7948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
