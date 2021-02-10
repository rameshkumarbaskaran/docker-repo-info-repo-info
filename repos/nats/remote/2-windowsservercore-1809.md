## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:2fb4f5152a7090daf80d1eb69ea6f01297d7756627352123a7e6a4fbe1ecd62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull nats@sha256:e803d4af76b87c5ee325ea177a909a3e9bcd2ea13950c784657f8b88235f9a2c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2457715817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cd0871672b58029cd30133fa0d50cd576fef8abf523764532d1202397e4b99`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
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
# Wed, 10 Feb 2021 16:00:30 GMT
ENV NATS_SERVER=2.1.9
# Wed, 10 Feb 2021 16:00:31 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 10 Feb 2021 16:00:32 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 10 Feb 2021 16:01:00 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 Feb 2021 16:02:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 10 Feb 2021 16:02:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 10 Feb 2021 16:02:09 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Feb 2021 16:02:10 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Feb 2021 16:02:10 GMT
CMD ["--config" "nats-server.conf"]
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
	-	`sha256:0f46e983d7f8b68b4a1248e9c9fb11adfceba23aaf3c7efc89fa006eb4b18532`  
		Last Modified: Wed, 10 Feb 2021 16:06:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fa948ce697076ea3364031950f24f9ee284dc7645ebff21e8850848bcf7cd3`  
		Last Modified: Wed, 10 Feb 2021 16:06:02 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097ef991fab9272eeedc7e351b95a2c867042ac0fcde5a55c661b58aefb2cd9`  
		Last Modified: Wed, 10 Feb 2021 16:06:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cceafed9909b219c390b816254428a161e85d21fba6c39ca9bcbdf1f61c13b0`  
		Last Modified: Wed, 10 Feb 2021 16:06:02 GMT  
		Size: 5.0 MB (5026888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac7adff44f48b747c52f8dc11c4a3c14a98d17ec6cfd2a5c43863538750169a`  
		Last Modified: Wed, 10 Feb 2021 16:06:14 GMT  
		Size: 13.4 MB (13409392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8f9fe35f2cc984a6525c88d9c9a889c2d9c84e24575d9295842f0f99beafde`  
		Last Modified: Wed, 10 Feb 2021 16:05:58 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353d71e76856488c1ce43641c25879592250d39e2e9045ae1b1a026015b3a5ab`  
		Last Modified: Wed, 10 Feb 2021 16:05:59 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a200002fe27bc523def6edf799cea74e0e7fb0d8e28376e1f46c4ad720bdd4e`  
		Last Modified: Wed, 10 Feb 2021 16:05:58 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8504098667b45e870bbaffaa140702247b6ae54c586884f1fbcdca80778eb72`  
		Last Modified: Wed, 10 Feb 2021 16:05:58 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
