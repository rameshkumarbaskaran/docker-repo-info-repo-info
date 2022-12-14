## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:73751e49460ffb149194b5a6dbaac6c89cbe930980c090ec3261cb742eafe60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull golang@sha256:fb67296f145dc4d5b4eb38b613464ea24c36854cca22a15b2a0af6cac0308e4d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264126889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7b10267693378cd6ac05480b93c713ca697fab274d4094bcfb543f2f1aadb1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Wed, 14 Dec 2022 00:31:01 GMT
SHELL [cmd /S /C]
# Wed, 14 Dec 2022 00:31:01 GMT
ENV GOPATH=C:\go
# Wed, 14 Dec 2022 00:31:02 GMT
USER ContainerAdministrator
# Wed, 14 Dec 2022 00:31:44 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 Dec 2022 00:31:45 GMT
USER ContainerUser
# Wed, 14 Dec 2022 00:49:34 GMT
ENV GOLANG_VERSION=1.19.4
# Wed, 14 Dec 2022 00:52:34 GMT
COPY dir:2cd450fd2156a5a74a4e4b1dc7a490c2568a41af5e46c584b0660f27917680aa in C:\Program Files\Go 
# Wed, 14 Dec 2022 00:53:22 GMT
RUN go version
# Wed, 14 Dec 2022 00:53:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb1e4df1760e3de08ff30de6fd3f3acf348399853dab1aa1632ed4080cd102`  
		Last Modified: Wed, 14 Dec 2022 01:14:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6778b951d29f9735989650092ed207db9277298447f0162c8fe059a79fd71d`  
		Last Modified: Wed, 14 Dec 2022 01:14:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43efe6d3eed8dae1f414ff88e3af891aec01f30a91dd6f08b331c5f276ea670a`  
		Last Modified: Wed, 14 Dec 2022 01:14:11 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f35dd05107084e8e2076914c92cca0fb4a6c3413651c7c6ef8187d37e9ba83`  
		Last Modified: Wed, 14 Dec 2022 01:14:11 GMT  
		Size: 62.3 KB (62253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83fe57fefeebabec45f4602b2bd5642b9f242f21a3bf51bdd8ba353b3128ae9`  
		Last Modified: Wed, 14 Dec 2022 01:14:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53716a2bb872611b3eb3a7a8a004f2d708aa95953b18318f9ed0776f45204cb9`  
		Last Modified: Wed, 14 Dec 2022 01:18:13 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef0a52915c32329fa6df300573fb731b885fdece4c20af64859ad08f2cb913`  
		Last Modified: Wed, 14 Dec 2022 01:19:05 GMT  
		Size: 157.3 MB (157323894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a343dcda48393cd79fe2bbd21e41854a4619160234e83d8ce3412be8ba100f31`  
		Last Modified: Wed, 14 Dec 2022 01:18:14 GMT  
		Size: 62.6 KB (62572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2460f70e97b9417330280881e54756d80beb457869ee5097b7abcf7da350200c`  
		Last Modified: Wed, 14 Dec 2022 01:18:14 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
