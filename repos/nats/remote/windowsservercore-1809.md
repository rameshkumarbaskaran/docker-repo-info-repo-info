## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:9270664ec8e3e24593346ab908a3217b6fe4514ff6017cf5dabe962ef335aa4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull nats@sha256:071bb1c3dd6db9f0061bda67de7d79a0cce57e8d0e8da73e85a7aa754ce76335
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2786387163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc338a505657aa4c86822f8b426eaa4187c7cee6461a6ff44f02bb7bb65d912`
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
# Tue, 20 Dec 2022 22:16:10 GMT
ENV NATS_SERVER=2.9.10
# Tue, 20 Dec 2022 22:16:11 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.10/nats-server-v2.9.10-windows-amd64.zip
# Tue, 20 Dec 2022 22:16:12 GMT
ENV NATS_SERVER_SHASUM=bd6d8d6c538da79e91d5c080d8c29d893bd46809698157d4a597930d4532e2da
# Tue, 20 Dec 2022 22:17:47 GMT
RUN Set-PSDebug -Trace 2
# Tue, 20 Dec 2022 22:19:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 20 Dec 2022 22:19:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Tue, 20 Dec 2022 22:19:57 GMT
EXPOSE 4222 6222 8222
# Tue, 20 Dec 2022 22:19:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 20 Dec 2022 22:19:59 GMT
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
	-	`sha256:690d95bd401433248324d5651b02491f88493855bbca3ab04f0f019662f343a1`  
		Last Modified: Tue, 20 Dec 2022 22:20:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43d1b51ede19ba263c609bdd044852910ec18bffbb4bfd2c4ceb7d172f98f86`  
		Last Modified: Tue, 20 Dec 2022 22:20:44 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84d3d0b2ec5af28532d1d914a2291a32302c2b624028f5ad624323865b3f13d`  
		Last Modified: Tue, 20 Dec 2022 22:20:44 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc43ff939ad6b0c8fddf784e623eaf2afcdfc0840d288ecfa7ae6441c144c1`  
		Last Modified: Tue, 20 Dec 2022 22:20:45 GMT  
		Size: 358.2 KB (358161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8b1f1b1238167695b28122989d27f52f599d9f7cfec8089d47725e11f3d472`  
		Last Modified: Tue, 20 Dec 2022 22:20:44 GMT  
		Size: 5.3 MB (5318419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39db20eaab99eb69fae5857a6d14e87e821ded6314cbc889c6f280f3d52d9f39`  
		Last Modified: Tue, 20 Dec 2022 22:20:42 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3991a405da35b750a5e4f85f67c25dbff8e0527cb54f2a8a6a2798449d7d3a`  
		Last Modified: Tue, 20 Dec 2022 22:20:42 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af362ca437bc15fd31c7e01a6088ed4ef8c251f3fc33d4f69c4dc0fbf6f1315`  
		Last Modified: Tue, 20 Dec 2022 22:20:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4920caa3fc8006708c0da2205604b65bb4530006d2db26c917dac02011e2007e`  
		Last Modified: Tue, 20 Dec 2022 22:20:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
