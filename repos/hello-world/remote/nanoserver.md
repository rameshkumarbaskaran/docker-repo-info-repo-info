## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:631e120bdccac3a5052e158606106d63ac4cbc0aeea4496ad4b5b47f96486824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.350; amd64

```console
$ docker pull hello-world@sha256:cb76c852a47032c7c42335ca57deeb72b0ff077557b61e3c99e0677ecdeec575
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117119846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedae85b8e224e2c3b029e1dfa13dfd33723f07abd1c1b3eafd6a684f8f6cb81`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 03 Nov 2021 08:13:55 GMT
RUN Apply image ltsc2022-amd64
# Wed, 10 Nov 2021 13:21:24 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Wed, 10 Nov 2021 13:21:24 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:83b9a19f898e6e25b6ee7e787da89582a8528b2defb5682f45364d04b35a278d`  
		Size: 117.1 MB (117116823 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b0937033554ce8abdc6af7642ebab60232320edd24d61d5f5d3daabc0ac4903f`  
		Last Modified: Wed, 10 Nov 2021 13:21:50 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb54155a27852671677f59aedb42ee249569dbe323d677803370323fc0ef7dbf`  
		Last Modified: Wed, 10 Nov 2021 13:21:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.2300; amd64

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
