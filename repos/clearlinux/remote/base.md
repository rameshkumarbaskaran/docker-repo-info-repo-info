## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:51aff29a3fd2e2752416048d2d7e4dd6243f849e34d49ed9ed6364e6ea3acad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:14496332c9c63d36f83aad4bd7555be5d757de6816eb54742a67c7ba350c0e0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97064560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca63c9d7c5cc2ef3e5534c63a5d65e7405595eb4ab87d5b6c7c4ac102df4f66e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 06 Sep 2022 22:23:13 GMT
ADD file:992983bce452b5e959822105964f891bb1e136d418dbb25fb78e43329bc5a27d in / 
# Tue, 06 Sep 2022 22:23:14 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 06 Sep 2022 22:23:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:353d52e95a26ff450c7713e60560b12343fe6a6de6393de26f9d5de5c5b29687`  
		Last Modified: Tue, 06 Sep 2022 22:23:36 GMT  
		Size: 97.1 MB (97064343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0805eb91d14fe51c27a37c0804cae26c65c79a7ce578adc8ed87f3d9e3f2b56`  
		Last Modified: Tue, 06 Sep 2022 22:23:23 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
