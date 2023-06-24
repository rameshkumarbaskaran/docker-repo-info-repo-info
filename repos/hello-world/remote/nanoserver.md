## `hello-world:nanoserver`

```console
$ docker pull hello-world@sha256:f1f987d0d47bf24cf7451fbb1f587da8d9e1e3f1859f0d1ab87a99c86496c7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `hello-world:nanoserver` - windows version 10.0.20348.1787; amd64

```console
$ docker pull hello-world@sha256:303fb1d919cb6d9264b1c000c6b2d9afc8f71479fec1e55275a1ea03d9fb61cc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120031174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f613ae3fb95a1afeb9711f86b5ef99c1b2455a061c764b700d364d024c57266`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 21 Jun 2023 07:39:21 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 02:24:50 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Sat, 24 Jun 2023 02:24:51 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:d6e77b89ecdadfdd3ef274e9a235590c9cd4dc832939932eff32f93250571005`  
		Last Modified: Fri, 23 Jun 2023 07:43:32 GMT  
		Size: 120.0 MB (120028254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5700f1dfe23df22e3e987e17a6fcd39f40e1adc9a83aeb7f75a9c0c8835f4cb`  
		Last Modified: Sat, 24 Jun 2023 02:25:12 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9732585770d05ddc50c0de29703952c3225de35bff32aca44f278225aa08b0`  
		Last Modified: Sat, 24 Jun 2023 02:25:12 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hello-world:nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull hello-world@sha256:7ceee8982e466968344d8ce47f1d4e70f78083e2f11ce2d3825d1c7e9a1ee462
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104403745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c85d0ed89b796e96bf64030e05fd916fbd4ccf5354012188f7dadd21b0be26`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 02:24:57 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Sat, 24 Jun 2023 02:24:57 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5649b34606045ba7e2cd5723b4e64f448405468787095dcd1e69cf9ed00a8a6d`  
		Last Modified: Sat, 24 Jun 2023 02:25:18 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea6225d2d815d2344494ed633501a07fbcc62d14bbb0733c661feaec95e8439`  
		Last Modified: Sat, 24 Jun 2023 02:25:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
