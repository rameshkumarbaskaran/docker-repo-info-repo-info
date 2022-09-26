## `archlinux:base-devel-20220925.0.89186`

```console
$ docker pull archlinux@sha256:3a9e03de9c3d1e95f90e31e591c3b2b11954e24d5c149b7ac205a39704b7782e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20220925.0.89186` - linux; amd64

```console
$ docker pull archlinux@sha256:bf5954655c93007d344e7f1a1e196c56e3bedcc0f7825b317a3b689e47181f17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237804461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aaeacc9b994422ee70790a3df869997ccb119694c510ffd37db2e7c03cf9b7a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Sep 2022 19:20:57 GMT
COPY dir:0c22ac20dabf097b7354470dfb3bf3d77edab31375e144264dd086eba60af762 in / 
# Mon, 26 Sep 2022 19:21:00 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 26 Sep 2022 19:21:00 GMT
ENV LANG=C.UTF-8
# Mon, 26 Sep 2022 19:21:01 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5b37b91f5c5ff3e99402b7c4ccc8f6651907f8fe5e094690bcb1f643807192e8`  
		Last Modified: Mon, 26 Sep 2022 19:22:27 GMT  
		Size: 237.8 MB (237795869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bf30a9abb9eaa4600eeff6f07e1d83b5e70ffd29368364e97cca06f6c8f9a2`  
		Last Modified: Mon, 26 Sep 2022 19:21:53 GMT  
		Size: 8.6 KB (8592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
