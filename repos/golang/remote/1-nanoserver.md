## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:a21f9d642a17b5330fecee9aa2d84620689673fa8ea8f83151c6348947abb6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.230; amd64
	-	windows version 10.0.17763.2183; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.230; amd64

```console
$ docker pull golang@sha256:77cc9bde493ee76b4e8da9ff29b7738f7d3feff29040d9fcda398c892c271ad2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262048791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690ccc50ae31ab2942aa8cc4331a7c884d77af0cafdc109f22745caed5ac8cf8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Sep 2021 06:44:45 GMT
RUN Apply image ltsc2022-amd64
# Wed, 15 Sep 2021 12:35:24 GMT
SHELL [cmd /S /C]
# Wed, 15 Sep 2021 12:35:25 GMT
ENV GOPATH=C:\go
# Wed, 15 Sep 2021 12:35:26 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 12:35:41 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Sep 2021 12:35:42 GMT
USER ContainerUser
# Wed, 15 Sep 2021 12:35:43 GMT
ENV GOLANG_VERSION=1.17.1
# Wed, 15 Sep 2021 12:37:48 GMT
COPY dir:96b2db49684f355600a0eba9c6bf46049724e901f0e48267d1df305ef566f9f1 in C:\Program Files\Go 
# Wed, 15 Sep 2021 12:38:29 GMT
RUN go version
# Wed, 15 Sep 2021 12:38:30 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:521b4ff1716af921a5cfbf2119d97dc479e9b1eb487d17d0f576ff856ab68e61`  
		Size: 116.9 MB (116897071 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7c64053617a596b2bbde39eb8f46e143b958761c013888304ba5c831cbdf8194`  
		Last Modified: Wed, 15 Sep 2021 13:02:20 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584fd00370fb04c15f318a76c38e3d8b28c593d60f10ff3d7a25aeccda8dd1f6`  
		Last Modified: Wed, 15 Sep 2021 13:02:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabd02ba6da164558e4f3d6b9fbcadea8bcfbd993ced8699091a7ca659aa1795`  
		Last Modified: Wed, 15 Sep 2021 13:02:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf15b650c040473e28ce4042255282c0b4960a2a82bee6a0289ad401c1fd54c`  
		Last Modified: Wed, 15 Sep 2021 13:02:20 GMT  
		Size: 76.9 KB (76865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc59d14e3a5feed1ac03340aa061261bf4aa31fac8916b67120b775b19a87eb`  
		Last Modified: Wed, 15 Sep 2021 13:02:17 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fa5e7cf72a2ce8db94ed423879184ae23798487b7c9c3d7930cbb9b128f679`  
		Last Modified: Wed, 15 Sep 2021 13:02:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aae1545c0bd853e60a2364f075bfc2f1ebffdf9c211ec0b2747f2e2f9b378e9`  
		Last Modified: Wed, 15 Sep 2021 13:04:49 GMT  
		Size: 145.0 MB (145019242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04745dffb1e794d38d5cc3cfb1694ecbb1208ba481d9bf4e02e629eb40a5ac7`  
		Last Modified: Wed, 15 Sep 2021 13:02:17 GMT  
		Size: 48.6 KB (48617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2a9f32ac53700a12d5fe37d77815a3de8efba1c685c9a82f2e76a60bdd12ee`  
		Last Modified: Wed, 15 Sep 2021 13:02:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull golang@sha256:02c3d3982acb986049f72d05f69697c17732a15428087a59d90a51d6c33c8a49
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247879757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0a9bf94eab084ba37e2c0f3dd4468f277de4a7599cedf20dc52f28dc605a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 12:38:36 GMT
SHELL [cmd /S /C]
# Wed, 15 Sep 2021 12:38:37 GMT
ENV GOPATH=C:\go
# Wed, 15 Sep 2021 12:38:37 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 12:38:47 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 Sep 2021 12:38:48 GMT
USER ContainerUser
# Wed, 15 Sep 2021 12:38:48 GMT
ENV GOLANG_VERSION=1.17.1
# Wed, 15 Sep 2021 12:40:45 GMT
COPY dir:96b2db49684f355600a0eba9c6bf46049724e901f0e48267d1df305ef566f9f1 in C:\Program Files\Go 
# Wed, 15 Sep 2021 12:41:26 GMT
RUN go version
# Wed, 15 Sep 2021 12:41:27 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2ca4d60596cfd2b5f14d3690345d5a3c729f5c92997c02dae42415488ac1008`  
		Last Modified: Wed, 15 Sep 2021 13:05:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440629e3e164571aacd603b2182b9c247d507467bdb083817c346bbbb6513973`  
		Last Modified: Wed, 15 Sep 2021 13:05:07 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7c8f44cbbaf6c8b375a2783723913bfbf53a33513d439811e785ae46e6f1e8`  
		Last Modified: Wed, 15 Sep 2021 13:05:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb48885a5ccaf9c8d8e69f3bb0fd77403366bd884a889408ded8ab83ba6172c`  
		Last Modified: Wed, 15 Sep 2021 13:05:07 GMT  
		Size: 68.1 KB (68085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c1d51e92ca574e622d8d830a48d878a457668e59fe5caebc43ff725d80b40c`  
		Last Modified: Wed, 15 Sep 2021 13:05:05 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9974579224822fe3c5731278665097046cfbf542f1eefc8432f9fa9fecbc66fd`  
		Last Modified: Wed, 15 Sep 2021 13:05:04 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4675b591c8369a8fb8996f5b8edf98c321db19628e28d73642da1450563be63`  
		Last Modified: Wed, 15 Sep 2021 13:07:47 GMT  
		Size: 145.0 MB (145015353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55786deb4b0c2fec4b29699c537249fcacb6c720f09ce7c0fd99dfcb487e2e86`  
		Last Modified: Wed, 15 Sep 2021 13:05:04 GMT  
		Size: 86.0 KB (86012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebf00f13a11af6f2a6080155b7de90a125d297e2c004d5def4648b5db511cc0`  
		Last Modified: Wed, 15 Sep 2021 13:05:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
