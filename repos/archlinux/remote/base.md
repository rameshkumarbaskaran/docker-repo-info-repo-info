## `archlinux:base`

```console
$ docker pull archlinux@sha256:5731615d9dd521f86bf75c0f092ea322e58e793e95541c7b7d5a9c43fd9c21f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a2c1a4eeec0df5f8259c01e8e7fb09514542053ff63e0f89592f1de5014eb174
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134183824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c656f9acae225a9b7d78f2ad2aed9493ea94ff4b0ef4f012372abcc6391c5527`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 27 Sep 2021 19:20:32 GMT
COPY dir:41379bd0eb07f5d88f28a81c88e1c4fd706f3f63efee8e72792a223ba0b0914f in / 
# Mon, 27 Sep 2021 19:20:34 GMT
RUN ldconfig
# Mon, 27 Sep 2021 19:20:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 27 Sep 2021 19:20:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9da739c6cf044a904e33751e9cf91a49f84a7bce978fe6b23838eca868925be`  
		Last Modified: Mon, 27 Sep 2021 19:22:20 GMT  
		Size: 134.2 MB (134177059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e107a42ffb7ed75fe3832146cd069171bf4891c025fc1a97a85c348298e57909`  
		Last Modified: Mon, 27 Sep 2021 19:22:01 GMT  
		Size: 6.8 KB (6765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
