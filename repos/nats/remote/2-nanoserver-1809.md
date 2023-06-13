## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:0a384e9a7d76bb1288a9b091976b9fa61e78c22143d6a07415707fdd6123219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats@sha256:ffdbc972ae083180acdcc8d74756ed6c94b032bce6d7ec4c224f8343919f232d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109564530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b23b2cb10135235e109abd0ca99d3cf4027f72a1c246c873707190f54bffec4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 13 Jun 2023 22:18:13 GMT
RUN cmd /S /C #(nop) COPY file:e92fb324fb1e715aaa4f213ef42afe80c4a76690e3b2d439bee510cb2ae47cd5 in C:\nats-server.exe 
# Tue, 13 Jun 2023 22:18:14 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 13 Jun 2023 22:18:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 13 Jun 2023 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 13 Jun 2023 22:18:16 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74147f1370eb575d5bc03ac650054b5dcc36d7b40bf7706dde9d9d159d10e1a8`  
		Last Modified: Tue, 13 Jun 2023 22:19:04 GMT  
		Size: 5.2 MB (5174125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c441087537bf6a2963fdc58d12d836350044355df07fa9d696fe6e61819cc0ea`  
		Last Modified: Tue, 13 Jun 2023 22:19:02 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f7788277dc1622146a19b5407e20fc8eb003cd62b331460221d930e9154d31`  
		Last Modified: Tue, 13 Jun 2023 22:19:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b991262b6e730687a02c0d68ac25bc2dcf4dff69f1e9db5315f654387aab754`  
		Last Modified: Tue, 13 Jun 2023 22:19:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c322d11690204cb63afb856a65f1fdd8016ebd23989de8952a6ecb7f6737f17e`  
		Last Modified: Tue, 13 Jun 2023 22:19:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
