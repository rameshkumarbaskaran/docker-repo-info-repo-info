## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:cfa379c242bdbb093b12fe3970703988bd18aec8bf890085fc226533d6948841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull hello-world@sha256:7780733f3cf8caf4de9b96deec0dd0a2bedc187d0a6934acd1308f3f7cd72166
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122006517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0eb300498435cbaa827ae2a85900e920dd9528c0a253ae6a07beb7b5fae99e`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 07 Oct 2022 21:37:41 GMT
RUN Apply image 10.0.20348.1129
# Wed, 12 Oct 2022 12:39:47 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 12 Oct 2022 12:39:48 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:b6520318982addabaf67d0cef5499282d15348f205cf5d7328925bcd681e85bd`  
		Last Modified: Tue, 25 Oct 2022 22:04:15 GMT  
		Size: 122.0 MB (122003513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2f9654ae65bd4aa50f3463f2d053025144322b599cc6506edf94170f1f170d`  
		Last Modified: Wed, 12 Oct 2022 12:40:11 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc05f03f8ab022e18841de9561dfccb6f6df66bd58150f7d0add0dda8f875a3`  
		Last Modified: Wed, 12 Oct 2022 12:40:11 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
