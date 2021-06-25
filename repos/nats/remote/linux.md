## `nats:linux`

```console
$ docker pull nats@sha256:b19cd92c64f6da8bc0e1d4ed95176cee036d72a0c1a0ac3b8a1f0859fced9b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:9ee8674607d72a7993a833da50a04bb798dc906079f7d4a3ff386ae9c7dad1b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24690f4c9243082798de0d5d0dcf537f0d65e65ba0e4c324f576019af6e88b71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:574cacffaccc18c0ebb219863832f97c5b4a301f1311490b79ebc4f7c91df1c5 in /nats-server 
# Thu, 24 Jun 2021 18:20:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 18:20:54 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:55 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 18:20:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ff7c72aa6eac78de3e8d419804aa418bec0a1d109825baafe6f27f8d5463c862`  
		Last Modified: Thu, 24 Jun 2021 18:21:47 GMT  
		Size: 4.3 MB (4335042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2e05cfe23a1b83926a7784d3a6f32ee581b1b20019023a53e605a28e098280`  
		Last Modified: Thu, 24 Jun 2021 18:21:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4d7fa672d2e979a1f71013d6c0ced4762a775e52c5fa1c597061e0661a4f564
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818a3d14ec5abc722d14eefa80fd1bbb0cf49078b6a2fb3e54632e211c176c9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:f297049dd293f8bd69f8b37a6337b711a278a532e801780056f74049b995408b in /nats-server 
# Thu, 24 Jun 2021 19:17:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:17:28 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:29 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:17:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f861ae2df753d566752887dd69fa7c0770cc5d866cf63d89323d119e6e132631`  
		Last Modified: Thu, 24 Jun 2021 19:20:11 GMT  
		Size: 4.0 MB (3992918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ea4dc62b81dd101ec8289e6ef95821857d589dd412611e32dd41affe68138`  
		Last Modified: Thu, 24 Jun 2021 19:20:08 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:593e1b418f3e55050730f63b1d5da6e5f6f9c990c66e15bb9cd6659ea836279f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3914539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4093ac9e36206435159f30858c34c7ed656e69e8dcbe1aaa6fbd40099701ade7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 25 May 2021 22:23:02 GMT
COPY file:1ccce8553c778be1204380469e7248fd9ee472bdec35db0b7dd150122ae7c37d in /nats-server 
# Tue, 25 May 2021 22:23:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 25 May 2021 22:23:03 GMT
EXPOSE 4222 6222 8222
# Tue, 25 May 2021 22:23:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 25 May 2021 22:23:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a459b50ce258c1a3884cfc6f671ebabe9d05421a39962966809134623f3b9979`  
		Last Modified: Tue, 25 May 2021 22:24:59 GMT  
		Size: 3.9 MB (3914063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1808b616cb182b07285cb2e4b7d289755ccf8fa8575a8bc73a20ae46f8f253a`  
		Last Modified: Tue, 25 May 2021 22:24:58 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:9af64abe7058267802b82eea320c8900f01e2900fc14c7819215cc38249b6a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b6ba9c13a2b4e06ce837ee797073c343df1705b660c37b3331e4afc500b19e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:5beb421ec5105e31f6e0b0a14e99795c4d0ca457385b898e67e502f8c1168b1c in /nats-server 
# Thu, 24 Jun 2021 19:07:11 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 24 Jun 2021 19:07:11 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:07:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 24 Jun 2021 19:07:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4fa9662b0eb20e8acff5f956ac375b9e6d6bae55ed10b15783f5bdea6e212ca2`  
		Last Modified: Thu, 24 Jun 2021 19:08:34 GMT  
		Size: 4.0 MB (3958114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae902de5ccdf10f5ab555454aaf3ce99d7642bbc3961ef684412f5d45cd03ab`  
		Last Modified: Thu, 24 Jun 2021 19:08:33 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
