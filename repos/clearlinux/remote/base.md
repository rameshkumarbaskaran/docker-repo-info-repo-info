## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:0581bb6e97553365a369e1bf2e9cb5a8c633c3bbe63daa06f9f19ea0a6789d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:accaea65be8672973904beea55fdc4716933d8d50f1339c4090356c634a42917
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69306207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b10fb46dcb8863f370135ab6bd9758f904b6b5887b7be9b859948120a353a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 08 Jan 2024 22:19:31 GMT
ADD file:8e7117190c7119fde88a2de3284da8523db947a2111e35ae00f34ca37739cd71 in / 
# Mon, 08 Jan 2024 22:19:32 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 08 Jan 2024 22:19:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:38154636753ad6037722ef08de63fad1abc673003fb93cec2038e87dfdad6d36`  
		Last Modified: Mon, 08 Jan 2024 22:19:49 GMT  
		Size: 69.3 MB (69305994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87af0b653138b974190e4b1a08c9adf7ceffbfa936dea519f6c7b9a7e1148659`  
		Last Modified: Mon, 08 Jan 2024 22:19:41 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
