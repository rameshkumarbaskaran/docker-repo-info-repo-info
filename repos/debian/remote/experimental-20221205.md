## `debian:experimental-20221205`

```console
$ docker pull debian@sha256:3fab52efecb023e40fa6d7634346fcd9783ce28370f8291388fe6f6b3c94943b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v7

### `debian:experimental-20221205` - linux; arm variant v7

```console
$ docker pull debian@sha256:e6e414b6709f5b4dd233228aa8642fec5e909d67795fe0eeafddaf85ac612a11
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715ee2cea488fe3b7d3e39b9255de966164166de48048720b38614a4faa09e6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:01:52 GMT
ADD file:67c7856b9f449444d23292272382e4085597b1177d2e9d4ba3a5cf4cae040d47 in / 
# Tue, 06 Dec 2022 01:01:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 01:02:12 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:be75358763d092f0c026bf214ed08a6578f209118c68bc9bf4a6e28c6883ff8a`  
		Last Modified: Tue, 06 Dec 2022 01:09:51 GMT  
		Size: 47.1 MB (47097033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a9ba7d64422b367c5ce1f6f0064b2b3cf4debb21b0922109a46563b96dc58a`  
		Last Modified: Tue, 06 Dec 2022 01:10:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
