## `golang:nanoserver`

```console
$ docker pull golang@sha256:12dc1d1fdd5f8d28789347ca5aa26669510bb67c0520bafc3b7d600e89f8aeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `golang:nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull golang@sha256:bd3cbb7b1bc03394e0ac196e293acb8a3deb6ad4560be4e3d5afb1f279b68123
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234147707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe0bf6b66eeb3524455dd448c78595050f5d0e90b441cce059da49b5890fbf8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:45:59 GMT
SHELL [cmd /S /C]
# Wed, 13 May 2020 12:45:59 GMT
ENV GOPATH=C:\gopath
# Wed, 13 May 2020 12:46:00 GMT
USER ContainerAdministrator
# Wed, 13 May 2020 12:46:16 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 13 May 2020 12:46:17 GMT
USER ContainerUser
# Wed, 13 May 2020 12:46:18 GMT
ENV GOLANG_VERSION=1.14.2
# Wed, 13 May 2020 12:48:31 GMT
COPY dir:cedee7ee5ff520e4aa4bf8ec004e9eba31ccdfd2a912466d83949af88a223e83 in C:\go 
# Wed, 13 May 2020 12:48:47 GMT
RUN go version
# Wed, 13 May 2020 12:48:48 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40353fa5ada037c8e7ee420534fa5382bdfbaf02e1076b13aed24281de55c455`  
		Last Modified: Wed, 13 May 2020 13:01:02 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a72d54d9d133d3699eb985ab2185f853990987e9d27b7684a1cc85b1e4b104`  
		Last Modified: Wed, 13 May 2020 13:01:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508740f077f04bd716c91abe093629a4f879980cea83d172b1f5f6a4c0e64ba9`  
		Last Modified: Wed, 13 May 2020 13:01:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e75b0268a2f057e874739401fafa440f9012b282a6477518fcb223c83a6fe2`  
		Last Modified: Wed, 13 May 2020 13:01:01 GMT  
		Size: 66.7 KB (66723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe006cd051b4870a7d6b5390952c199763bc0bb76c7885f7ef2ac62a74250b`  
		Last Modified: Wed, 13 May 2020 13:00:59 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b120a55c6d9c4902ea24674ec4c8e0298ec3efd1017b0b6ec0b2aff13664a76a`  
		Last Modified: Wed, 13 May 2020 13:00:58 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc46accb9e08428505e70ccb34ad83891e31e0b1c91aad81681356891a2010b`  
		Last Modified: Wed, 13 May 2020 13:01:26 GMT  
		Size: 133.0 MB (132982582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1afcc1e8fa6a88eb1c0df23397af759ecd1fedc1050878588f82b0e20e45b1`  
		Last Modified: Wed, 13 May 2020 13:00:58 GMT  
		Size: 73.0 KB (73025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02df649a27eec9cd7c9631eb56c3a9b8905da6f7aee96db996aa15d300ab5160`  
		Last Modified: Wed, 13 May 2020 13:00:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
