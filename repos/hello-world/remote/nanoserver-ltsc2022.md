## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:d543d4f4b18ede8ceed900af6466ee0008f9688851d4be2dfa5555aaaca96e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.768; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.768; amd64

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
