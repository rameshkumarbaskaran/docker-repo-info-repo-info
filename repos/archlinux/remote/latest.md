## `archlinux:latest`

```console
$ docker pull archlinux@sha256:01333c9d0acd59c4566d7e4138384d992cb16079530d4198d33916e4397e0230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:67d11262b299022437eb2961e45ea83f7e6b41bc2c42333a13132923ee08692e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127523560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8635d7bd071c3efa2365425018bb9a65399b563a8e5f4394848e2b0b4453b3c2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 05 Feb 2020 23:21:57 GMT
ADD file:2ea25033cb49fb646c8490ebc0747c9e61b8947186602fc7270294797b8a3c07 in / 
# Wed, 05 Feb 2020 23:22:01 GMT
RUN ldconfig && update-ca-trust && locale-gen
# Wed, 05 Feb 2020 23:22:02 GMT
RUN sh -c 'ls usr/lib/sysusers.d/*.conf | /usr/share/libalpm/scripts/systemd-hook sysusers '
# Wed, 05 Feb 2020 23:22:11 GMT
RUN pacman-key --init && pacman-key --populate archlinux
# Wed, 05 Feb 2020 23:22:11 GMT
RUN rm -rf etc/pacman.d/gnupg/{openpgp-revocs.d/,private-keys-v1.d/,pugring.gpg~,gnupg.S.}*
# Wed, 05 Feb 2020 23:22:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 05 Feb 2020 23:22:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ef42853c0f87fc68e54fc6b60fe8a5ff393396a487b3385d9c0a7277f68c481c`  
		Last Modified: Wed, 05 Feb 2020 23:24:24 GMT  
		Size: 124.2 MB (124206784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd2121e98da16f2dc079977509a764cccc133b39fe2989633b38d875badf0a`  
		Last Modified: Wed, 05 Feb 2020 23:22:59 GMT  
		Size: 1.6 MB (1598391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214eaa4433b284ae72c4b828b5266004f72dc93692d39ca46354fd75f6c98a63`  
		Last Modified: Wed, 05 Feb 2020 23:22:59 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56470d7667b79334ca3ab5006f67066e626c06c22e0cc43f30b414969856868e`  
		Last Modified: Wed, 05 Feb 2020 23:22:59 GMT  
		Size: 1.7 MB (1716956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896334b8e58301cb230d705bcc594765c8702efd1ea035648ddbafa193b65f25`  
		Last Modified: Wed, 05 Feb 2020 23:22:59 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
