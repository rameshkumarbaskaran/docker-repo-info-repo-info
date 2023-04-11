## `archlinux:base-devel-20230409.0.141585`

```console
$ docker pull archlinux@sha256:ad18af22c93d03208f11450638ed59c15d95371589ca1fa0c446602750625cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20230409.0.141585` - linux; amd64

```console
$ docker pull archlinux@sha256:8e3e32b6b71897fd55fee0585ac3586e19a65ff94e13792a6b679f1b2fc17a44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246126806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37dc5345d168f341052800dffb4cb2c2c75acc085b58a492f3473c3a4449586`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 11 Apr 2023 18:20:50 GMT
COPY dir:5e0b9e18a476517bd58f1fad29d1ed47630830094f9d319f506d70cb67034059 in / 
# Tue, 11 Apr 2023 18:20:53 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 11 Apr 2023 18:20:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Apr 2023 18:20:53 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f316fb25c719a175ba6a8e01af80a7846c7f563be54a639586fae206ef173d55`  
		Last Modified: Tue, 11 Apr 2023 18:22:07 GMT  
		Size: 246.1 MB (246118099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139b1d0eb0c2028fc2abb922cebc4e3444e9a8e074fae8e6dafe173c4279c716`  
		Last Modified: Tue, 11 Apr 2023 18:21:34 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
