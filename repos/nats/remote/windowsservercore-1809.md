## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:4331838044198073df8afe0ad453fd1eb97f51ec7bde9025303fbbb1189e155d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats@sha256:ae5ea527d83182c720c7d1ed179661da4d518fcd64cb5f5dee86948254dcb62c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2721254090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88151b674d5d60f9b53098f2888cdb2b6934a2f3b54d108de2cdb34972019f07`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Fri, 22 Apr 2022 16:20:42 GMT
ENV NATS_SERVER=2.8.1
# Fri, 22 Apr 2022 16:20:43 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.1/nats-server-v2.8.1-windows-amd64.zip
# Fri, 22 Apr 2022 16:20:44 GMT
ENV NATS_SERVER_SHASUM=a8c4535897e7973cce5005f7fa71ef0f681a7faf014f8875b5a35e865261ff1f
# Fri, 22 Apr 2022 16:21:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 22 Apr 2022 16:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 22 Apr 2022 16:23:13 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Fri, 22 Apr 2022 16:23:14 GMT
EXPOSE 4222 6222 8222
# Fri, 22 Apr 2022 16:23:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 22 Apr 2022 16:23:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8987265b365755a0b758f78710e444da1b49314f15f64aa591dd344430d3fb`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5265b75522ed436be37427e2b945e79901d0288c294b04bea492dbd522b2cfe`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0142ce0f758e44db725dfe50c5e3b301364181c2e9e8505003ea5e5faeb50ab`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1718491c665ff5c4180c99f48ca54ffd756d9e28ce78d0177dc4f5d8974185`  
		Last Modified: Fri, 22 Apr 2022 16:23:59 GMT  
		Size: 359.7 KB (359679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331728196114862c2dc2e870fbee9fb2f0e1f51778d0c228ed319a2a43739c7`  
		Last Modified: Fri, 22 Apr 2022 16:24:02 GMT  
		Size: 5.0 MB (4960879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b500a22154605ab8b08473544c72dc700dc6f83895c4efc82544f82f544bbf`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728c706f26744001339dc27c514f27f211b217c21f5fe860bd3e565365cef023`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf4bee55391723a25240f8a0bd0dfe04b2c3fa9dca71af7f792425ff3aec92`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f4247067242fb22fccdaa011c8629357ed677cf22255e88d521e5781f0290`  
		Last Modified: Fri, 22 Apr 2022 16:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
