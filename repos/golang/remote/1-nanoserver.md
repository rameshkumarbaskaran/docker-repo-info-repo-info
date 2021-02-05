## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:50470631c61e6fba1882d4c85b1a0ce471479c91a75a6d8115c8999e5653cd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `golang:1-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull golang@sha256:844743e315f6fae80a5316485bd1c4a5cc4623d0a2921a2d22381412c3b44395
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235228782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa71ff22870063084cea77128fc8ced5c87731b06968e94afe2fb7fd4196ed8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 13:44:35 GMT
SHELL [cmd /S /C]
# Wed, 13 Jan 2021 13:44:36 GMT
ENV GOPATH=C:\gopath
# Wed, 13 Jan 2021 13:44:37 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 13:44:52 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 13 Jan 2021 13:44:53 GMT
USER ContainerUser
# Fri, 05 Feb 2021 02:21:28 GMT
ENV GOLANG_VERSION=1.15.8
# Fri, 05 Feb 2021 02:22:45 GMT
COPY dir:aec6cdae9917bad4591f4d27c24de6518df53d6a67afe566e8896690025b9de7 in C:\go 
# Fri, 05 Feb 2021 02:22:55 GMT
RUN go version
# Fri, 05 Feb 2021 02:22:56 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50358a323c5421695eacfec8cf19b70cfc54a72e6dc491bc2bfd4391d84dcaf9`  
		Last Modified: Wed, 13 Jan 2021 15:13:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7b504f15f2836681dc74e6bf27d7be538fe7e6a6f53ea4bf3d8be6bb6545d8`  
		Last Modified: Wed, 13 Jan 2021 15:13:44 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf6648d03a5b65f08b03a3cf89c0de5e57b386f48c5316121c697a7d4f12488`  
		Last Modified: Wed, 13 Jan 2021 15:13:43 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc9022e2634f8a89707e4bfa55b2ff2a86865a3d7e5508effdc4abd5e92405`  
		Last Modified: Wed, 13 Jan 2021 15:13:43 GMT  
		Size: 66.3 KB (66267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3d33148024d9121b1452536b9df85f11745d7d415b1537823e481164375713`  
		Last Modified: Wed, 13 Jan 2021 15:13:38 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd4cb145046baac1a69056327ec616831eebf3e46c946b0b4046042d8d2631`  
		Last Modified: Fri, 05 Feb 2021 02:33:04 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732abd43d6c210100cc22d0106aa108d260b4d2e078966a904789faaafd51aa3`  
		Last Modified: Fri, 05 Feb 2021 02:33:33 GMT  
		Size: 133.7 MB (133743353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca5bc09ae2c96528a7ce574bd2a2a46a00ae1b4488f166eab599bd6e0a562fc`  
		Last Modified: Fri, 05 Feb 2021 02:33:04 GMT  
		Size: 73.2 KB (73206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53285eb8c909c1881ab8dc5ea1968faeb03c2b0f3f5fd61e67f0d0f364466aba`  
		Last Modified: Fri, 05 Feb 2021 02:33:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
