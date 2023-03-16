## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:2edfcef43806cfc5b4d830769a6646776a0b72a002a03c7fdee023f3558abaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.4010; amd64

```console
$ docker pull mongo@sha256:9f3fae264f8ff6149afa4e14524e19fec13a8d9487026091fdd9e393d3c8114d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2478522517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0889300675592c2aa4895dfc10b269759d45d84485e03d0d577fc9ae05ee3413`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Tue, 07 Feb 2023 10:44:53 GMT
RUN Install update 10.0.17763.4010
# Thu, 16 Feb 2023 00:42:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Mar 2023 22:19:29 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 15 Mar 2023 22:19:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.5-signed.msi
# Wed, 15 Mar 2023 22:19:31 GMT
ENV MONGO_DOWNLOAD_SHA256=79327a9901a39182dee2d74f84e46b4c6b1416cfc2c0cee791322ea82dce0388
# Wed, 15 Mar 2023 22:23:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Mar 2023 22:23:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Mar 2023 22:23:20 GMT
EXPOSE 27017
# Wed, 15 Mar 2023 22:23:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c707e813c8220ab3c92b6eb7b445ee0b1a485686ff62014ae32c17d2b1b6`  
		Last Modified: Thu, 16 Feb 2023 00:29:31 GMT  
		Size: 255.0 MB (255014079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531f6c3ad9784fc2870ea5ca08c4adccd9318602ed534d822e12b8b658a7b0b6`  
		Last Modified: Thu, 16 Feb 2023 01:37:30 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31bc0c316a10dd3887ae46685f518bee0dfe52e0316f16480ce0309f412871`  
		Last Modified: Wed, 15 Mar 2023 22:31:07 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e71b2027be5f93c493b2299b6038647eda759f0bc04238cb261e56bc1c431e`  
		Last Modified: Wed, 15 Mar 2023 22:31:07 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0e8d040ecf2763a2e43b5535b3679d5ffe2ab9033744863685fc4488c80f1c`  
		Last Modified: Wed, 15 Mar 2023 22:31:06 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3df5107aacab1180d36e1170ad077bb06b6337949342f2be46585f571f9ef8`  
		Last Modified: Wed, 15 Mar 2023 22:32:33 GMT  
		Size: 515.6 MB (515554769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374337d4a98150b99453e34ec337f3787e30032780592047440585a75bd7559c`  
		Last Modified: Wed, 15 Mar 2023 22:31:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b55380c8c4db25b58f2064e7c5be36977268d994283b729f973ffdb0cbd03`  
		Last Modified: Wed, 15 Mar 2023 22:31:06 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1548d3f95e7e8cf086930421b5c3d4d6ba49cc4a77ea2ffa7cc6089c2bc6d22`  
		Last Modified: Wed, 15 Mar 2023 22:31:06 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
