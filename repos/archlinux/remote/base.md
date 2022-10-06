## `archlinux:base`

```console
$ docker pull archlinux@sha256:df3968bf4cc3b56c870fc3687d9c217ebc7a9b47ab66a66961217317ef372622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a5337390f41961a1c18115935cc6ac5b8dfa7714cde2704ab86a5110df4420fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140382408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b17a3e650d6b974b7166a01f45ea55cae189018ee0d57b58864a289567aa873`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 06 Oct 2022 19:54:50 GMT
COPY dir:357d67580c7d304743f58414e41006932cb5fe247734f1d3ade0e217729b53ca in / 
# Thu, 06 Oct 2022 19:54:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Thu, 06 Oct 2022 19:54:51 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 19:54:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b3230fe6ff2a1bb5ff21943ee7b9b0c441f63a3790bff5954df37f50dfc01ea8`  
		Last Modified: Mon, 03 Oct 2022 21:21:42 GMT  
		Size: 140.4 MB (140374501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0021011b66e354f66e0fa5dbef713d683cf71ddeaaeaa718c4e1da551f9929`  
		Last Modified: Thu, 06 Oct 2022 19:56:15 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
