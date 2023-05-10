## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:a5cf526d6d89af3bf3163ffe71dc362d0223ec5183c2d2b7be8c599bbe842805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull golang@sha256:5f1be952dd0a5f9aba85af7613b132d3f5ffc8a8ea6009cacd9b512c5b7dd778
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228753687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b3ab470130e8dc7bb4922d6c52a8241e37f2e6852bc635d7f35955fd4f5ef3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 May 2023 12:52:54 GMT
RUN Apply image 10.0.20348.1726
# Wed, 10 May 2023 01:28:38 GMT
SHELL [cmd /S /C]
# Wed, 10 May 2023 01:28:38 GMT
ENV GOPATH=C:\go
# Wed, 10 May 2023 01:28:39 GMT
USER ContainerAdministrator
# Wed, 10 May 2023 01:28:49 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 May 2023 01:28:50 GMT
USER ContainerUser
# Wed, 10 May 2023 01:28:50 GMT
ENV GOLANG_VERSION=1.20.4
# Wed, 10 May 2023 01:30:34 GMT
COPY dir:522e0da3d6c3a6cfa6b16530131c440cc60a26151f29e0cb9d21de10dd15cbac in C:\Program Files\Go 
# Wed, 10 May 2023 01:30:50 GMT
RUN go version
# Wed, 10 May 2023 01:30:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7d382efe6974b94c05000b6a95c1fd28e1b8bb3e81cc4592b2aa1cc46b90192c`  
		Last Modified: Wed, 10 May 2023 01:48:23 GMT  
		Size: 120.0 MB (120001338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d879624716c16bfc9a9e8c219f4a25a8d311021e41efa6a951e95c4bb6fc44`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f215b7eafe1075b520de20800f9aa12a7c78cb1f8dad18b8bc45996e459859b`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f0354085e18a9015d575f85124b34250c691ae6225a9025a301516eb3429f`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74d501c19f757ed7199b0b3edaa4106915f0698f2841746cdfc4a67cec53de6`  
		Last Modified: Wed, 10 May 2023 01:47:58 GMT  
		Size: 81.3 KB (81262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a6c22d4a69f55f1103a72c26b33766023a322f8d29d4f22a0114fdf5139dec`  
		Last Modified: Wed, 10 May 2023 01:47:56 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0286a8c0b42419c268cda89cbd8e661ddda489d44e1199cf38adfd986feaaac6`  
		Last Modified: Wed, 10 May 2023 01:47:56 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be183f1da617db4f2791bfdcd2927dd8bb11450af497d39a19e705c5b5efe96b`  
		Last Modified: Wed, 10 May 2023 01:48:19 GMT  
		Size: 108.6 MB (108610294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882d52f031cdf3fecc79ccb50e086acdd59822255e4393fd7a788b3eb5d9691c`  
		Last Modified: Wed, 10 May 2023 01:47:56 GMT  
		Size: 53.7 KB (53656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f70ae266f790ad3b417361ebfbbeaa208870dfa065bf4360f05e9ecbcb290`  
		Last Modified: Wed, 10 May 2023 01:47:56 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
