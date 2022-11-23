## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:4f72ffeee3f442a6b1a1ced925fef19af25fedeb5ba7f87fc6ef203e159d24bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:eb26edada206406e1ddd6424a52e4dfff2877433459fe387cc84a5f38f5f5216
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2792775739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5716f4c1df21ae8729977cbb55ac61225683b46793d851a028e4d75f3b19a740`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Wed, 09 Nov 2022 14:41:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 22 Nov 2022 23:16:14 GMT
ENV MONGO_VERSION=5.0.14
# Tue, 22 Nov 2022 23:16:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.14-signed.msi
# Tue, 22 Nov 2022 23:16:18 GMT
ENV MONGO_DOWNLOAD_SHA256=d67e360f14dd4f1516d322d85c9c9aed3ff0bcf5e08b50ea9e60f64ee4817720
# Tue, 22 Nov 2022 23:19:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 22 Nov 2022 23:19:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 22 Nov 2022 23:19:15 GMT
EXPOSE 27017
# Tue, 22 Nov 2022 23:19:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcc0cd10e58716558145d847bcea390e3840d172df19b8d0f08a57dd985262d`  
		Last Modified: Wed, 09 Nov 2022 19:02:46 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a77005615f9f5d5dd07761e68c9faa7bd4f5167699326015827d0d1e07e81b`  
		Last Modified: Wed, 23 Nov 2022 00:18:28 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74dcccec48fd111438f2b593ba9d3b06ad4a9bda63a2cbff8756cbfa76d72f`  
		Last Modified: Wed, 23 Nov 2022 00:18:28 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22f4ec036a495c89578f6ad902bd4d6033884714bd7390b2182eb34fb2ce9f0`  
		Last Modified: Wed, 23 Nov 2022 00:18:26 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513b3c3c4072685e792216228161f252ac2c43db50a2797317c033f7f0c0e6b`  
		Last Modified: Wed, 23 Nov 2022 00:19:27 GMT  
		Size: 311.0 MB (310997180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11e08f01b7cb0174a19ce846b9ce40a2ac41d0dbebbee2e9ad7dc050a1295c3`  
		Last Modified: Wed, 23 Nov 2022 00:18:26 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0189fee0552a41a2a27c27531aef6cc2420c16ec6821a254257b3575dca6fdae`  
		Last Modified: Wed, 23 Nov 2022 00:18:26 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247133578db1566f3d0c947a5b4032ec52f62581802fa916d86e0f92d258353b`  
		Last Modified: Wed, 23 Nov 2022 00:18:26 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
