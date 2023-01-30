## `archlinux:base-devel-20230129.0.122153`

```console
$ docker pull archlinux@sha256:c1875289de35a3ccc8f3a6cad267a4c64c89187682d6c625569bae05dc53c5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230129.0.122153` - linux; amd64

```console
$ docker pull archlinux@sha256:b2c44c9a8b1043e13f62d2399deaa83103e562ba92b34b9dff7d50ae672c0291
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243457694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac286c82a7dadb6a693530902cfb6108e2813e3401b204f814149c18897b494`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Jan 2023 20:21:42 GMT
COPY dir:a195596530c408e680f453591555937d2f1ef5881e7e4de28cb024d6eee48d45 in / 
# Mon, 30 Jan 2023 20:21:45 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 30 Jan 2023 20:21:46 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 20:21:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:558fb3a8d7c6d1bfb0a6619bee47f50c830ccb97975e5763edd9a2f6210c16d4`  
		Last Modified: Mon, 30 Jan 2023 20:23:15 GMT  
		Size: 243.4 MB (243449044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a147ec4744ee4b18ddde59ee6dc1679d3dea3efc9bb7434723f0a198c7f304`  
		Last Modified: Mon, 30 Jan 2023 20:22:40 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
