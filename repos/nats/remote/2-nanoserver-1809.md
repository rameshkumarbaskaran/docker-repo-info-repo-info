## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:bee61031342613281257ab17f1396448cd5b042e4000cae69c2c4a43edae2684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull nats@sha256:0df80931742b945706d67b27200633771bbdb6ed1589f9cc70b008d6e50a622a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108296874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fdd7f70bf36b4bb5cb925f450fd51dcea2048ccc882dddfb6e2d18cc4a0f8f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 15:41:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 23 Sep 2022 00:27:48 GMT
RUN cmd /S /C #(nop) COPY file:41c74b7fec0394cfda2a0d22981dcf87c21403477b886f1e77ee32cfcf17c618 in C:\nats-server.exe 
# Fri, 23 Sep 2022 00:27:49 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 23 Sep 2022 00:27:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 23 Sep 2022 00:27:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b6bda313a93b8c355d5adf6e15f4b805f705c3741b235a7e4644bbffe6a6af3d`  
		Last Modified: Wed, 14 Sep 2022 15:42:30 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e045b06d720368f39939e6ba0eca42fc73ea6d507102319925e8de4c019cbe44`  
		Last Modified: Fri, 23 Sep 2022 00:28:40 GMT  
		Size: 5.0 MB (4956222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aac1cac27956471e7f10da9cb370cac2cc3009795f5c44adcbbf46b10c1a7c`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0ea2b7b2f77e07b75f2a6987bf7030ccdac83bcf89c34dfec268e3eefacbad`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ad20b77628af1f8a9af7de87c001e6c9abede83d98f34a2121af5de543c1cc`  
		Last Modified: Fri, 23 Sep 2022 00:28:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71cfb960851a0ce2890be343bcd094837beed3e170d068f953922e526b4225`  
		Last Modified: Fri, 23 Sep 2022 00:28:38 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
