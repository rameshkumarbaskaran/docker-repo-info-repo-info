## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:405ac6ee7d9e28dcc8330289aecc521db9a306ac070709fb721196bc02385803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull golang@sha256:e0c25cfad62d3c1de20ae8afc22a7e15b32f971ef0ae36d18eed849892e69f0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241881452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22713df7cded7793796b7f6df1395f6a476fe4436a6c2151edb9011bc0d142ef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 01:23:41 GMT
SHELL [cmd /S /C]
# Wed, 14 Jul 2021 04:39:11 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Jul 2021 04:39:14 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 04:39:34 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 14 Jul 2021 04:39:36 GMT
USER ContainerUser
# Thu, 05 Aug 2021 22:21:42 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 22:23:47 GMT
COPY dir:b5619cdbe374ab44f03453dea22f6ca80295560446197b4d9ffef2b5333db67b in C:\go 
# Thu, 05 Aug 2021 22:24:33 GMT
RUN go version
# Thu, 05 Aug 2021 22:24:35 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5307d56ac81f33a647e0ed6f4e0f70a39b207469fe0a28ab1b9f9379669e02b4`  
		Last Modified: Wed, 14 Jul 2021 02:04:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d72046f3f0748f7f1cfa8143e2940c7ce6648a4092f19478ab5be051da4322`  
		Last Modified: Wed, 14 Jul 2021 05:05:15 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c01484fb96cabf37eb40789a70cb7ded860d276f0f3d67cf73c460068c4da8`  
		Last Modified: Wed, 14 Jul 2021 05:05:15 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861d147727a049b4e876c27462f827024b9faad381fdcedb6566a9dabe2686b9`  
		Last Modified: Wed, 14 Jul 2021 05:05:15 GMT  
		Size: 65.6 KB (65616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770b7cc5eaa7b215b7bf7c49e2695c7e943eaa335695c19604604130a78196e1`  
		Last Modified: Wed, 14 Jul 2021 05:05:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d79025baf8cafa2aa136c89341d00ff26257dd9febe605a1daf233e67356ed`  
		Last Modified: Thu, 05 Aug 2021 22:37:31 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a1d872e5b45299285b6b0730d774f3bceda9dd057369eda60a1d9daed3e790`  
		Last Modified: Thu, 05 Aug 2021 22:38:01 GMT  
		Size: 139.0 MB (139017445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa6a4c65f53a8e9afafcab2c6eca6ea9e1fb50247d7f9c045bc26c12d8929ed`  
		Last Modified: Thu, 05 Aug 2021 22:37:31 GMT  
		Size: 65.6 KB (65642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af605bf19342c1e2e18ea0e49ce3428eccb9f74d1bf8232051681fcb325a340`  
		Last Modified: Thu, 05 Aug 2021 22:37:30 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
