## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:4d6e131016d7ddd9a30a2a0ba2628f8fcc80211c356219121949a18b442e049b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:bfbb7e02d70062d845a2b9cc77e95cc509d69140ccb1c2a3db17236eec88b50b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67752364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b30a7265637637f93d8f7a27f2ec0d900b54f88e589ab6cbec37650dafc331`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 29 Nov 2022 01:26:25 GMT
ADD file:7a547c9dda087b299ed1f9e22c5107463114ccbc247ecc9f0adebd054497fab3 in / 
# Tue, 29 Nov 2022 01:26:26 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 29 Nov 2022 01:26:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a7df7865f69f5f7dca3f4d1392c5795137c23b245e283e68fc39df0bfa93bb1d`  
		Last Modified: Tue, 29 Nov 2022 01:26:46 GMT  
		Size: 67.8 MB (67752148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb8c55ad73ddf0d303f9647a03161d24c9298113a6b886aa5cda04a190ceaf`  
		Last Modified: Tue, 29 Nov 2022 01:26:36 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
