## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:6c4c472647bc243ea44fab451f8d8b747296b72586c8dc140df3a2caee87ba48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:5ec9740e516362436bf674033417d83ffd37590c6d30c75bca52c60d1512afd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87827723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818bc1be792dc25d25bcdbabed0d63b82f688bfce041fed19ab2828d235732f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 27 Feb 2023 19:23:32 GMT
ADD file:61074de6880d53c0959ab9eb51d74f816cd68ee4a8232fc7ab138432c9fe4af0 in / 
# Mon, 27 Feb 2023 19:23:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 27 Feb 2023 19:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:036fe99d3f4fe1d3e3be3c1d6d015fe78220a196ade2692fef99e43548697f82`  
		Last Modified: Mon, 27 Feb 2023 19:23:51 GMT  
		Size: 87.8 MB (87827506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a969d352fde6d4505e30ba366ef0893dd6e1a00747e9deb0adcd9d1185921807`  
		Last Modified: Mon, 27 Feb 2023 19:23:41 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
