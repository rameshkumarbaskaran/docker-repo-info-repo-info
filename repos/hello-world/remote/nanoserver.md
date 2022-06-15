## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:d95706972446226ba0623e8e128f9b7f8402749f169cd6b463a7cd1290bf0417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.768; amd64

```console
$ docker pull hello-world@sha256:9ec668ee97c20731eb4f4f55f6248ac6b83a0d2e1add2110e6b5d62191f66dd7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117979576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db788e776744cd8feb6cf43df47514f9a6d9f8ab98fcfa10c763e493dd47fa1`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 12:58:08 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 15 Jun 2022 12:58:09 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:16dcd09ddaa9366692f6d318af489908d66013579288cd46841a3fcd0f66b59c`  
		Last Modified: Wed, 15 Jun 2022 12:58:36 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1189f324b04222419cece4c7cbd1a561c2228682c44eb6da6b1525c4b1e3751f`  
		Last Modified: Wed, 15 Jun 2022 12:58:36 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull hello-world@sha256:fa36b268301e951714b69bb6db7680639cdc1b7381cfaac12e98e09f94fdc0d6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103156295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef7f3a20adefd2ee56ec20ea43cb9c03b71eae39739ac03a2fb07bcb3ac1690`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 12:58:15 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 15 Jun 2022 12:58:16 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:941781a7904fa3029bb50d99b1459a7ec1d96afc538ac6cc2e3724ac41bab337`  
		Last Modified: Wed, 15 Jun 2022 12:58:43 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e486653a5f9a720877e17dcde2ee3234e459996493aa3bac79759647ad0e01`  
		Last Modified: Wed, 15 Jun 2022 12:58:43 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
