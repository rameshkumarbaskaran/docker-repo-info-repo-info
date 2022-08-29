## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:5edd490729b4499fca3299130b175d115618315821f7d94dce95f32e38c60ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:aa30a11363b4e3cf22abdd179b53eaacb46999c797ec95b0c4e350e6a3391c8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97063325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b39916cf8d159141abad607b2c70c3027ff87f2227200f3dc0b309301ad3fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 29 Aug 2022 18:25:40 GMT
ADD file:57e82b6309a47eeb869c4407389cb4348bd639c1f96496b2a15204dcdb216afe in / 
# Mon, 29 Aug 2022 18:25:41 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 29 Aug 2022 18:25:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:081efcec341602b4969b6334a63313d154977ee7e916555addcd3a2cca0abc7f`  
		Last Modified: Mon, 29 Aug 2022 18:26:05 GMT  
		Size: 97.1 MB (97063108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401fdb06f2fd427627d8271bf433567a87bfed1f2576e97e79c399d5e9ab6765`  
		Last Modified: Mon, 29 Aug 2022 18:25:58 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
