## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:2f2781d32404b4ac077b3a2a160cae4153e83ab6d2394cee179e18f408f44ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:be610018e2d35f652d78f7b2ba5d7f5680eb636a156f0412715d890a7d60f500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67434631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a0b0b4b2e0fd8ea50df1e3fcb01b34406c334fee374e8b0a8f6e600dc136b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 24 Jul 2023 22:23:22 GMT
ADD file:5e8e8564f70345930086f221c09818f5e536ae4eae5932fdf24489d492970305 in / 
# Mon, 24 Jul 2023 22:23:23 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 24 Jul 2023 22:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:085a1eec5fa61febb111c2fa1ffed6d2436b2f6163cdcea06b9963689921250c`  
		Last Modified: Mon, 24 Jul 2023 22:23:41 GMT  
		Size: 67.4 MB (67434413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb57cf7b7c8567f46c6adab74661844bab1bee27e052aad20bb1d1165e78a04`  
		Last Modified: Mon, 24 Jul 2023 22:23:33 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
