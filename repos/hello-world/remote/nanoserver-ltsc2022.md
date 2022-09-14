## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:d0a6ed9d01fcb8e5b24a4e4f1aa023eda3fa31b1b1fdfd0b940f29a3595510d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

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
