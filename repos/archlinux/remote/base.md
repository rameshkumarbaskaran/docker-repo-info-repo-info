## `archlinux:base`

```console
$ docker pull archlinux@sha256:d790ce3d666ccdbe03911bc77cdd37613ec77dba74f8a8fa80388e45af85720a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:8be0ef16329d575cd676018d8dc0398a3afe6fa9f710b1be2808cb56c784f6f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141868503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abeab40e07c301d01a97b2cc3c4240f345cd81fb467505192618debb0abaf4f4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 27 Dec 2022 17:19:54 GMT
COPY dir:4b076d2cd124d3fd8d2124df062dbb4d2165de2ca780899e5a8ed474c5256953 in / 
# Tue, 27 Dec 2022 17:19:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 27 Dec 2022 17:19:56 GMT
ENV LANG=C.UTF-8
# Tue, 27 Dec 2022 17:19:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:0fb1fc1e3209639276b5fe56211c1b2200881fad07571864d20a2bc403c5cc13`  
		Last Modified: Tue, 27 Dec 2022 17:21:38 GMT  
		Size: 141.9 MB (141860547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6830973604eb5cca90b48d3fcb956b97f561a446e1bf7bddca9e38d22e0999`  
		Last Modified: Tue, 27 Dec 2022 17:21:17 GMT  
		Size: 8.0 KB (7956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
