<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:89d5747fdf1610aab6b6e9b0f912c22a3109f1b406eb8ce0778dc2030eb3a345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:094c2ca2bf7e54569a8246e2c35ba82a6c8d8641720e17ccaa49e2394b52fbd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68080125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294c82754d474c2e66055848fbeb737c2b8a2359155b72e0b50f2a727671866e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 01 Jan 2024 21:26:32 GMT
ADD file:ff89443e7fad411d8c7d0f4a659a5e8a7f0004ddf261204cba53d6771f8050cb in / 
# Mon, 01 Jan 2024 21:26:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 01 Jan 2024 21:26:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:66cb613e7e51643a235e661efa8709435b51012e8156bf3df7236cf93228e145`  
		Last Modified: Mon, 01 Jan 2024 21:26:50 GMT  
		Size: 68.1 MB (68079912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c570f0582c41ae8f510fc4df35c74905f96027fc6e57b9e8ddf9c0b2f48`  
		Last Modified: Mon, 01 Jan 2024 21:26:41 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:89d5747fdf1610aab6b6e9b0f912c22a3109f1b406eb8ce0778dc2030eb3a345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:094c2ca2bf7e54569a8246e2c35ba82a6c8d8641720e17ccaa49e2394b52fbd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68080125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294c82754d474c2e66055848fbeb737c2b8a2359155b72e0b50f2a727671866e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 01 Jan 2024 21:26:32 GMT
ADD file:ff89443e7fad411d8c7d0f4a659a5e8a7f0004ddf261204cba53d6771f8050cb in / 
# Mon, 01 Jan 2024 21:26:33 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 01 Jan 2024 21:26:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:66cb613e7e51643a235e661efa8709435b51012e8156bf3df7236cf93228e145`  
		Last Modified: Mon, 01 Jan 2024 21:26:50 GMT  
		Size: 68.1 MB (68079912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a4c570f0582c41ae8f510fc4df35c74905f96027fc6e57b9e8ddf9c0b2f48`  
		Last Modified: Mon, 01 Jan 2024 21:26:41 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
