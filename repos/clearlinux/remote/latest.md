## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:e2cd74c2d606f84d35d4d1b76550dd0f5d5c9b04f1d7e29d64f60a64fe0af14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:7e125ce5f8ac740cb698cadd4fa162bf136a8de336ccfa911a3f72939651553d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67693008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccd50684f6f30a4256776918c385a04afceadf5e721eeaa7ec40bfa82176383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 03 Oct 2023 01:18:14 GMT
ADD file:e04b7e2e5a72ac69fc6c662d107478297b7e2ad199805863952cd97aab77c837 in / 
# Tue, 03 Oct 2023 01:18:15 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 03 Oct 2023 01:18:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0faa3d8ef8b5dad521898c5784b44cce88e720afb7688bd7f65c47072ebbcf5`  
		Last Modified: Tue, 03 Oct 2023 01:18:31 GMT  
		Size: 67.7 MB (67692793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fedb986e392aebdc636400d0e44844d2702817762b10befecc0b3e0bf158d2`  
		Last Modified: Tue, 03 Oct 2023 01:18:23 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
