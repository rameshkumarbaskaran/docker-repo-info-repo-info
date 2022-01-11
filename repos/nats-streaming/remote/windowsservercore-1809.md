## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:2cc23cf34a30d07bbb4db6499522e0a48742fae86ad3997f52b88dbf88e2ecd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull nats-streaming@sha256:f49548114fa9a741d9cebe2035ec34ffcf56ada33f797007e6e7ab6cf1386ad8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2719714545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098db14004c6459b5e47445fe968cd67304f5b3a1d9212f7384f8db19032417c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 19:57:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Jan 2022 19:57:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 11 Jan 2022 19:57:21 GMT
ENV NATS_STREAMING_SERVER=0.23.2
# Tue, 11 Jan 2022 19:57:22 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.23.2/nats-streaming-server-v0.23.2-windows-amd64.zip
# Tue, 11 Jan 2022 19:57:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b28dc8e1565d6fece68781515f759b0ed870831cdf2f7925cff7cf9acb44e7ec
# Tue, 11 Jan 2022 21:21:27 GMT
RUN Set-PSDebug -Trace 2
# Tue, 11 Jan 2022 21:23:12 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Tue, 11 Jan 2022 21:23:13 GMT
EXPOSE 4222 8222
# Tue, 11 Jan 2022 21:23:14 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Tue, 11 Jan 2022 21:23:15 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6b0d3bf43971fbd8415d8d92eb7059b4aed9092fc3c7878b893d688b3b6b478c`  
		Last Modified: Tue, 11 Jan 2022 21:19:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547439af6c2636b60dd7d8627268efd629795e6a4f8bcd3c3f7ebba364c6b79`  
		Last Modified: Tue, 11 Jan 2022 21:19:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a31a0b6b24d08070a42a0f8a686e7015147b029b878da7d569c2e61aa19367`  
		Last Modified: Tue, 11 Jan 2022 21:27:03 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f1d6d034a40c70932eb661047bb862f7e298402147f90d2f3766cc8e3a1ba`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a441c2c2db73b8e54172a01184b9dafa87386bf687aa36534d11f8646c65abcb`  
		Last Modified: Tue, 11 Jan 2022 21:27:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf43a8d096610b235d9fd922d616200d5260244001b216860fe74206f4ca10d`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 357.7 KB (357691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859fc29ccd05e15b9243fc0ac7b9e46bb2def51d869405938d746f75d01e9ce5`  
		Last Modified: Tue, 11 Jan 2022 21:27:09 GMT  
		Size: 7.8 MB (7761502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201caa128bd977747bcc262cef888242ef4ebef65928888b9f7c0fab17aec26`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0e7e2354a36b32060c592f44d8b321a26705c27030ed6a11c2d2a9f58b2a2`  
		Last Modified: Tue, 11 Jan 2022 21:27:01 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3619641381a86d3c401ca5a05a646db2c3fbdb40fe9dd75a80888f523a27d00`  
		Last Modified: Tue, 11 Jan 2022 21:27:00 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
