## `archlinux:base-devel-20220619.0.62803`

```console
$ docker pull archlinux@sha256:40a7947706c04edfb8543fc4e5ef1b8ce782cc3225cfff84d7a093ecc63d94d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20220619.0.62803` - linux; amd64

```console
$ docker pull archlinux@sha256:33823c01caf670409d0c1bf126292027e820f084d1c158aaa9b89ca616ab3004
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224847260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2f18626b8dafd00d2efa816970fc939c643012b11c967783465c15915318a9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 21 Jun 2022 22:20:52 GMT
COPY dir:083ee8ac27c98f147fbbd0b0a5fa6338cbfac41367c0f1f4d0ff09053eecc44a in / 
# Tue, 21 Jun 2022 22:20:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 21 Jun 2022 22:20:55 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jun 2022 22:20:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:36cc5434b2d6b446a0fe20a8ed9859fb52a36b3c711deed2822f3e0be9211df3`  
		Last Modified: Tue, 21 Jun 2022 22:22:10 GMT  
		Size: 224.8 MB (224839091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96cd407e1e8ef2411728c2d1adb90e06e179dec528d64f523b37ca808941f03`  
		Last Modified: Tue, 21 Jun 2022 22:21:38 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
