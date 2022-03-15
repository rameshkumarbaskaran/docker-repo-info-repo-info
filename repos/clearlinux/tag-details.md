<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:7b37fe2b309280e57ee08da650d652309d9215434e31b250782d917ee80b6622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:388b9ab4c9222885f4025efa4cd96f87265237f490fdfaa8e7c644921b319786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88055046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ce7f86ee605aa70f7025f2b6a873cb57205b0cda5de20a9385818784d539b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 14 Mar 2022 17:23:03 GMT
ADD file:334a451804f5b6b5b220f296a5fd6d69b998c0c20f75ec46413971b7d47c21ae in / 
# Mon, 14 Mar 2022 17:23:04 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 14 Mar 2022 17:23:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f66c8af2665fd6c7163f01ad2f841bf6f20b0e151ca5e0e7860420f03c4080eb`  
		Last Modified: Mon, 14 Mar 2022 17:23:26 GMT  
		Size: 88.1 MB (88054829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793a06b2cc994034b70f61375d3c61af524850cdded223f32ce42088b858747d`  
		Last Modified: Mon, 14 Mar 2022 17:23:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:7b37fe2b309280e57ee08da650d652309d9215434e31b250782d917ee80b6622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:388b9ab4c9222885f4025efa4cd96f87265237f490fdfaa8e7c644921b319786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88055046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ce7f86ee605aa70f7025f2b6a873cb57205b0cda5de20a9385818784d539b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 14 Mar 2022 17:23:03 GMT
ADD file:334a451804f5b6b5b220f296a5fd6d69b998c0c20f75ec46413971b7d47c21ae in / 
# Mon, 14 Mar 2022 17:23:04 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 14 Mar 2022 17:23:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f66c8af2665fd6c7163f01ad2f841bf6f20b0e151ca5e0e7860420f03c4080eb`  
		Last Modified: Mon, 14 Mar 2022 17:23:26 GMT  
		Size: 88.1 MB (88054829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793a06b2cc994034b70f61375d3c61af524850cdded223f32ce42088b858747d`  
		Last Modified: Mon, 14 Mar 2022 17:23:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
