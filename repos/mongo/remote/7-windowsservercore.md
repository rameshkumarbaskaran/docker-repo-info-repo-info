## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:4d16679f4103c194cfc4e403135b0dad6f60b8a4d1b8a10923f7a60f4b2d3219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:b23f0f330b3d5d30ad39c5174003ca84f243e06ea13b07554eb9445821622b29
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2472193755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8cc4abe576bee596834fb307d441369b384dba13fc5c8c20a76a4dffb6f058`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 02:54:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Nov 2023 02:25:52 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 02:25:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Wed, 15 Nov 2023 02:25:54 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Wed, 15 Nov 2023 02:28:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Nov 2023 02:28:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Nov 2023 02:28:24 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 02:28:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c131d94d08cb023367d3fd8434c336e9d07495660367cc521ddff869fb44dc7d`  
		Last Modified: Wed, 11 Oct 2023 05:52:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9021d3f18c544462ba44d454c8e899c9e85e46c764c333f9b8282aefa37e804`  
		Last Modified: Wed, 15 Nov 2023 03:10:41 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bd86fbbe395214807b203a5894e8dc630e438309d319ff06357646c1ce74a3`  
		Last Modified: Wed, 15 Nov 2023 03:10:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447b3610a31003c67cfca7f209e9599e532bde8b4011866d6e15be71339fc1ba`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392c63100c195055b8384d40e5b9a50b53ea32d015a8af77ca6ba3727e3fcfe3`  
		Last Modified: Wed, 15 Nov 2023 03:12:28 GMT  
		Size: 612.3 MB (612340679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f8e1c7b300cb23643b9439eb6cf46d36fb7aeeb1e6db58f072d7816aa284ca`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae3a12c8fc1f424608bad1bea4d02e38d70ea282746a22480dee5837be631`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847bea7c39edeb6d7828062029a9b7c222665024386c12233affca3384c0381`  
		Last Modified: Wed, 15 Nov 2023 03:10:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:f9a266f5dd083a659612b3ddae1d0ba57ecd8dd2caceff80bb2ce86ccaf330dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2643981269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7da1c5fc060225b9ae1a5eef1ddb7f5d28c046c15a35dc2de196aaa90856a62`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Nov 2023 02:28:35 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 02:28:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Wed, 15 Nov 2023 02:28:37 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Wed, 15 Nov 2023 02:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Nov 2023 02:32:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Nov 2023 02:32:19 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 02:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7e93b7ab1fcb2401675153bbb5e9cba8cbf2dab09628d41df888e30cc703c1`  
		Last Modified: Wed, 15 Nov 2023 03:12:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90151399a52e5b0f945c856cb634d1ab406c4e7a2c4f62c01e0ed50bb05b34de`  
		Last Modified: Wed, 15 Nov 2023 03:12:48 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d24900fb65faa9f4c9f0ff4fb614e8e7be8e5be6564593aaa5049d4b96e6331`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcfaf21e9c7a45ca514db3921fc2dfca01ec692f9cd37791f72578adc2fca6e`  
		Last Modified: Wed, 15 Nov 2023 03:14:37 GMT  
		Size: 612.4 MB (612380773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97f639746dd64b3bce4df1f365382c354f265550f6b8db5193cfa33a094f7f1`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b9e3c0fa0e5aaaa6afdb3cbc0a7f8dffa9f9c02cf14058bb5e8c221eec8d0c`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706e46f7ce84f8429f8b571986afe09bb12c5c9da3d8d75e63894650e4b870ce`  
		Last Modified: Wed, 15 Nov 2023 03:12:46 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
