## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:f25eaf5d853b269bc17cf8507b8a58169176f6d752ed49744bd079abdafe1ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull mongo@sha256:665dd6fc471cce6e13409c6e74a8eaf93f0f749bcc4fbd0bdcb3821217298464
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3016837476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea5044c44b4d898ede0ad13ac583c3da56b7dbb61f074f2e139f2dbcec4ff9d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 01 Feb 2022 02:45:06 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 01 Feb 2022 02:45:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.6-signed.msi
# Tue, 01 Feb 2022 02:45:08 GMT
ENV MONGO_DOWNLOAD_SHA256=f6e2bc600b2b8b0251a9e99d84fefc43c66e45deb5793ed8e65cd12a318c76ee
# Tue, 01 Feb 2022 02:48:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 01 Feb 2022 02:48:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Feb 2022 02:48:58 GMT
EXPOSE 27017
# Tue, 01 Feb 2022 02:49:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a0a2f919c7087cda3f02b0076c88126664d1d645989272d5d47aef5252e5a9`  
		Last Modified: Tue, 01 Feb 2022 03:07:06 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb97aa41421c20ac589ab6db5e704ecf70a6396774274b16de01c47047a4b9`  
		Last Modified: Tue, 01 Feb 2022 03:07:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d0ddc2d42e1e998c0d7741b12fa856c79cbb3be002497698ce29204695dbfb`  
		Last Modified: Tue, 01 Feb 2022 03:07:03 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296362ef6e1c2b75c79b8e6f966118b50d380ff94997bb09438027ea0a872bda`  
		Last Modified: Tue, 01 Feb 2022 03:08:07 GMT  
		Size: 303.5 MB (303506008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c635c4a8332e1bc0bbd25888c70b4a983d9b07b556b697101f4947d045883b2`  
		Last Modified: Tue, 01 Feb 2022 03:07:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f13cf5144b93264d939cac118da411eb81b29d298394f0eb7ac27afed0f7ef`  
		Last Modified: Tue, 01 Feb 2022 03:07:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f33ffc4da049a7d02b6c92d039fa1583e8fc868f1a404eae51690caf06317d`  
		Last Modified: Tue, 01 Feb 2022 03:07:03 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
