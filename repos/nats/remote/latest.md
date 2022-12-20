## `nats:latest`

```console
$ docker pull nats@sha256:d8f375976eef0d3d4b9c62d9f1e258c07d48336b4fd2e22282b03d79c66fa326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3770; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:792dc655a0bc44ad9f2e493112bb23832b72d5571ffbc49c3a18cc1201210136
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43163244a0bfe354a09aec1eaa79cc23bf6856b8edd53ce98ad748a7382f5540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 20 Dec 2022 22:20:01 GMT
COPY file:91df2c3ff0e8c9c77375df86e2577f5f0b3aaad9b932f435766b643de708c641 in /nats-server 
# Tue, 20 Dec 2022 22:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 20 Dec 2022 22:20:01 GMT
EXPOSE 4222 6222 8222
# Tue, 20 Dec 2022 22:20:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 20 Dec 2022 22:20:02 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 20 Dec 2022 22:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f7b61045ff00cf8faa9e8b18d9b98aaefe8f343e6b47539f434a2dedea5a26d7`  
		Last Modified: Tue, 20 Dec 2022 22:20:47 GMT  
		Size: 4.9 MB (4923696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72434599007ef2317a65c86d5f61154d83487286bf19b98c6f30910159f19d4`  
		Last Modified: Tue, 20 Dec 2022 22:20:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:bfdd11b14e15d804203b345b7c096af1d61167d69da33333bad0b0c02521d87e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b06e4db91ce8e59bfc1a97282eca5615a1418311f06d25f8fa9d98950adc0ec`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 20 Dec 2022 22:49:46 GMT
COPY file:1053558c802d9ad46d178dc0bcfdf685f804cd8cb5e135241d14798ca9831d45 in /nats-server 
# Tue, 20 Dec 2022 22:49:46 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 20 Dec 2022 22:49:46 GMT
EXPOSE 4222 6222 8222
# Tue, 20 Dec 2022 22:49:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 20 Dec 2022 22:49:47 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 20 Dec 2022 22:49:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:366968ad69f3d6584875c33f4e7fc9c8e184100043517abac91153bbdef1adbc`  
		Last Modified: Tue, 20 Dec 2022 22:51:16 GMT  
		Size: 4.7 MB (4687483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecfdc1ffaf24661533f96dfb0415dc625ab311ab3b58d7a5fe817df1bd40e8f`  
		Last Modified: Tue, 20 Dec 2022 22:51:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:832fc49b93f73c6efd42fe07e7b540da4c1dcb45d55136ac8a8cb7f8f10566dd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4683691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ff226e57cce59f1e3c1036f5087e2329f547a91610feea6f0d8cf984c5eff4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 20 Dec 2022 21:57:58 GMT
COPY file:0e36c1fb169284110192e7390bd636fa059a36a1e1924b06512c236ebc6c6a62 in /nats-server 
# Tue, 20 Dec 2022 21:57:58 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 20 Dec 2022 21:57:58 GMT
EXPOSE 4222 6222 8222
# Tue, 20 Dec 2022 21:57:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 20 Dec 2022 21:57:59 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 20 Dec 2022 21:57:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f816a9a44422c2372ccf828ff394ae0d5248a5794fd1ef93abcb354be9e1a208`  
		Last Modified: Tue, 20 Dec 2022 21:59:25 GMT  
		Size: 4.7 MB (4683183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fde4157bb73cd02223a27ba9f0ea84f78414d84ecadaf865bc4472326bb335`  
		Last Modified: Tue, 20 Dec 2022 21:59:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9f6f406c18a9d9dbb2bf4c18fdfc85e0e2175abd65101f967cfaef05a23ad5da
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4509478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d530339c6ef094d780314c829480d7b76e6344f58faf3e6c2a037167b10c122a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 20 Dec 2022 22:39:48 GMT
COPY file:8247c992341de8c4ae43e040a907c565b3f87352f4e9251f14a3e9f084292e1e in /nats-server 
# Tue, 20 Dec 2022 22:39:48 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 20 Dec 2022 22:39:48 GMT
EXPOSE 4222 6222 8222
# Tue, 20 Dec 2022 22:39:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 20 Dec 2022 22:39:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 20 Dec 2022 22:39:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:014d8215c73fd0fb4c0c6d526621c623107916e16019bca8fcd8c75bd023bad8`  
		Last Modified: Tue, 20 Dec 2022 22:40:34 GMT  
		Size: 4.5 MB (4508971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0787400c2bbf1006b5d01a089d7d561fb0686882f8f68d363833f334661ae34e`  
		Last Modified: Tue, 20 Dec 2022 22:40:34 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.3770; amd64

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
