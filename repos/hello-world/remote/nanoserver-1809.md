## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:424496d164b1d9df60a3983d9ce0869e81aaef1e432f7f492b890d94ed853145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.4851; amd64

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
