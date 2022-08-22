## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:8c8f4ee5d655c60b87f724f838f98d1b823d72693ebee734484f6f2a85158ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:04e7681a0a76a02904a7f44b056c81b9cf37be4c274b5bf9b3f848455d1f20de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234737977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c91d11fd6d9816dd9d78f649f0cad19f91aa17d66a0a3bd2bc9d258af8e279`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Aug 2022 19:20:55 GMT
COPY dir:fd2d68e25f1a9c322fa72941f712bfacc3ad5b51aa3ada809fcdb5e2e98c828a in / 
# Mon, 22 Aug 2022 19:20:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 22 Aug 2022 19:20:58 GMT
ENV LANG=C.UTF-8
# Mon, 22 Aug 2022 19:20:59 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ddf2501c622073db1641db7a817e12a7ef26a445895611a2c145dcc248b00fa8`  
		Last Modified: Mon, 22 Aug 2022 19:22:17 GMT  
		Size: 234.7 MB (234729200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12df4496e57311e177c58a39214c38f4b71aaee5c4e04c917840bd7f111da06a`  
		Last Modified: Mon, 22 Aug 2022 19:21:43 GMT  
		Size: 8.8 KB (8777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
