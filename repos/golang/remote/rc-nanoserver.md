## `golang:rc-nanoserver`

```console
$ docker pull golang@sha256:d8a7a8ee3000c8b31297b9fcf7a06e9c2360dada7a2a971ebee573a2690eec0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `golang:rc-nanoserver` - windows version 10.0.17763.1282; amd64

```console
$ docker pull golang@sha256:25f8dc9997ab2eaccca405585f404745983db020681c517d87db6d6d1baaf3f1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235003350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0802c834f571cc9350420b9b7fcb8479b8c2a0320e92970e30f9082f336736e8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jun 2020 11:12:32 GMT
RUN Apply image 1809-amd64
# Wed, 10 Jun 2020 12:24:27 GMT
SHELL [cmd /S /C]
# Wed, 10 Jun 2020 12:24:27 GMT
ENV GOPATH=C:\gopath
# Wed, 10 Jun 2020 12:24:28 GMT
USER ContainerAdministrator
# Wed, 10 Jun 2020 12:24:44 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 10 Jun 2020 12:24:44 GMT
USER ContainerUser
# Thu, 11 Jun 2020 22:23:34 GMT
ENV GOLANG_VERSION=1.15beta1
# Thu, 11 Jun 2020 22:26:01 GMT
COPY dir:bca8b35311fabc2b83a3f43030a6dd3dbb9ca7fba444cf0fac8f73bd11980917 in C:\go 
# Thu, 11 Jun 2020 22:26:20 GMT
RUN go version
# Thu, 11 Jun 2020 22:26:21 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:c7d6d47ff7dfb2aa4d4e819641b93ec971e8541978dff0ffc24c193babeb8c07`  
		Size: 101.0 MB (101043386 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ccc2ab174115d7c1f51c57b207bdadd2668d5de4d6f81a62f1dc59b31df7f15b`  
		Last Modified: Wed, 10 Jun 2020 12:39:48 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583d464994f7875d7c8cb87eed53cca0febfb7858a842e2c50062e033fac949`  
		Last Modified: Wed, 10 Jun 2020 12:39:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b915241332cbe27b35f3eb233a8c2d632493880ddc7a5ab772d4fc00a32cdf`  
		Last Modified: Wed, 10 Jun 2020 12:39:47 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1088d70f6361299e2ed3757ecf7c4b4194b7086ba6bb0657ec5846d430669097`  
		Last Modified: Wed, 10 Jun 2020 12:39:47 GMT  
		Size: 67.4 KB (67379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c056ad564aad66a81fc80e987921a29f646707699d3ad7cb8e074426e0015d24`  
		Last Modified: Wed, 10 Jun 2020 12:39:44 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c5d4522a10e7984a982304400e1f6d2c32fb3df328f8145176b3dcf36ab19`  
		Last Modified: Thu, 11 Jun 2020 22:29:26 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bb0f98d4f2198593b342d77a2c64441ca9045169db635d8aceedd71bca17ff`  
		Last Modified: Thu, 11 Jun 2020 22:29:53 GMT  
		Size: 133.8 MB (133809183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b598ac81b54d03d56b05c3922997839ff2b437f93210f56d97cafb0f2bbf41`  
		Last Modified: Thu, 11 Jun 2020 22:29:26 GMT  
		Size: 77.9 KB (77888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213a3d429395323600fd9672a81d5081b0adc080db685303a7cba995ea7c8889`  
		Last Modified: Thu, 11 Jun 2020 22:29:26 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
