## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:fc581e741b67c6a85f2753f679df1d63f7337ec84e12120ffa8101f02f1416f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:ebb36e587763fa2dfc9e5790e6590f0b156f36eb41176546e7153cf8c10c57e7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3023958332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8d3b97ba81a2ea22a76f79e6e905914440a296f3b09ea1cbb7d3001df9fc16`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 16 Nov 2022 19:27:33 GMT
ENV MONGO_VERSION=4.4.18
# Wed, 16 Nov 2022 19:27:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.18-signed.msi
# Wed, 16 Nov 2022 19:27:36 GMT
ENV MONGO_DOWNLOAD_SHA256=e647d6432ceaf4949bd989e10bad5cd10788f87c41ac2fc054a6e6122503fc64
# Wed, 16 Nov 2022 19:30:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 16 Nov 2022 19:30:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 16 Nov 2022 19:30:03 GMT
EXPOSE 27017
# Wed, 16 Nov 2022 19:30:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9046bb62c9497aeb70d28a9b2fac88279cd7482b837deb8e27caccec3c6fc8a`  
		Last Modified: Wed, 16 Nov 2022 21:26:45 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164d899d8285b6b862f278692b61b1555773d16639bc6a892a5e045ad6de30e6`  
		Last Modified: Wed, 16 Nov 2022 21:26:45 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6cb175825173208766a236a0ee73ce1474a1f66f69df68bbe780095400bd1e`  
		Last Modified: Wed, 16 Nov 2022 21:26:43 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5549969ec64fbc89f7225b823388c93dfb93f6b27293c1269753be5d91284dbb`  
		Last Modified: Wed, 16 Nov 2022 21:27:29 GMT  
		Size: 245.4 MB (245361956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8571e75a4d8d2443e8b286554310b591cc4fcf9e894b0cf2e288b438760223c1`  
		Last Modified: Wed, 16 Nov 2022 21:26:43 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f1e1555106723b4e54691b5125f9e51ec7f2ff50e9fe7cefe5e7af09a52ff0`  
		Last Modified: Wed, 16 Nov 2022 21:26:42 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9576315adb96c8191c2a2f100da9f744647aabd5097ca93f112435a144a50036`  
		Last Modified: Wed, 16 Nov 2022 21:26:43 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
