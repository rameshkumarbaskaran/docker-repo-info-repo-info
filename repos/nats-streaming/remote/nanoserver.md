## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
