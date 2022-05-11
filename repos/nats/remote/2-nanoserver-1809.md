## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:a778e8e1e3203b35fe0bdb6c5a94e8f63de63b9f4bf2eaf17eee3317170649c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:f91885fa620a9738072e61f4d68d9a8400803e2cfafda40886de5903451520e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2bd603b8bbf94bbdf8466e6848b146754fe29271b8e95884a8d2abcfac67eb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:42:08 GMT
RUN cmd /S /C #(nop) COPY file:1e690007468fe11473f18dc8fbc8b7aa29351e71d03ca73f75d9fcfbf1fd7911 in C:\nats-server.exe 
# Wed, 11 May 2022 14:42:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fb401df1c150a43c2ec9b3ff57a672b92c67107234ab008625c5fea9f9e69`  
		Last Modified: Wed, 11 May 2022 14:43:04 GMT  
		Size: 4.6 MB (4622748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09ac197c7dae98dd6fa2697e81011965729a49252e223601d418ba0ad439c36`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f37eaf04793dd48de8ebbf4bd5188e4d0f528f5047265be5c86a5d12c133c26`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae6fc61c5a618a623aef25b66fda889d02d4ca7084477f4c21831a7150291d`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7ab8b701dbc07245b31e34f1ed8493639f5d99ae276a089bd8c7a35a8bca9`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
