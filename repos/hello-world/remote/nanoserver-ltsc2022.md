## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:63d5ca114d8ebdcf48ed28f6819ee341011fa370be70f1f45ac0ee94820eedca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull hello-world@sha256:dd295b166e7a35d810b7d286c62fee3c575fdde553182271fc0e5fb01ac81b15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116900093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9974df6f6147f8e758b87c298d1c79c5d233e828146e6b2392578d653a8cf4d`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Mon, 13 Sep 2021 06:44:45 GMT
RUN Apply image ltsc2022-amd64
# Wed, 15 Sep 2021 12:15:05 GMT
RUN cmd /S /C #(nop) COPY file:55c009fa8b983e38026b41064e5367bc779dae76c0d404a11886c3cb19ec4509 in C: 
# Wed, 15 Sep 2021 12:15:06 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:521b4ff1716af921a5cfbf2119d97dc479e9b1eb487d17d0f576ff856ab68e61`  
		Size: 116.9 MB (116897071 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6df74b1747cb262a0eb9ba8906c8ebd2d777256eaffabcdf1de6a4bf79c054db`  
		Last Modified: Wed, 15 Sep 2021 12:15:27 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7304b4b26ddc15aabaf043e3b32fb910de29584cb353214f92a9369f95e07c7`  
		Last Modified: Wed, 15 Sep 2021 12:15:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
