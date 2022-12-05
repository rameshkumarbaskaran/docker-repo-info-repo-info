## `archlinux:base`

```console
$ docker pull archlinux@sha256:55c45738d156c99d00242e830ec54eef8c02748a7c2dbe248892da9a1205974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:3d6aee337dd9ecc8fe77748b2ca752fd8df376bb7906e12c78df405fc67e59cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141795991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8792549afc11a8564693e63f6d1a75a45d0c24b76f288b4a9030ffa0dcb8b1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Dec 2022 20:20:00 GMT
COPY dir:4757859b63a669f0999e7e839d9752a4922ec2fb682fc9d4736e5e0dca4a7504 in / 
# Mon, 05 Dec 2022 20:20:01 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 05 Dec 2022 20:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 05 Dec 2022 20:20:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b4eb00ee61960c4be31f11880595238c7a8821317aa5768f85ee62d5c4d26685`  
		Last Modified: Mon, 05 Dec 2022 20:21:42 GMT  
		Size: 141.8 MB (141788039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00026c6783148c69ad6afbc1f14108341d55e2944decd384eeccc93693bbc508`  
		Last Modified: Mon, 05 Dec 2022 20:21:22 GMT  
		Size: 8.0 KB (7952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
