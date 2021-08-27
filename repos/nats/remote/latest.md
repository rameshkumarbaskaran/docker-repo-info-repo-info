## `nats:latest`

```console
$ docker pull nats@sha256:45ba1e75b73aa90e7005aa09c5991b299bf4a5523d5ceaa0644005aea14bd0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2114; amd64

### `nats:latest` - linux; amd64

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

### `nats:latest` - linux; arm variant v6

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

### `nats:latest` - linux; arm variant v7

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

### `nats:latest` - linux; arm64 variant v8

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

### `nats:latest` - windows version 10.0.17763.2114; amd64

```console
$ docker pull nats@sha256:9c370308b1924738df19dd502a9d8d8c13066580fd1550eddbf4f70663c87fe5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107338949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90920ed24cf8337e7f99fdd7199bff8ec7dd43cfa5063f0f373e6700f8a17a2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 25 Aug 2021 16:07:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 27 Aug 2021 00:16:45 GMT
RUN cmd /S /C #(nop) COPY file:bafd3fc1559b39648f01fab1b3b19a9fc9bb95afae5b07b1d7987b376806e053 in C:\nats-server.exe 
# Fri, 27 Aug 2021 00:16:46 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 27 Aug 2021 00:16:47 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 00:16:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 27 Aug 2021 00:16:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae8616c17f5cca409a4b1289387e37dc532657ba2b52bb60713ff621acccd506`  
		Last Modified: Wed, 25 Aug 2021 16:11:20 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb815244c76bae445a6697a3f1b6a0643fc016be2b2da5192dc6bb4079cd0119`  
		Last Modified: Fri, 27 Aug 2021 00:20:21 GMT  
		Size: 4.6 MB (4591622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33193ffa3c81a2ebd95cb6af96ce80ee557191a64ba47e1977479e1167530ca`  
		Last Modified: Fri, 27 Aug 2021 00:20:19 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c57e2e68d87e03a37f706b01fe403fc34435b82da71d1080e11ec9df4d418a2`  
		Last Modified: Fri, 27 Aug 2021 00:20:19 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b1707f600e77fb06d48bd9c3759cad471944658bdfa3dd59b2852dc7983b4`  
		Last Modified: Fri, 27 Aug 2021 00:20:20 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b434e68e7546ed285144b98ef8fc3a10f1b6ee578ef2503e9f09aefab0370d0`  
		Last Modified: Fri, 27 Aug 2021 00:20:20 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
