## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:56c727593cdcccc3b8cccaaacfd54144e11cbced9d761cd006f2c407a154f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull hello-world@sha256:f139ab66fdc388020ea59bc16452f137b6a194b2bfc5153a408a7c670a10b85a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104400917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c889e21ef6e07f64400119314a0a080217d27ad11c3e30404047b5cdd2fccb75`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:15:07 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Wed, 14 Jun 2023 19:15:08 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325d61a5dd8a664b3c232034d9118a6a26a884e9d68a2b082b4ec806ea96546d`  
		Last Modified: Wed, 14 Jun 2023 19:15:30 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a2addc4ca57eeed868f1a4da54c8213cb3268fdc73dc85870a4141eb1fb4b0`  
		Last Modified: Wed, 14 Jun 2023 19:15:31 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
