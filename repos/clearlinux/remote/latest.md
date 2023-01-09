## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:6021883e7397f2393ce449b132678e4e72ee9f74c4b949ae2ebfd46498f60a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:10a8b934c2512d987d916577233d72588400c23f570d3e9b313a607d8c2a71e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91507762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386d5155b3ee20274394070ba637c37fb60943ce627d4cc7ca2f188740c8ec67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 09 Jan 2023 17:19:15 GMT
ADD file:7b66103c5aa15d217b0a5944ee69ed4b3634c488734b74ef848c9e1362aade22 in / 
# Mon, 09 Jan 2023 17:19:17 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 09 Jan 2023 17:19:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fab6b7ecfcddde962036762174d5c2d491681737d5aa2ec212b446e12b013d1d`  
		Last Modified: Mon, 09 Jan 2023 17:19:38 GMT  
		Size: 91.5 MB (91507545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111325d89e5a6b8045216e533866d68578deeb68790daa7f41b27d9b224884e`  
		Last Modified: Mon, 09 Jan 2023 17:19:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
