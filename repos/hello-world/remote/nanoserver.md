## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:b56156e812316c75b0f24d0c4fc13f98882cd2af118d063a7fbdef576b585433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.1787; amd64

```console
$ docker pull hello-world@sha256:b4aaa8a7d6bcaddce4de86d84fda8e8c47363583f273a792f5a21a71b4e80d15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120031578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fb9a013a942dcaf30c8cda86317ac503437e838a5fe3d8aa2717a5a8106939`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Thu, 08 Jun 2023 12:38:25 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 19:15:01 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Wed, 14 Jun 2023 19:15:02 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:f94f5e4cef3f52c830328b87b7298c638fa9ef22a0babf737eda2a2dd6d024c4`  
		Last Modified: Tue, 13 Jun 2023 20:05:48 GMT  
		Size: 120.0 MB (120028549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e081239de66420206edab006314510997bff2ff24a23b91363440873bb8a71`  
		Last Modified: Wed, 14 Jun 2023 19:15:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb32c3fd4583453977ef7fef16efafca2d713a458d299eb6f5ded7172781451`  
		Last Modified: Wed, 14 Jun 2023 19:15:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.4499; amd64

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
