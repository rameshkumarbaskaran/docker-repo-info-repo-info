## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:1db69154831d3b3a88080c69533b678362e4d86676ca33b2e50336765c7436bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull nats-streaming@sha256:94fafaf460823aa892ed913e1f95a42f617b0b0ade5f63fec023190aad998802
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109610228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e2b8ca8f56a4b97f31133be06094bd3eeb0219661aba4e8aaaad7a79d723c6`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 15:55:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Jun 2021 20:24:03 GMT
RUN cmd /S /C #(nop) COPY file:72a29a3f2d4a0bd237295ad8b2a317a32c76cbb8a1af898a564024d5013c0475 in C:\nats-streaming-server.exe 
# Wed, 09 Jun 2021 20:24:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 09 Jun 2021 20:24:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 09 Jun 2021 20:24:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:80d93ce19113bbf944b699f12e59395e0eabeb00ccd1fd5dc7df46bb115eba2f`  
		Last Modified: Wed, 09 Jun 2021 15:59:58 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348b9d29d0e17e2575302e48a756c01845f95766a27b3efd5037e69dc02c3ffd`  
		Last Modified: Wed, 09 Jun 2021 20:29:05 GMT  
		Size: 6.9 MB (6934149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfbb95c41b561debff13c2fdc579566b502a46d04cc2aa8636fc043d67cf6f9`  
		Last Modified: Wed, 09 Jun 2021 20:28:57 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1321261d7f7de3d8a203008e1bd4541c0a15f00938a86e8f610acd674513bff3`  
		Last Modified: Wed, 09 Jun 2021 20:28:57 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58df4d427933ebe735d64a9ffec8fb7774cc74c1158c33e365322810443cc018`  
		Last Modified: Wed, 09 Jun 2021 20:28:57 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
