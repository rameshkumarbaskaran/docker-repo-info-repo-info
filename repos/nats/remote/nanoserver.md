## `nats:nanoserver`

```console
$ docker pull nats@sha256:00b49a07da2c980ecc4d8b7c51db2e61a21794eeaf4a7d9ec4266ffe6550660a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats:nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats@sha256:10aaea87cc3f0763b67c70734d880a75890efaa5a30de546108be2ada36f5e4c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105455226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21816b899e9f961535bdf4c927a6c22c77d6390807d3aede30858735653d63`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:02:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Feb 2021 16:02:27 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 10 Feb 2021 16:02:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Feb 2021 16:02:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Feb 2021 16:02:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Feb 2021 16:02:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23b613036f8aee9066e712b3aa58f10f2fde093623511a5658867f53a6d01b18`  
		Last Modified: Wed, 10 Feb 2021 16:06:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669220385c98fbe939f12a1128ef3a5f45021ae3a98ed2ed61a4c8d95b7ab641`  
		Last Modified: Wed, 10 Feb 2021 16:06:37 GMT  
		Size: 4.0 MB (4042932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a47b7c10d54ec5b52d03a2d0c658b075d4105ab9b59cd95a696ccb58607c9`  
		Last Modified: Wed, 10 Feb 2021 16:06:31 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d300df0c4477783a017efb3381849554c7ba401c9df70982305c3cad17f30be`  
		Last Modified: Wed, 10 Feb 2021 16:06:31 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0e8ca54195402ce7b355e9fe3af360fa6ab56b0d95e4b97af2d49791c72912`  
		Last Modified: Wed, 10 Feb 2021 16:06:31 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe54975704c576040bece879da194401db87213ce13eac73156f64bb1b0c93b`  
		Last Modified: Wed, 10 Feb 2021 16:06:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
