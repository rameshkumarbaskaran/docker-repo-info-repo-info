## `nats:latest`

```console
$ docker pull nats@sha256:178f84bff4dab5a40bf69ba0a004b2a93b54aef07e24236bccd933fea56ed5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2565; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:99183db21c5915cd7a09ddeff053a2cbd894ac0309055d7057559c687a3cc9d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7d4b6b9b8026e958bf3cbfa8f505cdb1117492e18364d8530de08280c9084d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:82e16305486574a60ef2430a32e2aa62cda93d6ee9c8a92c59514c51ca83cc65 in /nats-server 
# Sat, 05 Feb 2022 05:59:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 05:59:57 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 05:59:57 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 05:59:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:08e24ae16feab2f7411aaa3a7fded7b24379848fd5805dc619dbd8d5ab3f5544`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 4.5 MB (4480984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c77338b2b1d179ee70d5ae5db8d09e23a30791b19bc29adefd175a6a0209db`  
		Last Modified: Sat, 05 Feb 2022 06:00:49 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8eaacddefbb77330f27386b955043e951c520493811549b86f17532aaa3d369a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63e99a35399073e64fad21463fa8feb722f9cf0be282442a5266ade57ac1c71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:ab57498beb47554f59d41e48de205afc83ec0484942f9d333171fd2683b75527 in /nats-server 
# Sat, 05 Feb 2022 00:58:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 00:58:27 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 00:58:28 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 00:58:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:12b2ccca539636b986824725c5c6ea2783956bd56f6bd5331d7fa1710d8c1ef4`  
		Last Modified: Sat, 05 Feb 2022 01:00:49 GMT  
		Size: 4.1 MB (4146457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc869410e8f891bf74a9a130508359a16a91d75ee2e000a8df7777ad6229c3f5`  
		Last Modified: Sat, 05 Feb 2022 01:00:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:d51d5ebf3e45bc75fb311e19c4fce37493c67ad963565fd7ab500e2d9038cd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4140284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a62bc8b93a75210716447a48eb1e3303e5a800f8e3a5a7ce89faf504ca12c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 06:12:54 GMT
COPY file:fdac7f170b947c702f4d76227a1a0822a7483091f22a271692632f02f0c84a2f in /nats-server 
# Sat, 05 Feb 2022 06:12:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 06:12:55 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 06:12:55 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 06:12:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e44a6e98809966c949c9996cc79c25550e6992ba0f1167cef80bf80834f1b52e`  
		Last Modified: Sat, 05 Feb 2022 06:15:17 GMT  
		Size: 4.1 MB (4139776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2c7c3e60dfea58933554c4c1e9f4c7fe2fd9d017c3ee0521b4deee23a61885`  
		Last Modified: Sat, 05 Feb 2022 06:15:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:bbc12315f623dda9d2b116a35b7d740b1c9dbcf774ec1b170a9a1b1338b1d572
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39f509ff5ad481fefb3fbc1386564ba8be085d7c0a0de4858d9914b1a186ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 05 Feb 2022 04:09:04 GMT
COPY file:0acdeef31553bbb6797a82f6f78cb4c9d65b6d4f05e0718bb05947999b409369 in /nats-server 
# Sat, 05 Feb 2022 04:09:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 05 Feb 2022 04:09:05 GMT
EXPOSE 4222 6222 8222
# Sat, 05 Feb 2022 04:09:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 05 Feb 2022 04:09:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e59aa3fa3a53fd27190bc2a229a77179ce9d65dcbdc0b5a0a0d78f7bc6921f9`  
		Last Modified: Sat, 05 Feb 2022 04:10:21 GMT  
		Size: 4.1 MB (4125780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885795371491925b55e5a0dde4a803cd8bea1fed30e054808bc7462a1c63e199`  
		Last Modified: Sat, 05 Feb 2022 04:10:20 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2565; amd64

```console
$ docker pull nats@sha256:7a1ab2e6e8274fa48286f74bdc4049613f4a195b106ad60b1c20d639a7d9e6eb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107616018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65a67e57e8400b4d29c0ad5699f7a280a95dfa3f515fcf965c4bacd3f16c3a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 09 Feb 2022 20:51:18 GMT
RUN cmd /S /C #(nop) COPY file:22259e2260770ea5dd451a0236981db746473d05f765b470bed0fc5501da9c83 in C:\nats-server.exe 
# Wed, 09 Feb 2022 20:51:19 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 09 Feb 2022 20:51:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 09 Feb 2022 20:51:21 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8bc49c59cde14e3a9ed8fedce001c00fcb5fe0f9b914aa07273e04f23333d180`  
		Last Modified: Wed, 09 Feb 2022 18:14:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b72f9873a54f539c487aadc8937ae832cd2cffdd1af06f368629e058518ef`  
		Last Modified: Wed, 09 Feb 2022 20:52:11 GMT  
		Size: 4.5 MB (4522598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a10b192969d99c1eceb2713eeff85e1048113487b44dafa3d2012754fbdba`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e12c5402b38a673c9ae6c7de6d41c4f00a6c575f7e94336c5d9235c733efe2`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17a4d20c99029a251a506f8c1b304cb89fbd352d8e4f0729834fae9e52cf3d`  
		Last Modified: Wed, 09 Feb 2022 20:52:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adde8dc40298e7b0637e0543056d95dd5bb5ad4c8db8a6017be7b49527cfd58f`  
		Last Modified: Wed, 09 Feb 2022 20:52:06 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
