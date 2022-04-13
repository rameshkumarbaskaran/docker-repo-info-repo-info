## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:855ca6219a87bf4c975ec8613486e4bf3a4ca109f02492533844c1cd96f933ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull mongo@sha256:7e25d485adb1eec3fc5a6ee85cd63e14f252ce059eb143b17bc8141558b4de45
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2469905145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00466b4e8e7490bdfe3d351743a806f05d7cd6a1157d8553a532c3f69e700757`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 12:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 17:36:30 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 13 Apr 2022 17:36:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.13-signed.msi
# Wed, 13 Apr 2022 17:36:32 GMT
ENV MONGO_DOWNLOAD_SHA256=0eb6e5c43c74a992301529515c52b7e326239cd12649fb6f91e807fcbbf06f39
# Wed, 13 Apr 2022 17:37:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 17:37:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:37:59 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:38:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2a5d28823cc7f2a78cb6b52a2cadb350e978705d7634adbcfbc4bd80d4637c2`  
		Last Modified: Wed, 13 Apr 2022 14:11:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88f4816091580c70a2e7d956f552d7046d7315b8d055eae6afe97d076626dd`  
		Last Modified: Wed, 13 Apr 2022 18:12:39 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf75ee62601c04ba8418e070482647ed7f1053db8bc6a22c9ad32aff56f86e9`  
		Last Modified: Wed, 13 Apr 2022 18:12:39 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b902054b60fc8d4a07bbbd9c8afcea225b1f78b34d0aade7dea945f82c9301b`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f2bbf5932c9d7944fe75ce8cae1f7b1bdb07db3acc38bb4cb9b9652282372e`  
		Last Modified: Wed, 13 Apr 2022 18:16:53 GMT  
		Size: 242.9 MB (242940409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202910162eb1f0313fa93e562bb2ca41aac77416b173b3ae8e5abb051ca1fc16`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38a45180fa43fab88ad9ef517b812132c8178f8f7d118cdc2554b485f75c9b`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86221664f145c9d5df593a0eddab4f09cac704aeb90533a026b500df44f6890`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
