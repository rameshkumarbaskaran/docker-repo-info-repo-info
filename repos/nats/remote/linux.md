## `nats:linux`

```console
$ docker pull nats@sha256:0e3da4bd4949f156933e44268ff3e81307b1715fe8a8f4c78885f08a11806326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:35ff92bfc7e822eab96fe3d712164f6b547c3acffc8691b80528d334283849ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4535346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165538b9f99adf71764e6e01627236bc7de03587ef8c39b621c159491466465e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 03:35:09 GMT
COPY file:c88c76fcaa944eb4751e2b3c987b59dd654a42db7426be2223f22a0698cd6e5c in /nats-server 
# Fri, 27 Aug 2021 03:35:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 27 Aug 2021 03:35:09 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 03:35:10 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Aug 2021 03:35:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d96e79a5881296813985815a1fa73e2441e72769541b1fb32a0e14f2acf4d659`  
		Last Modified: Fri, 27 Aug 2021 03:36:00 GMT  
		Size: 4.5 MB (4534870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04479ea8ab2597ba1679773da48df06a9e646e3e7b67b0eb2c8c0bc6c51eb598`  
		Last Modified: Fri, 27 Aug 2021 03:35:59 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7201c8cd794776fa392c3a25eb89e4ee987aeaaae647caa364621d5daf5ca3c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4201703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2211a135c8d5c9641c74ba5d54c3c1df4ac3f24fa70a6a57be8a2975af7854`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 02:48:56 GMT
COPY file:81d7dcb1f2223ae767ee02f3b24758797ca55a665d17dcb2054eeb097fb2eafa in /nats-server 
# Fri, 27 Aug 2021 02:48:56 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 27 Aug 2021 02:48:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 02:48:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Aug 2021 02:48:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a820d11a96d84195887c44533ffcad67997fcb79d52f4564709bfdbde47d578d`  
		Last Modified: Fri, 27 Aug 2021 02:51:18 GMT  
		Size: 4.2 MB (4201229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1c4f82bf849dc3d9d18f1c560b9afd0e5237eb2f05377e6792dda2480249cb`  
		Last Modified: Fri, 27 Aug 2021 02:51:15 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f2057644b631cd588b9ef8800c17a98848297ef9e8b14e896c6637c419716372
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4196286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e34b9a7771c2092b58b5d6f99401eee0374e56201d34a1c7f84d6f53c05428`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 04:12:30 GMT
COPY file:6576d0950936fbd8cd0ba8e9a7c8094950f25bd1a90d55b60e3e65ea2042854c in /nats-server 
# Fri, 27 Aug 2021 04:12:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 27 Aug 2021 04:12:31 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 04:12:32 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Aug 2021 04:12:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d135e76e7d6d665dbc290a175c8ae8ecfb2ca0aa9f3a2ba24b7dccf731e64cde`  
		Last Modified: Fri, 27 Aug 2021 04:14:54 GMT  
		Size: 4.2 MB (4195812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc14281759482e956b9f087159fb1610c9a80c3fe13daec5850693cafea3d3d`  
		Last Modified: Fri, 27 Aug 2021 04:14:51 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f5540c14ed29a1ef1c754918bc89f829f49fd6580803a9219f5d1cd554338b6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56533e4f95e8c4154db8d7717a0b0435a0ce0888125cfd0e4087543db765a6bc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 03:19:15 GMT
COPY file:61407b2494616881c09d27c01bdb5a1169dbf9163831a2352284c5578e6cdaad in /nats-server 
# Fri, 27 Aug 2021 03:19:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 27 Aug 2021 03:19:16 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 03:19:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Aug 2021 03:19:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3c5d1fa5c137082797b53a6d9ed69aceb52e853695ee3bf824776ad6f0d2b753`  
		Last Modified: Fri, 27 Aug 2021 03:20:37 GMT  
		Size: 4.1 MB (4147902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbae3f13cb6757dadd56bd833076486ed81b2c1c87b7b3ca721e459d8f477b6`  
		Last Modified: Fri, 27 Aug 2021 03:20:36 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
