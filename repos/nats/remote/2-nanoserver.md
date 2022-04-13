## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:338b160beda6c311f0a03bd19a96f5b0513d81ea04e4e2cd319b2db00d9f7218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:8f862dd6bae660425765780cdc271275a6fd0487a731be1ee22b48edb4be477d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107652289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebe13c71286e0e75bccc444f6884d496f043c06be5e76f2fe4b31a852927bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Apr 2022 14:45:43 GMT
RUN cmd /S /C #(nop) COPY file:741c07610cba7dd6badafc477fe411065386e3878f26a0bf50ed1d89036d6dcf in C:\nats-server.exe 
# Wed, 13 Apr 2022 14:45:44 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Apr 2022 14:45:45 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Apr 2022 14:45:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Apr 2022 14:45:47 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390a1614c6e51a8b6427f7a28e408d5e7686ceac8399397a9e62357ae5e844d`  
		Last Modified: Wed, 13 Apr 2022 14:46:38 GMT  
		Size: 4.6 MB (4550075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756555742908471847260062ea575f5d1b2353f4b644f9e4ff80ab80b00486fe`  
		Last Modified: Wed, 13 Apr 2022 14:46:33 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c129657727c02d0dac7e07e554140e188f4deb6e6270dd954b4c4d7198ca554`  
		Last Modified: Wed, 13 Apr 2022 14:46:33 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72622f01880f0ece2286a64bca2116dfcf00642664c5f1b9171c6cce041318a7`  
		Last Modified: Wed, 13 Apr 2022 14:46:33 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faf58f7a1d30381ba2dd6e38f4b10d8b27d8064a2eec3f1f9205028422adfd0`  
		Last Modified: Wed, 13 Apr 2022 14:46:33 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
