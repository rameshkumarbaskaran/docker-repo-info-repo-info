## `archlinux:base-devel-20221002.0.91257`

```console
$ docker pull archlinux@sha256:33787b7abe685e0343c022b23bc0d54be281c60fc7d73f75b13e15085b6d7a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221002.0.91257` - linux; amd64

```console
$ docker pull archlinux@sha256:552467000569cfe052f535fe31fd66cb2bcd749f73d36255d6a777ff86b06798
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238593146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd00261ea299c70e6bfdde761a4b33e4e104a19a4f4b69cc05c42085522ea7ee`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 06 Oct 2022 19:55:51 GMT
COPY dir:18fea0b266ee182d9d39f5c46c96dce2236a702069f997545d0df7b9c4099d49 in / 
# Thu, 06 Oct 2022 19:55:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Thu, 06 Oct 2022 19:55:54 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 19:55:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a64de180eba4662e4ee754ae56002a9e7471e8f9a44f207562a29b6beacd97aa`  
		Last Modified: Mon, 03 Oct 2022 21:22:29 GMT  
		Size: 238.6 MB (238584575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb010f01c1e989914c006a49bb84bf8863e524a38a93b14e9f4e3340a82eadc3`  
		Last Modified: Thu, 06 Oct 2022 19:56:26 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
