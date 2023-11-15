## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:ee873213ce0dc96ecfcb9d4b226cf895ae03dfd44cc5aa9e320459b8f65f96f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

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
