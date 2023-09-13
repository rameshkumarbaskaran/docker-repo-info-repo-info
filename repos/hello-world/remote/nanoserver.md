## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:5ffc02be0e7a6fb1224a55342b222e92238db95aef59b1701430b3f45a75e354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.1970; amd64

```console
$ docker pull hello-world@sha256:efd257c8ea08ac9905e1b6b547c48f09e35d0916ddbbe33b0450e8faf061d97f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120570607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1998b5e6dfe20d2633f1602021f08a2ae2760bf7685dfe01c2db9a9ddfc82478`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 01 Sep 2023 00:20:14 GMT
RUN Apply image 10.0.20348.1970
# Wed, 13 Sep 2023 03:52:50 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 13 Sep 2023 03:52:51 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:8f8cef0759210af9d01a2fb45d79956a2db738bbd3734b7244b17e14ad945cab`  
		Last Modified: Tue, 12 Sep 2023 18:47:39 GMT  
		Size: 120.6 MB (120567584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d0a576ffdf4daee4b4473fdae04768ab239a0e30a93a87ccb6ba1be62df2d2`  
		Last Modified: Wed, 13 Sep 2023 03:53:11 GMT  
		Size: 1.9 KB (1855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d2970d05600f9ee866b6a368d7d8eb75fc40ca14d8d4471a5e450ae47d467c`  
		Last Modified: Wed, 13 Sep 2023 03:53:11 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull hello-world@sha256:75043f8f1db5630340cb611a64f0bb0f5bd49379cba1e202bf0f09c927542fa8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104495538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e162f4c1b2ff554907af7ed3f4b89f8678ad59f19240e829de3bbcbb12fbd66`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 03:52:57 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 13 Sep 2023 03:52:57 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591bbac16d61bc06d0e0ef6276e35da4fef3f656a556be2784f5dbb6970b2a30`  
		Last Modified: Wed, 13 Sep 2023 03:53:17 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51f0bc4bc3c8af5de2ba3776c9e69fa70da31a589bd88b258fb97224517a555`  
		Last Modified: Wed, 13 Sep 2023 03:53:17 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
