## `nats:windowsservercore`

```console
$ docker pull nats@sha256:46b35fa823d04b32db5488256a4e2944f53e4181575d5f6e12539188678e2580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `nats:windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull nats@sha256:9443c12faacb5a3a68e7d72c8939deefb2240d28d87e0a130ab7200b69d0d0b6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1945661654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f797d8b6b26eabc171bad981e86752e0d91c7230c77ea22448b266347dcba2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 22:38:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 14 Jul 2023 00:00:18 GMT
ENV NATS_DOCKERIZED=1
# Mon, 07 Aug 2023 19:15:34 GMT
ENV NATS_SERVER=2.9.21
# Mon, 07 Aug 2023 19:15:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.21/nats-server-v2.9.21-windows-amd64.zip
# Mon, 07 Aug 2023 19:15:36 GMT
ENV NATS_SERVER_SHASUM=43df40bcf81e819e3467a31c548643439d4200486f3032c61ae4b134243f8796
# Mon, 07 Aug 2023 19:16:32 GMT
RUN Set-PSDebug -Trace 2
# Mon, 07 Aug 2023 19:18:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 07 Aug 2023 19:18:10 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 07 Aug 2023 19:18:11 GMT
EXPOSE 4222 6222 8222
# Mon, 07 Aug 2023 19:18:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 07 Aug 2023 19:18:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b452db6d50a62b6e0e8dadb19715cfcf62cf73e54b5d3bac96621c1093673c`  
		Last Modified: Thu, 13 Jul 2023 23:25:18 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f8ca4b8d322e27c827c0ba667217bc04a39b69f5f483d5f2f9726e6d42522e`  
		Last Modified: Fri, 14 Jul 2023 00:03:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90ab1308c1b3263ff0620e4115fd86c86b4477f3d922b9a7c4e50f49d30e16f`  
		Last Modified: Mon, 07 Aug 2023 19:19:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a1d53756050ba20a10b2844df7ebd4b8aaebb4216109336ebcac6b8228a6e`  
		Last Modified: Mon, 07 Aug 2023 19:19:14 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa8c44e7d06cf6c31fe1c6ad674859679d240909eafb6ed851e6d03356e9aef`  
		Last Modified: Mon, 07 Aug 2023 19:19:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497c7efbe8bd1163f631faba31b9bd8953f9f3ee327fb0060c54a2c16934dee9`  
		Last Modified: Mon, 07 Aug 2023 19:19:13 GMT  
		Size: 242.8 KB (242807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac00b0f950d64129fb2b469dd94cbd7846de63709c81cfc4d0e3c930c510f05d`  
		Last Modified: Mon, 07 Aug 2023 19:19:12 GMT  
		Size: 5.7 MB (5717098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bedf7e26406873ad052c3ba6453d62c9e1fcc1dbc7b74dc2be837c4529c3f30`  
		Last Modified: Mon, 07 Aug 2023 19:19:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1613adc18de33d44a97750bc2c0fd12271578df5c6bd12f6511910d9729c9287`  
		Last Modified: Mon, 07 Aug 2023 19:19:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafa9703f3bfc906b6e68f1b55062a092481086bb68b7ab9a630c1124672be06`  
		Last Modified: Mon, 07 Aug 2023 19:19:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6f034130b765c9e3e852fa793501d66174050c6b979dbe5c697c4a84d909e5`  
		Last Modified: Mon, 07 Aug 2023 19:19:11 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
