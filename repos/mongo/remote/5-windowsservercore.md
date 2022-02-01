## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:e4b4246f148945f12d03463f277439635a104a882624a697cdd452c9349451aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.473; amd64

```console
$ docker pull mongo@sha256:5ec9968eb933a0c9386886302800704578daf5dc103d607d663e11463527ab9e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2511198105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6fb7f7170f8a8a5f9e033e5ecb02bf94a2ad8cbc32a0fb099b9a015a552ce6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Mon, 24 Jan 2022 23:14:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 01 Feb 2022 02:41:53 GMT
ENV MONGO_VERSION=5.0.6
# Tue, 01 Feb 2022 02:41:54 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.6-signed.msi
# Tue, 01 Feb 2022 02:41:55 GMT
ENV MONGO_DOWNLOAD_SHA256=f6e2bc600b2b8b0251a9e99d84fefc43c66e45deb5793ed8e65cd12a318c76ee
# Tue, 01 Feb 2022 02:44:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 01 Feb 2022 02:44:46 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 01 Feb 2022 02:44:48 GMT
EXPOSE 27017
# Tue, 01 Feb 2022 02:44:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8c23346c84162bdf06f85b57d55396916bb13e6a631f65a1e6ee317bfe8a7f8a`  
		Last Modified: Tue, 25 Jan 2022 00:06:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b1482f10078d77a35deab202065dfa70935f75fe39211a8573d263f5bc5d6c`  
		Last Modified: Tue, 01 Feb 2022 03:05:42 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29ec28f052fb0f323216a2c6e75880b961321f77ed8e8aeaaf46bcd0bc2a401`  
		Last Modified: Tue, 01 Feb 2022 03:05:42 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96620a66f28e1b752bd6a4c307c5c39a5c34286609387c973d4387f52a6e8ba1`  
		Last Modified: Tue, 01 Feb 2022 03:05:39 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cead1a99d36711c3850312afcb45da37861a1087ee66308d084c332631e9b555`  
		Last Modified: Tue, 01 Feb 2022 03:06:47 GMT  
		Size: 303.7 MB (303688343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab4a3fe8e947565d72acddf92c4df88316d19bec34066a51aa83c69a4ad8a46`  
		Last Modified: Tue, 01 Feb 2022 03:05:39 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cad8d986697f0e2765d76f6d06e854ad0445dc43c3117ee93b05bcf2fe89b45`  
		Last Modified: Tue, 01 Feb 2022 03:05:39 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198646ccb0cac81d264dcffc47c3d059f7baf482d78d86d0201677a362342529`  
		Last Modified: Tue, 01 Feb 2022 03:05:39 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.2458; amd64

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
