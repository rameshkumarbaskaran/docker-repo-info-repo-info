## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4e1fc1be5cc3daf03baac7b1b636bead7abd9e33a69c154aa1761e0735b1f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:ba0d15a1d81321b7dc556caa59f327672523cf7381bf64d28c69c2d96165c5b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127206324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c8b3677ed66df563c871ba97b38cf00f2c795e1a24f2247bb21566ca4a34df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 22:19:51 GMT
COPY dir:419b23cf3e7221564b387c6af9ad8809f71730e5962afaeaf6b4d02e47f6728f in / 
# Tue, 21 Jun 2022 22:19:53 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 21 Jun 2022 22:19:53 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jun 2022 22:19:53 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e814398820a35bb2a2a486bccc79d47fbf45783fd95fa1a41b69b9a216e77db0`  
		Last Modified: Tue, 21 Jun 2022 22:21:26 GMT  
		Size: 127.2 MB (127198772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acd6aa28f56ac15cec935db4b5f96468de5bfd704ab70e399652f94a9c6f209`  
		Last Modified: Tue, 21 Jun 2022 22:21:07 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
