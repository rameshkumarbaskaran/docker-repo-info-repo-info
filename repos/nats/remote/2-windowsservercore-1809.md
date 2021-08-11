## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:2558ef935864c9d97c8731a8be51caa75b7780837c6176fa9aed5fbf3fff08e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull nats@sha256:0e78bad63f72d1020403cf996909467537a3c9165fbcfd06b88f7406f59599bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691258982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a47d7557c24bcb648de02138c009970f8531bdbd85cfd90d84c37cd555de5e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 13:42:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Aug 2021 16:48:51 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Aug 2021 16:48:54 GMT
ENV NATS_SERVER=2.3.4
# Wed, 11 Aug 2021 16:48:57 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.3.4/nats-server-v2.3.4-windows-amd64.zip
# Wed, 11 Aug 2021 16:49:00 GMT
ENV NATS_SERVER_SHASUM=729dc0609e0461aa5fb893c85c04c6b6afa40945183d8d8324d03186d1678a99
# Wed, 11 Aug 2021 16:50:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Aug 2021 16:51:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Aug 2021 16:51:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Aug 2021 16:51:43 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Aug 2021 16:51:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Aug 2021 16:51:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c613f4c34660a122de754415a884afe6b12172ac3ce792a2e4aae831cc8b2e27`  
		Last Modified: Wed, 11 Aug 2021 16:25:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d8e65d39d1b09c34e0dadad1a6b7818f430fb13ce2ff8d70c549b137f9131a`  
		Last Modified: Wed, 11 Aug 2021 16:56:54 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e177f56ca15df09ff11b20af8edb24572d53b8a9c977780eba79cfc86f67d96`  
		Last Modified: Wed, 11 Aug 2021 16:56:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18c2fb6029597619ad5a6cd36736ab43936eeab0312eb830583939966d2bdc0`  
		Last Modified: Wed, 11 Aug 2021 16:56:52 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f5d8b50ae3ebddabcf17583e39acb5b72718f2f61240b066e4ffcfbf5065b9`  
		Last Modified: Wed, 11 Aug 2021 16:56:52 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa030a209d0a740d0824245921faba93d25cfc8d9058fedda47e174f03f329c`  
		Last Modified: Wed, 11 Aug 2021 16:56:52 GMT  
		Size: 351.6 KB (351552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61129d3a4e1ad65d8e5be0b1554d2d9afb8bec36fd36cc12db019f0637356e8b`  
		Last Modified: Wed, 11 Aug 2021 16:56:51 GMT  
		Size: 4.9 MB (4896175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6fc46d367ad12b2a10dd2601bc445f98fb0cfef1e1d72d5926485f3a8bacdb`  
		Last Modified: Wed, 11 Aug 2021 16:56:49 GMT  
		Size: 2.0 KB (1975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfb7f25142dd9717a7f3f09690ed063b17a81761a5228ffe5b7c5c52dd5f064`  
		Last Modified: Wed, 11 Aug 2021 16:56:49 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f5a44d5a1730d95e68ab4e9d77c3d180b882b61ab52c7fe73b20bcb6d26996`  
		Last Modified: Wed, 11 Aug 2021 16:56:49 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee7e5860655f537c28fe4b9245928ccbdafff272ad5347db69e741d93e932e`  
		Last Modified: Wed, 11 Aug 2021 16:56:49 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
