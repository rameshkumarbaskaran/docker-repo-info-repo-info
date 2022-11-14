## `archlinux:base-devel-20221113.0.102112`

```console
$ docker pull archlinux@sha256:ce6fcd78c698176b06f81cf2d1f881ca86f5fbc6b6078894af42a1fe1ea170df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20221113.0.102112` - linux; amd64

```console
$ docker pull archlinux@sha256:4e96b5361c605ef460c2cc315370e809b227634da51a7d49abb8fa9c32ca4044
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243005615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d090529544b8276299fa5979b7d7960828752afd4a5182ca64d4b71519302e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 14 Nov 2022 21:21:06 GMT
COPY dir:8c06a6373ab1904938712a4232a2a4b86ecbb85293114557f3dccf4c2c6c23c3 in / 
# Mon, 14 Nov 2022 21:21:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Mon, 14 Nov 2022 21:21:09 GMT
ENV LANG=C.UTF-8
# Mon, 14 Nov 2022 21:21:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:81811940900b378cdf21a67573dea207571aeece75a017e6e12ba2629b65e64c`  
		Last Modified: Mon, 14 Nov 2022 21:22:34 GMT  
		Size: 243.0 MB (242997003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb557f22bcc7268e490cabcc90e6ff57290814121c7f4d979047f8045a0639`  
		Last Modified: Mon, 14 Nov 2022 21:21:58 GMT  
		Size: 8.6 KB (8612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
