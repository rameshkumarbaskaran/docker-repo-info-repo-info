## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:22465402ce357b9bbbfaf3853dc904e34184d828edb472868673c38a02e6b7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats@sha256:03f97fcd9cd3319e75ebb981c3af42c2a88b95e2f484ec3aeff1c1d734b063ae
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1656404940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c30b9773f8a110b38afb110496f37de9933ce5b90e82dd0a8f843b9ba35acae`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:17:20 GMT
ENV NATS_SERVER=2.9.18
# Wed, 14 Jun 2023 20:17:21 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.9.18/nats-server-v2.9.18-windows-amd64.zip
# Wed, 14 Jun 2023 20:17:22 GMT
ENV NATS_SERVER_SHASUM=139c2d63193d7df39894b144fb08a40e15548f89087e1932617239d36ab0c901
# Wed, 14 Jun 2023 20:17:45 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:18:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:18:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 14 Jun 2023 20:18:45 GMT
EXPOSE 4222 6222 8222
# Wed, 14 Jun 2023 20:18:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 Jun 2023 20:18:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b020d266b90663e4a08cb8a268fc54c8cb1a9241c336a6e6f1729e16f0d135e3`  
		Last Modified: Wed, 14 Jun 2023 20:19:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c30d3a997645f33d20fa13eac290bff874dafd9baba7e27c28a05e7d632da18`  
		Last Modified: Wed, 14 Jun 2023 20:19:33 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6755ab33ed91c39427a9de6eabcccda0b4c01d801297a953d3c40fc83068615a`  
		Last Modified: Wed, 14 Jun 2023 20:19:33 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7048ba31253f6a437a2d43c565b8623badd9ae698c3ea2bf3943ee00766b4e8`  
		Last Modified: Wed, 14 Jun 2023 20:19:33 GMT  
		Size: 312.2 KB (312236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a85805c362c48c21ea4be8fc389308321d19232ae7d53303327a8555a8c84`  
		Last Modified: Wed, 14 Jun 2023 20:19:32 GMT  
		Size: 5.5 MB (5459741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5bcfa853498f5e05ae2c6947a076308947a387e316039424fc1f12d648e8a0`  
		Last Modified: Wed, 14 Jun 2023 20:19:31 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cb7e8f0d98fec70cae8dba259447711fa6d4b0fdb1762b2b9a2344a07731c6`  
		Last Modified: Wed, 14 Jun 2023 20:19:31 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1c9c860ba23fd419460f5b0eff7bd724ccee531b796c44310f67d24a8ac6c`  
		Last Modified: Wed, 14 Jun 2023 20:19:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e308156f464715dfbae62b48af7822328ee169a1c20a534a5a622ef9bbb1ce`  
		Last Modified: Wed, 14 Jun 2023 20:19:31 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
