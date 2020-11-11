## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:b6b8fea1692f62d7fa95cbc1c26c327ebfb7fb462bcf244529c6673c4c2b9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull nats@sha256:e96c2ce3f49ae39edf8e8e1f96758444fa789188ab5ab1fbe715e87c00dfb264
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406135673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc73d352c4de0fc8d86ddc189c6f2d26168ad1020dfd91d6d9772dfdbac699f`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 14:18:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Nov 2020 17:01:32 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Nov 2020 17:01:33 GMT
ENV NATS_SERVER=2.1.9
# Wed, 11 Nov 2020 17:01:34 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 11 Nov 2020 17:01:34 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 11 Nov 2020 17:02:05 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Nov 2020 17:03:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Nov 2020 17:03:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 11 Nov 2020 17:03:16 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Nov 2020 17:03:17 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Nov 2020 17:03:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e03cd29396986910a2aaaf968e93bebcaf4b0101821290e0560b401893615ccf`  
		Last Modified: Wed, 11 Nov 2020 16:53:20 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d59214fb7b605a325f942085c8f9dbcc4fa01cb3626a6eaf07a0e437729d5e4`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f6a932dbe771300fd54c1918eae3fe1ec27eefaf4c2cb53158ce42d2297f2`  
		Last Modified: Wed, 11 Nov 2020 17:07:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ecf26d504fce34d82f86380c00abf6402c0189b04f8d4c648b60283ace53a`  
		Last Modified: Wed, 11 Nov 2020 17:07:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b8b1e73766a6adbbee255728fe047b200f2abe18f2b259ea217a72926a1108`  
		Last Modified: Wed, 11 Nov 2020 17:07:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa082c2c81dccf916c772d702f70753b5b9793b2faa47470e438c3a621353a1`  
		Last Modified: Wed, 11 Nov 2020 17:07:35 GMT  
		Size: 4.9 MB (4850088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b9c60b746fc66f5007678df2370427e239055237ebd493bf86243bdbe59f28`  
		Last Modified: Wed, 11 Nov 2020 17:07:42 GMT  
		Size: 13.2 MB (13245485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6573bc87586cad4a469241fc3d46d8653174d7b032ed89811aeaae906eba99`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8806ce4aec8c8792d4cb2df3cad788f46b2dbf3a8ef1b720e6d55e2020a42b`  
		Last Modified: Wed, 11 Nov 2020 17:07:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446b0cdc209906b12342f5fbc691540f0fa2ba39a097b705b34940e9d3d93ac`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643cd43bc5e1c2cc358f960136f70b9b06da49a92e9d3f295689fdc378206c2e`  
		Last Modified: Wed, 11 Nov 2020 17:07:26 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
