## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:38606078c96176e50f076558a1c9807c2a0aa08cb78ba2221181a88fadba685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.1006; amd64

```console
$ docker pull hello-world@sha256:9a0ba871841eda4224f5e50ccc8c27cc480a48b7c675a4f0be9a5a52b07be916
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118134354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e861854f2e32f97dec4ed843dd2b1105725e14c233f759973d6fea0331f71b`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 12:47:40 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 14 Sep 2022 12:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7838a6eb98a69bf0e295ca16e136ed50291f6109a6ef1732b10c8e04c22e307c`  
		Last Modified: Wed, 14 Sep 2022 12:48:06 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e00cf48a380403edf434444e7934f9297543b6dac8064a0165473c2d35f01`  
		Last Modified: Wed, 14 Sep 2022 12:48:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.3406; amd64

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
