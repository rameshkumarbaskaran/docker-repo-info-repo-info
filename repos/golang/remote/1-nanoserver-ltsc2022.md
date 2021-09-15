## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:efaa9f79edd690098fdbb29469385d3bb3eae396bf801aa2616733664fe3dce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.230; amd64

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
