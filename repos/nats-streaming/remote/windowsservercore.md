## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:90f956a0b4d242f64dc27f084e4322ad40f669004f06d6660fde87222b4f25bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64
	-	windows version 10.0.14393.3808; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull nats-streaming@sha256:fd2b16284f5c09bc81615f52d55aa557e0c4faaf4ffbe623fa9c4a9f855094ca
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330067351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7796ffa578afe3152a7069c15ad9993baf8de4b7e748bbf2eb9013ecc443ef9a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 15:03:03 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Jul 2020 21:07:08 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 15 Jul 2020 21:07:09 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 15 Jul 2020 21:07:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 15 Jul 2020 21:07:45 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Jul 2020 21:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 15 Jul 2020 21:09:18 GMT
EXPOSE 4222 8222
# Wed, 15 Jul 2020 21:09:20 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 15 Jul 2020 21:09:21 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dd35c9a62007b6ded1ca968562be97de62ea3e2b3c7db85f4a50baaa9efecb`  
		Last Modified: Wed, 15 Jul 2020 15:09:33 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6c591c0a8170250552e7e384d3a79de15e68f382a34d1e5752c6c7ab0cbfb5`  
		Last Modified: Wed, 15 Jul 2020 21:13:48 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1d80c963f67159f6b9cbf927c2fd4bdf00c6f73353f96b1baf98daaa6c7cb5`  
		Last Modified: Wed, 15 Jul 2020 21:13:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e611a275568f5c39624077dd6209104cd19177aeced5c0b7e0f00e9e7aaa2b`  
		Last Modified: Wed, 15 Jul 2020 21:13:47 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c167f6381ec0f43e4cfcc10919a987bf178e694e5b2b4cdff32b39161c9411f`  
		Last Modified: Wed, 15 Jul 2020 21:13:47 GMT  
		Size: 4.8 MB (4800424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffec8d449046498ebfc5d1d69f93ec54cb307a7cd7b2a46003d66c63b69edbcd`  
		Last Modified: Wed, 15 Jul 2020 21:13:49 GMT  
		Size: 15.1 MB (15065705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b0372f086e7590d8b3b4f0c70dbe11c050d24011d09293dc8e1978e0cd25f0`  
		Last Modified: Wed, 15 Jul 2020 21:13:45 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e0c6e97c31e972420da6bed768b9f5fb8a5644521f539e83e4ed9c4b13155`  
		Last Modified: Wed, 15 Jul 2020 21:13:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d615621d3c5ab9becb58f63dd233e553d272091e768dae0074d3c0bd9d124`  
		Last Modified: Wed, 15 Jul 2020 21:13:46 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull nats-streaming@sha256:daf9e5a9590ebd64d8629288af9923d028c3130df505f7ff6d2badab5fdb36a4
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5758611587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14d84aa3c32e47f13a9aa728500047ce78b9247002ddf8006b19e08bc213366`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 15:05:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 15 Jul 2020 21:09:46 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 15 Jul 2020 21:09:47 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 15 Jul 2020 21:09:48 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 15 Jul 2020 21:11:13 GMT
RUN Set-PSDebug -Trace 2
# Wed, 15 Jul 2020 21:13:11 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 15 Jul 2020 21:13:14 GMT
EXPOSE 4222 8222
# Wed, 15 Jul 2020 21:13:15 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 15 Jul 2020 21:13:16 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1430ee68db5fe3026683f1b7c74f31ae748da71bf8ad611efede726e9e036b1`  
		Last Modified: Wed, 15 Jul 2020 15:10:21 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bee39dfb46c142a6dd8c7b99236cd36b36ed56346c403d7be4fb8623f9b8d5`  
		Last Modified: Wed, 15 Jul 2020 21:14:20 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7de9a5c713789f72af564cdc5f28c0dba85d4b95332f815a7d0ba032170616`  
		Last Modified: Wed, 15 Jul 2020 21:14:20 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ba6847dae4e00016f022ecb49741fecdfb048a3cf945beed074720180415ff`  
		Last Modified: Wed, 15 Jul 2020 21:14:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62e9ba6e0d6f49e9b722408130b963a54818538f1d9f7f3856239f03795f5ab`  
		Last Modified: Wed, 15 Jul 2020 21:14:19 GMT  
		Size: 5.4 MB (5379274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c099f3a69d1984acb328df528418c5d92a1a208d1949990ebaac1b8256e12b9`  
		Last Modified: Wed, 15 Jul 2020 21:14:21 GMT  
		Size: 15.8 MB (15761002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec2f283e382f964302246e46c7558554d80d222708541d0ad673e912fd538f4`  
		Last Modified: Wed, 15 Jul 2020 21:14:17 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748659c661458abcab3c6af30d446fd311404a91f63607c45c10b8620a484270`  
		Last Modified: Wed, 15 Jul 2020 21:14:17 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed56fa4c13c0af0264cde0de3b1c5c2d040ed6e725662e6b19057481de9dd0f`  
		Last Modified: Wed, 15 Jul 2020 21:14:17 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
