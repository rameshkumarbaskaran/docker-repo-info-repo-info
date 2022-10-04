## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:8a86cc4640c6eb7a79d0f2461db94ec9ad2fa6f65727e744ac8a12d7ef5737b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull golang@sha256:2b3956aca3b53e8bc9b66d1b9f913dcd322a11969d18f07b057afb95898cfb45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275549822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54aea239848272ffdcdf36296dcdcb56298305015ecd8327edeb58cd28d1b164`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Sep 2022 20:11:22 GMT
RUN Apply image 10.0.20348.1006
# Wed, 14 Sep 2022 12:59:22 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 12:59:23 GMT
ENV GOPATH=C:\go
# Wed, 14 Sep 2022 12:59:24 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 13:00:05 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Sep 2022 13:00:05 GMT
USER ContainerUser
# Tue, 04 Oct 2022 19:49:12 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 04 Oct 2022 19:52:03 GMT
COPY dir:1fc645e1b9a8ffb5757805e06eefa6c9c9b0f649b5403eeab554ede8594c418b in C:\Program Files\Go 
# Tue, 04 Oct 2022 19:52:59 GMT
RUN go version
# Tue, 04 Oct 2022 19:53:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:09629875cd6ee57fa551626fa2963d8b54718ba9acbf28e7cb5d684a9cb754d7`  
		Size: 118.1 MB (118131331 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66db2526be0f06c7bd6ba20bdc126ca2d5645acfeb41b5784e4664de37e72b49`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218b9cf76f654e06a3b6ef23073f7aa93beb2d7a009f84ece64ec3e3d1e7c5e2`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb708701bd5e2013191955685f70bb81113076e9a185d3a60689a9da8f296a63`  
		Last Modified: Wed, 14 Sep 2022 13:25:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a0722a534d7c153c052d9de736838075e3b4058d1d45fe5698776b85014a61`  
		Last Modified: Wed, 14 Sep 2022 13:25:26 GMT  
		Size: 85.4 KB (85374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7486bac86e8639da1434b9a65d14589fc776aa03daf816dcb7eeae093674535c`  
		Last Modified: Wed, 14 Sep 2022 13:25:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4915aa3ef9a1aa0ebfa55064a12ac5593080cdb53a163f65102df8cd96dd7cd`  
		Last Modified: Tue, 04 Oct 2022 20:14:39 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab788fca2eff28ef2fb0908b0883fcb7727cb64dfed3e0fb4fdc73891f7a8150`  
		Last Modified: Tue, 04 Oct 2022 20:15:15 GMT  
		Size: 157.3 MB (157276578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d44de55c8762bbddffe7acda6fc0d318a63985b335cdf0e79b9d177004f884`  
		Last Modified: Tue, 04 Oct 2022 20:14:39 GMT  
		Size: 49.5 KB (49529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9e0862bfc21f04243f240097831973ca7b6eb5088220486321f491e5b842a`  
		Last Modified: Tue, 04 Oct 2022 20:14:39 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
