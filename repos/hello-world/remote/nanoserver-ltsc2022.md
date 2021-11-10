## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:9202e50be02b7b1fc8089e854b5c7b437d0fbbfd1c3dcee089ba9081df6c5eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.350; amd64

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
