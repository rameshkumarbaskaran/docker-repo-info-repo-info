## `golang:nanoserver`

```console
$ docker pull golang@sha256:d5046d55a6f7f08a96ff953d870668540384a8debf5cd62b57039c5bbde4d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `golang:nanoserver` - windows version 10.0.20348.1607; amd64

```console
$ docker pull golang@sha256:7bcc78180a60039a85086e2027595640655c693ab1f8cbcdb99c038c9063dea0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230910933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a7dd0d99ae714f45d8d2c64d35d3c5b8353e2f7b723aef0a34afc7471e9929`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 02:15:36 GMT
SHELL [cmd /S /C]
# Thu, 16 Mar 2023 02:15:37 GMT
ENV GOPATH=C:\go
# Thu, 16 Mar 2023 02:15:38 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 02:16:34 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Mar 2023 02:16:34 GMT
USER ContainerUser
# Thu, 16 Mar 2023 02:16:35 GMT
ENV GOLANG_VERSION=1.20.2
# Thu, 16 Mar 2023 02:19:27 GMT
COPY dir:ba7807802ed24328b363fd1db731e4c016063d2f2ee48aec17d5bb33bef460c8 in C:\Program Files\Go 
# Thu, 16 Mar 2023 02:20:20 GMT
RUN go version
# Thu, 16 Mar 2023 02:20:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa68b8cf98c4e81d0a56e6860ff5347ca921b2991f0fca1a397b892e862ec97`  
		Last Modified: Thu, 16 Mar 2023 02:47:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3e1a313e9eb78dd2a397e1e2b0bfaa4fd5c5749c45bb807229930a78aaf57`  
		Last Modified: Thu, 16 Mar 2023 02:47:12 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dea9517972a6152c9e785c9f47254b6ac12ccf7993a693fdbb32b472da76ef`  
		Last Modified: Thu, 16 Mar 2023 02:47:12 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1704c6e39a6b62d6fb49c05bbc39a72f93a7ef59ad440624dc9a859e20cede52`  
		Last Modified: Thu, 16 Mar 2023 02:47:12 GMT  
		Size: 84.7 KB (84651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7a5254bc275f6aac700968b63b65cc4b63edbc2a7a542cbf371e9c0d217bd7`  
		Last Modified: Thu, 16 Mar 2023 02:47:10 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ae89c8ce67c49a798bdabddd9d2428fb9d9f4ccc2951460b1de497b05ff56`  
		Last Modified: Thu, 16 Mar 2023 02:47:10 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8126f2efa0e62c4e53900ed85f6cdd1d59ca5df5110f157d62ea510741d0d1a9`  
		Last Modified: Thu, 16 Mar 2023 02:47:47 GMT  
		Size: 108.6 MB (108593954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa1820fbee3631d4677b9f2f467bf1e5de834ee25798981d5508aa3bbd5b60`  
		Last Modified: Thu, 16 Mar 2023 02:47:10 GMT  
		Size: 53.4 KB (53438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bd1c4637e84d9853108d8c9b63ce0786f30aa5b77abd13722e0a4e3b034f45`  
		Last Modified: Thu, 16 Mar 2023 02:47:10 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull golang@sha256:8b970df2201954057d0a8bf2b4abfc44f7a1759d86a41e3cceefb51d8b53cab1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215426617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1ce1b044b891526b23a208269e4eb042763e322e9470cd06fbf3111b0ddba2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 02:20:46 GMT
SHELL [cmd /S /C]
# Thu, 16 Mar 2023 02:20:47 GMT
ENV GOPATH=C:\go
# Thu, 16 Mar 2023 02:20:48 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 02:21:31 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Mar 2023 02:21:32 GMT
USER ContainerUser
# Thu, 16 Mar 2023 02:21:33 GMT
ENV GOLANG_VERSION=1.20.2
# Thu, 16 Mar 2023 02:24:25 GMT
COPY dir:ba7807802ed24328b363fd1db731e4c016063d2f2ee48aec17d5bb33bef460c8 in C:\Program Files\Go 
# Thu, 16 Mar 2023 02:25:11 GMT
RUN go version
# Thu, 16 Mar 2023 02:25:12 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5cc414fce78380e134ec2315d713a8a9040bff5d1298887a2a68029cfc0922`  
		Last Modified: Thu, 16 Mar 2023 02:48:05 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77358ace842a4af47a00594821c3cc0c53ef0f00f3695692c2f19b6f9fd023bd`  
		Last Modified: Thu, 16 Mar 2023 02:48:05 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633faaff1da959771878c043ba820b0e38b62cf26268b1e87acd834496c3de90`  
		Last Modified: Thu, 16 Mar 2023 02:48:05 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d52a594f074a3f99c586be0721850cc97d40228451e2e289e99145906f8566`  
		Last Modified: Thu, 16 Mar 2023 02:48:05 GMT  
		Size: 69.5 KB (69550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027c3baf1644b032096e95101de22f26e2b8e43c242cac344351be66be56757a`  
		Last Modified: Thu, 16 Mar 2023 02:48:03 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859b55c57b82108f0b811e9f1a80e79ae9baaf51a1741221f35ea50ba3abae0`  
		Last Modified: Thu, 16 Mar 2023 02:48:03 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c68595098490b87ea37f4745f224a0e7182fa47de6ca41e2ca61f734f80b470`  
		Last Modified: Thu, 16 Mar 2023 02:48:40 GMT  
		Size: 108.6 MB (108593528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af56052abe0107b0654dae0d66f1a079991258eea0f90986193593fbf4468662`  
		Last Modified: Thu, 16 Mar 2023 02:48:03 GMT  
		Size: 72.2 KB (72161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca54eb51fbde252597ff26cd12d22f42560d647cd9bd99d7454577e132a5314`  
		Last Modified: Thu, 16 Mar 2023 02:48:03 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
