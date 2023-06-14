## `nats:latest`

```console
$ docker pull nats@sha256:40d48cba5bed37f53983436599567d26d6840d6e9bc5d30f2e33041b8a38b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4499; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:a745065ae9a8f32cc91b2071488c1f59436f5f37f34c7c6b8cc92151faa0e3f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5890e892d1ad969919c44edd59234aba90bed05efa593466e4febb8894ffcdd0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 04:35:22 GMT
COPY file:b153b1503cf6a82c5cc80b44ddaff7ccc3405ac7d7709c9b40a9e173ba2f50f1 in /nats-server 
# Wed, 14 Jun 2023 04:35:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 14 Jun 2023 04:35:22 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jun 2023 04:35:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 14 Jun 2023 04:35:23 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 14 Jun 2023 04:35:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8b0c326d1b5e38f75b5b85a41c0a33b3dded3024fc094e69c586e8502027c3e3`  
		Last Modified: Wed, 14 Jun 2023 04:36:07 GMT  
		Size: 5.1 MB (5121932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7c6ae7a938b576ab8648f86530b510f2be9541d3822aa3378fc924927f2fbf`  
		Last Modified: Wed, 14 Jun 2023 04:36:06 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:f26f23aad2feedaeaca9df38eca5559b431fbb8ed841789b1e6b2c3c84ffa79b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae95e37599ef924cfe3d5890b3af209e09951179f6672d35af6811876e61253`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 13 Jun 2023 21:49:33 GMT
COPY file:e5bb5e8247a1c4bdb92d70dc84443f615728207816f4c76763893029e98fe987 in /nats-server 
# Tue, 13 Jun 2023 21:49:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 13 Jun 2023 21:49:33 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Jun 2023 21:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 13 Jun 2023 21:49:33 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 13 Jun 2023 21:49:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7f1a7a7f3e313c163918678d53d48af6476087e63070356ad38ff1c041606bca`  
		Last Modified: Tue, 13 Jun 2023 21:50:13 GMT  
		Size: 4.9 MB (4884348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af05a149bcbd29ea7705539c8b49e2c00b5883848519f3929bf4c4dc424022e`  
		Last Modified: Tue, 13 Jun 2023 21:50:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:ddf36c6f5382250cf0c060174d558e0baa7f3476a02202f6f2c62704d8c2291f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4876509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106a7db0d6aeb34de7f7373b5a9730cae54001f06148c1cd6009bf01bfa9f33`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 14 Jun 2023 04:52:17 GMT
COPY file:e75b1e12b729f292a57f2d1659447109dff58c1d8490e106b86376f59145089b in /nats-server 
# Wed, 14 Jun 2023 04:52:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 14 Jun 2023 04:52:17 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jun 2023 04:52:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 14 Jun 2023 04:52:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 14 Jun 2023 04:52:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea8b2adaa2a72f51d0db4333759ca7e2991e083292d08571a49ee462a01d9068`  
		Last Modified: Wed, 14 Jun 2023 04:52:54 GMT  
		Size: 4.9 MB (4876001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9750ae1eb25bd2c63839e3ccde3cd9f97e8556cc9b72a65afa7463bd715448`  
		Last Modified: Wed, 14 Jun 2023 04:52:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:edbf69c3a8dab18af6eefffc70fcea84205a4397632e23fbde4cca5fe03446ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b395b40ae1ff951faa10f8f5c05810b77b0a03c2ef5a8eaa8bc443497b52348d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 13 Jun 2023 22:34:13 GMT
COPY file:0fec8537fba7c573dbe20b854a6b32d8b0940e46f9e81c41611d447b82a034bc in /nats-server 
# Tue, 13 Jun 2023 22:34:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 13 Jun 2023 22:34:13 GMT
EXPOSE 4222 6222 8222
# Tue, 13 Jun 2023 22:34:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 13 Jun 2023 22:34:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 13 Jun 2023 22:34:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2cce796fcd5a4e60d6ca871c71b29485d80a6babd1c43a056db0b52aa6e904b6`  
		Last Modified: Tue, 13 Jun 2023 22:34:58 GMT  
		Size: 4.7 MB (4687516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22153c0efa275cbe62c344213d16db73c5732467534b2a316e379bdd77324d29`  
		Last Modified: Tue, 13 Jun 2023 22:34:57 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats@sha256:6e78b57a2010189c5b419130055b295f0b45ffd01d9d693e473a8b0455b04931
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109577889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f78f2040b93146d50e68bca77f438d15f51186b7b5d264c5aff87781bffe5ff`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:19:04 GMT
RUN cmd /S /C #(nop) COPY file:e92fb324fb1e715aaa4f213ef42afe80c4a76690e3b2d439bee510cb2ae47cd5 in C:\nats-server.exe 
# Wed, 14 Jun 2023 20:19:04 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Jun 2023 20:19:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 Jun 2023 20:19:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jun 2023 20:19:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa91c896c6fb45a9c5f783f062b792391b211d8d17964941c5352cf6858b2a5`  
		Last Modified: Wed, 14 Jun 2023 20:19:49 GMT  
		Size: 5.2 MB (5174009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5c072b8b934a1081d0260d8379c92eea084db8d38a9dd214b4ea3899a6e16b`  
		Last Modified: Wed, 14 Jun 2023 20:19:48 GMT  
		Size: 1.7 KB (1662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6082349db6622caea203da789c29a17747b2739c95012aaa531888976e1201b`  
		Last Modified: Wed, 14 Jun 2023 20:19:48 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac5b8008f5ff928e6f1b971f089660417ed155b4f5a79843cf73a03e08a103`  
		Last Modified: Wed, 14 Jun 2023 20:19:48 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536d4c38572e98e3b7b614620d8ba6a0b1186e628f440e2d3aa9cc354d7e75a`  
		Last Modified: Wed, 14 Jun 2023 20:19:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
