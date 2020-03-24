## `traefik:maroilles`

```console
$ docker pull traefik@sha256:d8d07854fc8123227b916460903ae368a27146108df96a696b08656e5a47b52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:3dd7053eaef5072de87162644d4c14b4c6d6f10baa00e9714b9959480c3a8ba2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21578577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3e8a9c33887f506e928881e765eccd48b8535e63cf04178f8e78c1351b6c8`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 21 Feb 2020 02:50:22 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Fri, 21 Feb 2020 02:50:24 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Mon, 23 Mar 2020 20:27:01 GMT
COPY file:977e3eca412036b63f1f1b09d8388d4e5d6b3535c7af5df64ba18886ed8efd6f in / 
# Mon, 23 Mar 2020 20:27:01 GMT
EXPOSE 80
# Mon, 23 Mar 2020 20:27:01 GMT
VOLUME [/tmp]
# Mon, 23 Mar 2020 20:27:02 GMT
ENTRYPOINT ["/traefik"]
# Mon, 23 Mar 2020 20:27:02 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e40d0b92fe2d2ef50c6f43f32c33dc117ab26d69a29d74ae15725a379dbde0c2`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 131.7 KB (131682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c068c5049677b6879089396aa0d2d162ac9697e25bacf333c0596a248bae8a5`  
		Last Modified: Fri, 21 Feb 2020 02:51:04 GMT  
		Size: 327.4 KB (327376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d33f083e50ccd3f0b3af53d0e2a2c2dca2898906a953c1e2e4b14c530aefe1`  
		Last Modified: Mon, 23 Mar 2020 20:27:37 GMT  
		Size: 21.1 MB (21119519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ad05498d1d177ef22566fa16d1e9256adce71af86013d7eb9b082c1294249899
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20230021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156c24891f895dbc51607c824d2e299ff2ea302df9fc2b8962f5fdd2e4f8b1fb`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 03:46:16 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 03:46:17 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 03:46:21 GMT
COPY file:0a84c8de85d7e943231603655ccecf108fb25302c6ed1f9c6cb4f9e90c926dfb in / 
# Tue, 24 Mar 2020 03:46:22 GMT
EXPOSE 80
# Tue, 24 Mar 2020 03:46:23 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 03:46:24 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 03:46:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3ea78b0360c0223e83ecbb7336ab0de873d099e2aa889216bc3622c7dc315adc`  
		Last Modified: Tue, 24 Mar 2020 03:47:54 GMT  
		Size: 131.7 KB (131681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd374e140760994a9274b43e4cbf314b61a77acb227eca705d35780bb33a6a07`  
		Last Modified: Tue, 24 Mar 2020 03:47:55 GMT  
		Size: 327.4 KB (327405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e556ef2bd973f47fadf08d98f358fd091604a1de5409cf4a7cc8d3187623d3`  
		Last Modified: Tue, 24 Mar 2020 03:48:03 GMT  
		Size: 19.8 MB (19770935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f6a41eb9ec2b3294c6a1a65cd25e440c6f2b07a4af0b644d08c73045ae9c821c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19950885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fd16d96e8adc131956fc884a01f9e45e2adafad71b15083c3ae764b799ee9c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 24 Mar 2020 05:55:25 GMT
COPY file:c1f4ee36c6a15bdd9f8e9d8fd7b3c37c57af612bce8638eaf7a83e7873de24cb in /etc/ssl/certs/ 
# Tue, 24 Mar 2020 05:55:26 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 24 Mar 2020 05:55:28 GMT
COPY file:a3694a993cf25306aff467c03d4f70f02c07bff1afad394515f87b732cdab043 in / 
# Tue, 24 Mar 2020 05:55:29 GMT
EXPOSE 80
# Tue, 24 Mar 2020 05:55:29 GMT
VOLUME [/tmp]
# Tue, 24 Mar 2020 05:55:30 GMT
ENTRYPOINT ["/traefik"]
# Tue, 24 Mar 2020 05:55:31 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.23 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:58ceb9a2a8ba9dd83eef0c2cf887c175911b301df486d142f7d09293605add22`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 131.7 KB (131676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b9edf48787b0368bb1af04734041d3b374acefa70417bdf0090919056c874d`  
		Last Modified: Tue, 24 Mar 2020 05:56:42 GMT  
		Size: 327.4 KB (327402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8802a35e2e74e1dcf82490548042848f15ea48357d7f9c232231f94cda68ef`  
		Last Modified: Tue, 24 Mar 2020 05:56:49 GMT  
		Size: 19.5 MB (19491807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
