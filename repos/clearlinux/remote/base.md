## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:1d865a4614b6c362f6a0aeabca7773e66cbcf0a7fe18957c71e5a6704f28d62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:533bcbae0feebbab02b40aa510a57727c709cbb242189c8d55af6534ed07d9a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68821466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc8a8fd7af9068d5f4f837a850cb1425b9644cee7b0425cfca4f68361ab6ec3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Tue, 11 Oct 2022 17:24:55 GMT
ADD file:bf21e40bb5f4afa9e224409fc2a39110b74bce17d7696613206deb13315a6280 in / 
# Tue, 11 Oct 2022 17:24:56 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Tue, 11 Oct 2022 17:24:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9788d575f7c3a4cb52dc5305af3407e745a2e1a495920e0e697b4e17303411a1`  
		Last Modified: Tue, 11 Oct 2022 17:25:17 GMT  
		Size: 68.8 MB (68821249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed187032fa546f62946332e9eee026f7b1e157ef997c5ec5da8337df4772685`  
		Last Modified: Tue, 11 Oct 2022 17:25:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
