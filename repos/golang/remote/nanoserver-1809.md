## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:faef9fa5333be34ff689f74d987666551ab92379afefcf25da0acc0f4fa10730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull golang@sha256:e0a06582a9e533b25781c0076d5b98a2bd0a764c841b284258597afd910674cb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260768813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0dad627a4b7740943760869941fdce2a61ec2712aaf9b135fda921cc2eeaf9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 09 Sep 2022 22:22:51 GMT
RUN Apply image 10.0.17763.3406
# Wed, 14 Sep 2022 13:03:35 GMT
SHELL [cmd /S /C]
# Wed, 14 Sep 2022 13:03:36 GMT
ENV GOPATH=C:\go
# Wed, 14 Sep 2022 13:03:37 GMT
USER ContainerAdministrator
# Wed, 14 Sep 2022 13:04:01 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Sep 2022 13:04:01 GMT
USER ContainerUser
# Tue, 04 Oct 2022 19:53:11 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 04 Oct 2022 19:55:56 GMT
COPY dir:1fc645e1b9a8ffb5757805e06eefa6c9c9b0f649b5403eeab554ede8594c418b in C:\Program Files\Go 
# Tue, 04 Oct 2022 19:56:42 GMT
RUN go version
# Tue, 04 Oct 2022 19:56:43 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:bcd4ab6c304faa0a7f4e183705a7f6e4545b728788221d17886d2a507ea0a06d`  
		Size: 103.3 MB (103334221 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0668477bacdfc2e7df1cd4268b246175ed9b30cf07ccb4bcfcb258d8bee830e`  
		Last Modified: Wed, 14 Sep 2022 13:26:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd835cc99524be3bba77b73a838666949cf7d47639a399e21f6d14634a36d6b0`  
		Last Modified: Wed, 14 Sep 2022 13:26:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676957d5345611461c5bb939bd80adc80391d96397aa8a4511fcb998a9c57870`  
		Last Modified: Wed, 14 Sep 2022 13:26:18 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4570eed23060516293c36e26c87bcda7c57eaa2e2677941747fc0d245eb30e3`  
		Last Modified: Wed, 14 Sep 2022 13:26:18 GMT  
		Size: 70.5 KB (70482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528822ef8700498a1b6039b0b3fe96dbe512d72f9f888362aa2b2bcefa7e0fd5`  
		Last Modified: Wed, 14 Sep 2022 13:26:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521ff275738a37de4ddf8ba84b729478c1703dbcc006e850640baa9d4588940a`  
		Last Modified: Tue, 04 Oct 2022 20:15:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5bff486fa6c508f3a0c3a98ee8ac913a00bc6ad8035bbb387def89a9a79029`  
		Last Modified: Tue, 04 Oct 2022 20:16:04 GMT  
		Size: 157.3 MB (157283364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91af77cfbd5c232a962b23334971e2539004d5bfc84f47eed99e3591e08a414`  
		Last Modified: Tue, 04 Oct 2022 20:15:29 GMT  
		Size: 73.6 KB (73598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d23064cfcbd1d314633c997d7a0900972eb945aab89e086d01747a5ea780683`  
		Last Modified: Tue, 04 Oct 2022 20:15:29 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
