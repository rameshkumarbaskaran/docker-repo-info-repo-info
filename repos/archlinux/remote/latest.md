## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a1d7643994d32f807d53d22ee862f3c92de610d3ef6e00de7e907ced81505866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:85deb885f1c51373deb763f4a7f41a397607c590e1bbd52873cb10d86098215f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134759002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b518c6217b9d4a5465909c243d862d05a1519f824b8c68824dbaa9c32c13dd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 17 May 2021 18:20:39 GMT
COPY dir:29ca8ca1c54681df76de7744d67596b5c6a2f0d6589910fdc07ba844fcd60026 in / 
# Mon, 17 May 2021 18:20:47 GMT
RUN ldconfig
# Mon, 17 May 2021 18:20:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 17 May 2021 18:20:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:fff2a4638e3458e0c873e7c2918d5d0f8dc37b94f6b32af9a921a2cf72f761c0`  
		Last Modified: Mon, 17 May 2021 18:22:50 GMT  
		Size: 134.8 MB (134752340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2625d012e671ff9825eb4feedb97da0739a968ee467bb684ddad4166256ba661`  
		Last Modified: Mon, 17 May 2021 18:22:28 GMT  
		Size: 6.7 KB (6662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
