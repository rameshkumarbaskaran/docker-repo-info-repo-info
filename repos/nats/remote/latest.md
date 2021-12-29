## `nats:latest`

```console
$ docker pull nats@sha256:4d4b166c324b4e9f0853e36d62cf831c5e4bd089fc6c5932ad9a98a8f73a143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2366; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2366; amd64

```console
$ docker pull nats@sha256:d5b187939141b66d0480e6dd5e3b878abd5372efc6f4f26a92b7c0029ea48056
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107547635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96befd294a3f45573c0d15724d0700dbff10edac97ede11a013bffad728168e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 04:34:39 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Sat, 18 Dec 2021 04:34:41 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Sat, 18 Dec 2021 04:34:42 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Sat, 18 Dec 2021 04:34:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Sat, 18 Dec 2021 04:34:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4f56553f84cd7b4574c0b4d1ee6585d70eda0c9f3a5f1b276ec5e7cdc713bd74`  
		Last Modified: Sat, 18 Dec 2021 08:06:40 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc8a1565220717c5c64229e0ba21ccd6622cde8482e3c124233dfa9003b60cd`  
		Last Modified: Wed, 29 Dec 2021 13:24:21 GMT  
		Size: 4.6 MB (4637251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883fbea1eb1283a4bbf26392acf172e4ef79b4ab0b4778d46f4b1a84493b1dca`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939ae0d8b1fb893c6f64343b668aa03be89852764eb042ee8803cda7f6a8cd78`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca947ae0ca6d9fe8fb291c8d5bd0fb944a8eb0d77d86744b85f13d91431ac9b3`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0aaab409f72994f4e3999f144ef170ad74faff15cb7507c2acab06bf80cf`  
		Last Modified: Wed, 29 Dec 2021 13:24:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
