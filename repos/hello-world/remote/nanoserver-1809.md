## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:e566292a0d9b42be8e46afc80c1ea6f66b134f819ba4b16c69ca78090e6693d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull hello-world@sha256:96ebeec770e1af26469c98913277e1c3b40933202ca398cefc16177c3f26cc75
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102785986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559c787b45777474057560283a07759e384a6be9fd76896b888f5b2341a00d9c`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 13:21:30 GMT
RUN cmd /S /C #(nop) COPY file:dbb4e437ca342a79d5980fcb71c065abfe00353f696b1b54084e7c09d32ec085 in C: 
# Wed, 10 Nov 2021 13:21:31 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0a19534517e2b98f305ad88e8bf97a76afe29339ae9c8a978ab76f2a86689a0`  
		Last Modified: Wed, 10 Nov 2021 13:21:56 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9d578c352f95aa2d7e4e55db3341028eaddb67f8e1e21ad5e1706c16283892`  
		Last Modified: Wed, 10 Nov 2021 13:21:56 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
