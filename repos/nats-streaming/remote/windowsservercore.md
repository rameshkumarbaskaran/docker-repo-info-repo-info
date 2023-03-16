## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
