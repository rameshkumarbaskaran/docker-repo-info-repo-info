## `debian:experimental-20200224`

```console
$ docker pull debian@sha256:532d153d852864b26588ef0e6b6dd44d1c1161210a5c76c9ae158cfc30d72bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; 386

### `debian:experimental-20200224` - linux; 386

```console
$ docker pull debian@sha256:40de0ac07cc3c36ff85df99ded8ea17377d3c9c96057fd195bcbadbf89e7005a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52999796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b44f9dd5bec05227df03b643054918a10ec74d874c5e343714f8f45805630d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:36:34 GMT
ADD file:5955a629c35b1206468485798e83690e152f5d8339418318b4bc5f98767d2df5 in / 
# Wed, 26 Feb 2020 00:36:34 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 00:36:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5367f3e8a07cb0a9f87933b63de70f98eaa2c832490cf96072fa70efc87341fa`  
		Last Modified: Wed, 26 Feb 2020 00:42:59 GMT  
		Size: 53.0 MB (52999575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7ecec61c6a38b9086cfd38dbbb7deb338135040dd4aaa6e93e1eb9d859121f`  
		Last Modified: Wed, 26 Feb 2020 00:43:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
