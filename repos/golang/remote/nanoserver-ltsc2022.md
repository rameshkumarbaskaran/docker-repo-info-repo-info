## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:21817acb2d183c9227bea086cc87a6bdb82481123b40f99a2abf67ce98b3d011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull golang@sha256:df5d470db433f673d4e669988163e8c516bed6ab878c4ba9c8e8aafb107d712c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (270035785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f6a480348e67076b89bce6211923277a3894a1878879a69b8a0867e1c38ba5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 03 Apr 2022 05:29:07 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Apr 2022 02:43:38 GMT
SHELL [cmd /S /C]
# Wed, 13 Apr 2022 02:43:39 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:43:39 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 02:44:31 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 Apr 2022 02:44:31 GMT
USER ContainerUser
# Wed, 13 Apr 2022 02:44:32 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:46:59 GMT
COPY dir:a9b45ca01f58effecbb8cb70f3a197420158293686993992aa72e6e0b30f6c79 in C:\Program Files\Go 
# Wed, 13 Apr 2022 02:47:51 GMT
RUN go version
# Wed, 13 Apr 2022 02:47:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:5ee98801bdad72bc36678d072c89f7dd482fee29086c1d9c8ad6ff0cb5afa385`  
		Size: 117.6 MB (117579416 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0ae7f8fcefe8f9cd0745bf20258e1950e1c72b8ca86cc031fca90ec3e24203e`  
		Last Modified: Wed, 13 Apr 2022 03:16:38 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd9cc0efd13f2a7ee80907e5303d679c50a0ee6d80cb4e3997eb48b6194f2fd`  
		Last Modified: Wed, 13 Apr 2022 03:16:38 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cfa5b462ce5e34ee95d0ff0107af5a0dfb914b3cbd6b7ecefad7476112b6ea`  
		Last Modified: Wed, 13 Apr 2022 03:16:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8733747372bd79deaccf5a82ec8b57a002081723e7979288db8f2b3aae91d32d`  
		Last Modified: Wed, 13 Apr 2022 03:16:38 GMT  
		Size: 87.0 KB (87043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2146cdbbd790d711c33d79892c675d8b46f157e9e9379d65ff23961cc6753fd6`  
		Last Modified: Wed, 13 Apr 2022 03:16:35 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d353a757968db5680cabbcca53c407820e2a8a0633d7b2042cb37a6aed458f48`  
		Last Modified: Wed, 13 Apr 2022 03:16:35 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edbcdd189da2b57b631171df85c105697b2eea5c8f539fa7299fbd23f50fefb`  
		Last Modified: Wed, 13 Apr 2022 03:17:31 GMT  
		Size: 152.3 MB (152308838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3eea41d79bc75af2ad20bdbb120dde902d9554fee812f85b94da1fa766390e`  
		Last Modified: Wed, 13 Apr 2022 03:16:35 GMT  
		Size: 53.4 KB (53357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e796fabd1f1554254b910cf31035a870c616608f7aefa4422d89af9c6107932f`  
		Last Modified: Wed, 13 Apr 2022 03:16:35 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
