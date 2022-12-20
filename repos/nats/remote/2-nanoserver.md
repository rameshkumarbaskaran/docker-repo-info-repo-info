## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:a077b97e3f91e599c0780fda4a14e571812c2a82e67a1fcf140a37161fa6a148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:485bcc363beccc6b7ab11095344ecab9b21883699c8708b8a9850a9a25faefc2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111654858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4a34f42c47928f922d9a0b86b390dbd3109ab2ef45cf324bfbf94e07a645b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 02:41:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 20 Dec 2022 22:20:11 GMT
RUN cmd /S /C #(nop) COPY file:699b8f46651a6b1f508b703e66aba9e4026441d03f5c5230616470e2e75ed34a in C:\nats-server.exe 
# Tue, 20 Dec 2022 22:20:12 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 20 Dec 2022 22:20:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 20 Dec 2022 22:20:13 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 20 Dec 2022 22:20:14 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e9d361872b14736e9b1544993bd1f54f9284833fe47bff0ed4a51b726c47d8`  
		Last Modified: Wed, 14 Dec 2022 02:42:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d632860cbb5d5b5381cdbe4e66db4fb3cace8d1aa0643a2be7eb0995af9a5`  
		Last Modified: Tue, 20 Dec 2022 22:20:58 GMT  
		Size: 5.0 MB (4977419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79275989cfc855788150f25a13286ae24af460daf970afbb6be25084a972d2a1`  
		Last Modified: Tue, 20 Dec 2022 22:20:57 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8a1fc39ddc3a97d353c0bd42c85a85a8e98326f093a2affecef1034d36b320`  
		Last Modified: Tue, 20 Dec 2022 22:20:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b717649059d79c8ce10edc3c840b5c30739772c982ac304f0d9ee83d260f6`  
		Last Modified: Tue, 20 Dec 2022 22:20:57 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b93a7a10958e4023b1e3157f8c27e228a974109978ec1cdd9076201e86a74`  
		Last Modified: Tue, 20 Dec 2022 22:20:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
