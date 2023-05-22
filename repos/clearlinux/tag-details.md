<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:2acc48331653f385b25124447468ae6398ebf191742aa67cae99b7ed3dfa47c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:3ad6ba60e8028ac96e2e3d60e6ba155283190dcc61cce2e6caa68a4ad51ea3f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78112697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146b01690612aeb386c4e57fbdd88aaa07ee0bb46f99fa1221cd7b676ee31147`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 22 May 2023 19:22:53 GMT
ADD file:3137c5df694c911f1f35692d3945111a168801a96e39c845aa40d28de9e661b7 in / 
# Mon, 22 May 2023 19:22:54 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 22 May 2023 19:22:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92ef16c9791cb579d96f3f2190f4d9419019a5d1c6e45d134f67b2e8fe92c14b`  
		Last Modified: Mon, 22 May 2023 19:23:11 GMT  
		Size: 78.1 MB (78112479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03658db0d442908c76a7f0c5cb572303d67417fc5c0d0955f2f357d503337839`  
		Last Modified: Mon, 22 May 2023 19:23:03 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:2acc48331653f385b25124447468ae6398ebf191742aa67cae99b7ed3dfa47c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:3ad6ba60e8028ac96e2e3d60e6ba155283190dcc61cce2e6caa68a4ad51ea3f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78112697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146b01690612aeb386c4e57fbdd88aaa07ee0bb46f99fa1221cd7b676ee31147`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 22 May 2023 19:22:53 GMT
ADD file:3137c5df694c911f1f35692d3945111a168801a96e39c845aa40d28de9e661b7 in / 
# Mon, 22 May 2023 19:22:54 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 22 May 2023 19:22:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92ef16c9791cb579d96f3f2190f4d9419019a5d1c6e45d134f67b2e8fe92c14b`  
		Last Modified: Mon, 22 May 2023 19:23:11 GMT  
		Size: 78.1 MB (78112479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03658db0d442908c76a7f0c5cb572303d67417fc5c0d0955f2f357d503337839`  
		Last Modified: Mon, 22 May 2023 19:23:03 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
