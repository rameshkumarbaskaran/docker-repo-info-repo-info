<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:da4372410dedc047cafc56911ad7865d96ad3658868af7ed9debdeb6e70a4143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:39b7573a9a65f08cce9e5744d53a99616d87a20c3cbbf910e25c6e56f8ef519a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88141835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe1b060d3acf6af90a6bba586146a680325c1dce1b58b146ae2c4a3a8a98873`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 23 May 2022 18:21:03 GMT
ADD file:e7a324a585fead8810947a17de9f26bb7b71a5a7970c0a1df7e49a6008738569 in / 
# Mon, 23 May 2022 18:21:05 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 23 May 2022 18:21:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b64057b4e1b70f276c58a5fe911764666b130a049ea3c1f89ccd8921385a198`  
		Last Modified: Mon, 23 May 2022 18:21:26 GMT  
		Size: 88.1 MB (88141617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5b4bc6842dd630b0d28d1d68b128b2597e0c9edc7f7484bb4e6440fa47394c`  
		Last Modified: Mon, 23 May 2022 18:21:13 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:da4372410dedc047cafc56911ad7865d96ad3658868af7ed9debdeb6e70a4143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:39b7573a9a65f08cce9e5744d53a99616d87a20c3cbbf910e25c6e56f8ef519a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88141835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe1b060d3acf6af90a6bba586146a680325c1dce1b58b146ae2c4a3a8a98873`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 23 May 2022 18:21:03 GMT
ADD file:e7a324a585fead8810947a17de9f26bb7b71a5a7970c0a1df7e49a6008738569 in / 
# Mon, 23 May 2022 18:21:05 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 23 May 2022 18:21:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b64057b4e1b70f276c58a5fe911764666b130a049ea3c1f89ccd8921385a198`  
		Last Modified: Mon, 23 May 2022 18:21:26 GMT  
		Size: 88.1 MB (88141617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5b4bc6842dd630b0d28d1d68b128b2597e0c9edc7f7484bb4e6440fa47394c`  
		Last Modified: Mon, 23 May 2022 18:21:13 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
