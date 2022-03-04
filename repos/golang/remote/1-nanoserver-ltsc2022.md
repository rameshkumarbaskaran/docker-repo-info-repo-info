## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:57936c972af1eea1ae435c97b758451cf517c467458e2c995ce388d3cc4fa0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.524; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.524; amd64

```console
$ docker pull golang@sha256:2a655f042ad37a7f76bb4571799810ecf4f2bbb5b56bd8a0e868fe90fac4c18e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262794764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2006cd5ec8f7ec0af809ea4297f38d6e1ed95e2005d33cf66e2ddfa2e75386`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 13:48:34 GMT
SHELL [cmd /S /C]
# Wed, 09 Feb 2022 13:48:35 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:48:36 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 13:49:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Feb 2022 13:49:22 GMT
USER ContainerUser
# Thu, 03 Mar 2022 23:23:49 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:25:58 GMT
COPY dir:30287e5480cb94d00aba798bdf22cad49bb2ae2de25f97441d1d8401e0571f4d in C:\Program Files\Go 
# Thu, 03 Mar 2022 23:26:58 GMT
RUN go version
# Thu, 03 Mar 2022 23:26:59 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d52811c4b439c00c93423790e004fc266374135015625d93ffb80def500d7b64`  
		Last Modified: Wed, 09 Feb 2022 14:34:32 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263041b42d7aee90b2defa92fc60f7db99cbbb4686f589864f236b46225ac2a3`  
		Last Modified: Wed, 09 Feb 2022 14:34:31 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0167ac52d6f1254de3c047db124eaa082939ef069a8951247813c10025676d6b`  
		Last Modified: Wed, 09 Feb 2022 14:34:31 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95619fbd5e91dcd251f92bd790e401d548ac0352fc1c7ec9b7a17fd0e46cfdf3`  
		Last Modified: Wed, 09 Feb 2022 14:34:32 GMT  
		Size: 87.2 KB (87240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c044d79e4b1aeb1f8dfdb389f38af55837434f7ff54f3b66176470da6c2c8c`  
		Last Modified: Wed, 09 Feb 2022 14:34:29 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae8b4c6f34656dbd0f2fe1b9ea206e2bc9c4a5bba983d01c5f2f06c4827c41c`  
		Last Modified: Thu, 03 Mar 2022 23:48:42 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25216ee82c98e79fbddb413d06499b22eaca6a5c4dd308d4ab434d96c04c5651`  
		Last Modified: Thu, 03 Mar 2022 23:51:10 GMT  
		Size: 145.2 MB (145198302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aab4242c36892f6e036e536b2b9cf1fd26ae60f1d714458108c30e034692232`  
		Last Modified: Thu, 03 Mar 2022 23:48:42 GMT  
		Size: 44.5 KB (44482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdc2aa11aa75910b766ed58a39ceceb83a7342454a39d7803a27c727255713d`  
		Last Modified: Thu, 03 Mar 2022 23:48:42 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
