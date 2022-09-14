## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:9a29bbc6ad11bfeb80d0bd98a39ca389687dd1b10fc43c66fd8ddf51f0bff67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull hello-world@sha256:ca68b1d9faa998468d4c7c4d0f07cf6126b8c220c5929be21b1a8bc15752d003
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103337241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22920b6a140f0add723e79a1a80551d66e435dc09a8d90622e6ccf72b010c299`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 12:47:47 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 14 Sep 2022 12:47:48 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9db0f53253b1aa71d86f1a9b3daaee9b752292c8c4ef8d3e94976a7ec033b7d8`  
		Last Modified: Wed, 14 Sep 2022 12:48:12 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f5cc2ffc563aef3941bcbf822565f754e1a68dfbb6863815837eb865777d20`  
		Last Modified: Wed, 14 Sep 2022 12:48:12 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
