## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:8af5624f20406dff2f04047a77a0125d124cb6fc5e7c59cbd7ad65b11f226279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `hello-world:nanoserver` - windows version 10.0.17763.1282; amd64

```console
$ docker pull hello-world@sha256:9d21bfe120245583dfd139d70e41c0822fa5bac129c4a42e2fa5c945284fcc3b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101045968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8a46951ebde059b05d2d096b5f8d943159860b0a465214d772f56c09fa5c09`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Wed, 10 Jun 2020 12:11:34 GMT
RUN cmd /S /C #(nop) COPY file:0afaffc2fa64462107b7178b2ae7d20404ff12f637eabe3a8046192b9d9a0338 in C: 
# Wed, 10 Jun 2020 12:11:35 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cf5ac7c6c58741a924e776926efa9907666d0a29e497f1ac1d9dc8decdf5ed98`  
		Last Modified: Wed, 10 Jun 2020 12:11:49 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049a34ecd92e9d941503d92ced206a404f8f7a2e2c74f497f9283d6ce842489b`  
		Last Modified: Wed, 10 Jun 2020 12:11:49 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
