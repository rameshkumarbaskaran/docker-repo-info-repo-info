## `archlinux:base-devel-20221225.0.113672`

```console
$ docker pull archlinux@sha256:73d72b6f85966e914d59d3e856f589e5c59664417a16218cb2f025e99efb3222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221225.0.113672` - linux; amd64

```console
$ docker pull archlinux@sha256:6fa941953ad874c5363e01b636bcc572bd358f86c8caf237f5e7fd5415b44f97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243214601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab9d3b59167b2968faf960580a73567d52cb46e8e0ad767419785a0274e6261`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 27 Dec 2022 17:20:55 GMT
COPY dir:836eac076a3d3584555414a1ba8af1e19111ac4254ab0013c04ebf622f4fbb39 in / 
# Tue, 27 Dec 2022 17:20:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 27 Dec 2022 17:20:58 GMT
ENV LANG=C.UTF-8
# Tue, 27 Dec 2022 17:20:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:59701891056658ebd004fbb96fc17f6c195d4b3864b1f01659fa2cab5a948ba1`  
		Last Modified: Tue, 27 Dec 2022 17:22:24 GMT  
		Size: 243.2 MB (243205975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150bcc6bc64c75e66ac8e41ca39d55f2dfc2fba9a62b618811fbb0e0fdd49de`  
		Last Modified: Tue, 27 Dec 2022 17:21:48 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
