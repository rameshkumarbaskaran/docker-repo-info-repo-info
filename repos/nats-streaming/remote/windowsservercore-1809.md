## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:682087027e66bb745b188d0b1ca9a3cf0f0b0a2e6ae04d338d3ee24aba728347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats-streaming@sha256:41dea33a881e6753c01723311502cb94f8a97aafc6478b9ea509427718efe396
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355727338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ad1a13d9266e709fb7ce9d5c68af974d294037365ef37ea04f1d716640fa0`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 18:28:09 GMT
ENV NATS_STREAMING_SERVER=0.18.0
# Wed, 12 Aug 2020 18:28:10 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.18.0/nats-streaming-server-v0.18.0-windows-amd64.zip
# Wed, 12 Aug 2020 18:28:10 GMT
ENV GIT_DOWNLOAD_SHA256=a0c0261df2ce589fe9706617323e06c5bcae70511112eae921681b1169674bc8
# Wed, 12 Aug 2020 18:28:40 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 18:29:59 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 18:29:59 GMT
EXPOSE 4222 8222
# Wed, 12 Aug 2020 18:30:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Aug 2020 18:30:02 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e3adb80435dc87212402721793806fcc57e37207f136d54dab4564112a8f2`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4681d5724bac38ef07123cd742c5f102015501251bc7a43e6aa7c4fbb4fd0033`  
		Last Modified: Wed, 12 Aug 2020 18:34:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a009c706d5d1f72c29aefca58fafbd704158ee9bb86fcb49dcd4611eb203c8`  
		Last Modified: Wed, 12 Aug 2020 18:34:12 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19562909ec2ea373bb8b31c51d91e026b676b446ea09be5b70f88ebb1c131f`  
		Last Modified: Wed, 12 Aug 2020 18:34:11 GMT  
		Size: 4.8 MB (4795257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83f2272ddbd6f09b2b0b150da9d1955783526da27ab0defe7c7869de01ca1c`  
		Last Modified: Wed, 12 Aug 2020 18:34:14 GMT  
		Size: 15.1 MB (15056067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40d2f1e409336109270be5bebd824215d52616a95d951f8b5a44fe582b476fb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda8b4f710c94e9142c8cfc527ba116957c89714da5649f62cd51c31a4417bb`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e0032c0caaa897adb6fdda846d8b7c7fae85fbf219082a869022fdb1f7d62`  
		Last Modified: Wed, 12 Aug 2020 18:34:10 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
