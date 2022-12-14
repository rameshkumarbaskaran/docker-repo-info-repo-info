## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:bd5262b0964a38e7e28de29632b03d507ba57fc832bb3171567478da841d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:11e1ab562299ebbb64ab18c5afd891fa67655420780a109677a922340d8777d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786352699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6dc041a550a2790319a7bb1f8b2b6bc818495c7300afc3226fc2da4d42219a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 02:37:16 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Dec 2022 02:37:17 GMT
ENV NATS_SERVER=2.9.9
# Wed, 14 Dec 2022 02:37:18 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.9/nats-server-v2.9.9-windows-amd64.zip
# Wed, 14 Dec 2022 02:37:19 GMT
ENV NATS_SERVER_SHASUM=a3456ed1a8f02d9d8ced35a1adbe1f6451af0c303f87ff74c15879dfc8cabd30
# Wed, 14 Dec 2022 02:38:59 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Dec 2022 02:41:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Dec 2022 02:41:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Dec 2022 02:41:20 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Dec 2022 02:41:21 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Dec 2022 02:41:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b4fa0f968fba4be86c61da602c6d1d95bea2a5b257fa97e5cb498f7ddc7fe`  
		Last Modified: Wed, 14 Dec 2022 02:42:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1296500fbd02b72d68a4f8d4c78bb6c35ddaaa2c332cfe9254604281a913a00`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50931b0d887f06faade1d2051e8cceac2255778e1b4b9653fc75474db54b489d`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d625cf2ad988d5ac80b24112ef78da7fe7bddd4b5d188962fcb3ab90f04b57e`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665d13d7cbc9a4ce6c8e5bc9120d5e3343377d7211f1e4d12480ddda591f522`  
		Last Modified: Wed, 14 Dec 2022 02:42:15 GMT  
		Size: 342.0 KB (342028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75307c50ea67f0603708dfc03956f1d610f261a5fa0f54d064b1690b0f866274`  
		Last Modified: Wed, 14 Dec 2022 02:42:14 GMT  
		Size: 5.3 MB (5300085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1799e7de223a25ae30a351e317b449f128c31f00e818c0df0b02a4be360e4cf3`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeddb4c41b8d5fdc840c446ef490340728041b9202f2db80dce668c9d8d8ca5`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb917ab1b2406dc49a3fcc8fe92a27023ef822724a7c3056fa6f14ea3eca9d09`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2920025a2b586dcc5fa9b1580994f3bedbdbc128a7ab0a5c9bba8ca690025e0e`  
		Last Modified: Wed, 14 Dec 2022 02:42:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
