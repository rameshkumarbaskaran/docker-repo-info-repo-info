## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:e86b239da62cf565d827cdb3d90d01e4cbdd1544257b648830ea1d42f76fdbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull golang@sha256:94027c54af3ef36f40eab85e9e99486f59a3f835461717b9eb4be489f84585a2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228762781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dce45ebe87edd469151423e849f46bc5edfac26b121e45573d94c3cf69917e7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jun 2023 12:38:25 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 18:50:26 GMT
SHELL [cmd /S /C]
# Wed, 14 Jun 2023 18:50:26 GMT
ENV GOPATH=C:\go
# Wed, 14 Jun 2023 18:50:27 GMT
USER ContainerAdministrator
# Wed, 14 Jun 2023 18:50:39 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Jun 2023 18:50:40 GMT
USER ContainerUser
# Wed, 14 Jun 2023 18:50:41 GMT
ENV GOLANG_VERSION=1.20.5
# Wed, 14 Jun 2023 18:52:40 GMT
COPY dir:2b56775b246889ea39ed6a295f7604dfecd0a015e0fc1352d091198ccc0b1678 in C:\Program Files\Go 
# Wed, 14 Jun 2023 18:53:02 GMT
RUN go version
# Wed, 14 Jun 2023 18:53:03 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:f94f5e4cef3f52c830328b87b7298c638fa9ef22a0babf737eda2a2dd6d024c4`  
		Last Modified: Tue, 13 Jun 2023 20:05:48 GMT  
		Size: 120.0 MB (120028549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf26306b7c3ea55d7d8bb15ad1c70de776773883ccc3ce02d9cfac7a8177ccf8`  
		Last Modified: Wed, 14 Jun 2023 19:09:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e89ef6c468c60a6c21ff5ec72c6cf2b0bea9e24bc1e7c990293fbc7279e323b`  
		Last Modified: Wed, 14 Jun 2023 19:09:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da192db941d3aa6195cfaf205ebf22038804e7025fafc3eaf86c798b276b7bf`  
		Last Modified: Wed, 14 Jun 2023 19:09:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948d32b6ff27bbde81b0fd07f89e23c955bef46612ae29fefa4b4797a5866968`  
		Last Modified: Wed, 14 Jun 2023 19:09:48 GMT  
		Size: 77.6 KB (77573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535e233f2d7e6eb5ee95b1c0c1c31d978b47787c939dac2c46fbb23647e6ae68`  
		Last Modified: Wed, 14 Jun 2023 19:09:46 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4372a329a44183bd64f9e1088a2ff51548585d8daf27930b3345cc64990d250`  
		Last Modified: Wed, 14 Jun 2023 19:09:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a25abec28e9aeb1d5cbdf2012d084d107c9531765d668c0e3cc1a507d3237c`  
		Last Modified: Wed, 14 Jun 2023 19:10:09 GMT  
		Size: 108.6 MB (108596816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f64d52a29004475aef44d5445391b55f281ae5d4c80fb4edb7e6712d8fd398`  
		Last Modified: Wed, 14 Jun 2023 19:09:46 GMT  
		Size: 53.5 KB (53460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb6c5ef06f1a8bd79867c9cb67315db60bf14a23ab94f8cb3c3759212c5ac13`  
		Last Modified: Wed, 14 Jun 2023 19:09:46 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
