## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:0728f2a6f38b6ddc9220b714320ea805334d12ff55fe3085f54fd4c3990ffa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64
	-	windows version 10.0.14393.4225; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats-streaming@sha256:f37e01c95a35e80a9ded4c68744089da72385d2b912ea64785af120e5dfac46e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459529339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b413bdbbbc445bd56eec6684f454ad90530794c0c418fe4d91945d27158fd2ca`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Tue, 09 Feb 2021 20:26:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_DOCKERIZED=1
# Mon, 01 Mar 2021 23:37:33 GMT
ENV NATS_STREAMING_SERVER=0.21.0
# Mon, 01 Mar 2021 23:37:34 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.0/nats-streaming-server-v0.21.0-windows-amd64.zip
# Mon, 01 Mar 2021 23:37:35 GMT
ENV GIT_DOWNLOAD_SHA256=00bd52804208a52014f518836198a3ebcd513fc5029eda9de2b4ef846f5cb828
# Mon, 01 Mar 2021 23:38:06 GMT
RUN Set-PSDebug -Trace 2
# Mon, 01 Mar 2021 23:39:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 01 Mar 2021 23:39:27 GMT
EXPOSE 4222 8222
# Mon, 01 Mar 2021 23:39:29 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 01 Mar 2021 23:39:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:751b8860e89a7e6999d74a11dc393620b118057ad881cb87f1d6e3653cb2db43`  
		Last Modified: Tue, 09 Feb 2021 20:48:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f01e717591f83c73890556e7a4c77e53caed8daf6c9b0150f497e094a4a698`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee7e8f68acf02f1803fbe58fd1c98e5136b5c448a9ac12d39f5a4a64ce198a8`  
		Last Modified: Mon, 01 Mar 2021 23:43:41 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c75a51835c930004670181ad34afd7c2e90ba762a6696cfc732939750e5023`  
		Last Modified: Mon, 01 Mar 2021 23:43:42 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d34a3454dc6e83cea274b8fd2765fef221836a6993fbe56ceac434981fb5b0`  
		Last Modified: Mon, 01 Mar 2021 23:43:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0dcdeb9a6756964b7928054f4f2182d16a35b34ea18396a0d4b38cf484fd9f1`  
		Last Modified: Mon, 01 Mar 2021 23:43:37 GMT  
		Size: 5.1 MB (5051217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34eb42fac48c971f1a0135c6584d1083bb0e536911e46b1a1e389c4ffe729a8`  
		Last Modified: Mon, 01 Mar 2021 23:43:41 GMT  
		Size: 15.2 MB (15200127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f665eadac63d2ed583f4d30a7d28791f710880674a828e61d8c2105ce70655d3`  
		Last Modified: Mon, 01 Mar 2021 23:43:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fe9508026c89dd38a20a05c48fc44dcb7d86441cdcb88457d74e6625ee04cc`  
		Last Modified: Mon, 01 Mar 2021 23:43:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024aa4f6d5eeceaecd71aa08ba9e78ea00fd32ea15890f9d228db2fc18580407`  
		Last Modified: Mon, 01 Mar 2021 23:43:35 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:windowsservercore` - windows version 10.0.14393.4225; amd64

```console
$ docker pull nats-streaming@sha256:eb47ac16c5b855632476a7b18bf7e414b1bd8f550cc6076715b87e5f0b3a531b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816649326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ab14b94a5ce8d1e02ac5175112977ea6d3a9ab5a4b1d4f23979ef50fe19563`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Feb 2021 20:28:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Feb 2021 16:02:35 GMT
ENV NATS_DOCKERIZED=1
# Mon, 01 Mar 2021 23:39:57 GMT
ENV NATS_STREAMING_SERVER=0.21.0
# Mon, 01 Mar 2021 23:39:58 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.21.0/nats-streaming-server-v0.21.0-windows-amd64.zip
# Mon, 01 Mar 2021 23:39:59 GMT
ENV GIT_DOWNLOAD_SHA256=00bd52804208a52014f518836198a3ebcd513fc5029eda9de2b4ef846f5cb828
# Mon, 01 Mar 2021 23:41:08 GMT
RUN Set-PSDebug -Trace 2
# Mon, 01 Mar 2021 23:42:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 01 Mar 2021 23:43:00 GMT
EXPOSE 4222 8222
# Mon, 01 Mar 2021 23:43:01 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 01 Mar 2021 23:43:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ac4a230905430e1aea27172a9432f576cc4a530e72bea516a2b304d2b7e9c101`  
		Last Modified: Tue, 09 Feb 2021 20:49:11 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc28e30e89dab2d0b2b2f6c3114771d9d803d5942c730de78d2dd457ad4ac40`  
		Last Modified: Wed, 10 Feb 2021 16:06:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e865ae49ff7ab275634dd5c255d968f5f0f59d027134ad6df4133fa52d0d0af`  
		Last Modified: Mon, 01 Mar 2021 23:44:20 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f73566aa9bcff8499433bf39ef4bf7fbf46bcaf045cdfe4cdc3b374fd4ac3`  
		Last Modified: Mon, 01 Mar 2021 23:44:20 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322aaa185ec2b5e90cc9eb8c57ee82a54b439aafd42bb20b59e2736d28cdc8e1`  
		Last Modified: Mon, 01 Mar 2021 23:44:20 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f75278df3ba6220910463178e2fd69782bbc0c3abbbfa41ddd271358106f32`  
		Last Modified: Mon, 01 Mar 2021 23:44:21 GMT  
		Size: 5.7 MB (5657685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36a484255a580d8cbe179712aec8211899c8500471dcd9802790090750911c0`  
		Last Modified: Mon, 01 Mar 2021 23:44:36 GMT  
		Size: 16.0 MB (15967963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1eabaebec46e6111a59bec9221d1e0d4973de580e30a453fa7bbb2e1ad9385`  
		Last Modified: Mon, 01 Mar 2021 23:44:17 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fef8d63616ebeb7cc5aa29815610700aeccd828419c232dd4b8ba2edc47f8a7`  
		Last Modified: Mon, 01 Mar 2021 23:44:17 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32683573142d691c7c5ca7fbebf8c2d37bd0ab61abafdf7be2690d440dcad8c0`  
		Last Modified: Mon, 01 Mar 2021 23:44:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
