## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:6309d9d1a205111087624a15e0901ee5c7de8aa374bddec2db927d15948d7121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull mongo@sha256:4604cd0ce5f2481d6797828f41dc02620f76ad6335e673c90548f32212e38140
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2449875870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4a5c4f0d9b2079494ca962cc325f98bc90e35c8d752383c131ee3bdce144fb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Mon, 24 Jan 2022 23:14:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Jan 2022 23:26:38 GMT
ENV MONGO_VERSION=4.4.12
# Mon, 24 Jan 2022 23:26:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.12-signed.msi
# Mon, 24 Jan 2022 23:26:40 GMT
ENV MONGO_DOWNLOAD_SHA256=a46ddabb46813c509555bdb012e34f0aadd12b5348a23ad7206fc18ac5a2fcd0
# Mon, 24 Jan 2022 23:28:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Jan 2022 23:28:59 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Jan 2022 23:29:01 GMT
EXPOSE 27017
# Mon, 24 Jan 2022 23:29:03 GMT
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
	-	`sha256:64158832b8c1ff2a9e5a1eb35c9fa725e1f51e4cbd5fd7eda21834742c784e36`  
		Last Modified: Tue, 25 Jan 2022 00:25:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278043201d45fb21f8712f1bfd78d9b0765254f5e38061d369cc1c49d8cb932f`  
		Last Modified: Tue, 25 Jan 2022 00:25:44 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fcb0153dc5b5382f3834e83b39738f1bfa3a73fe1f5c3a37a776a3f049c246`  
		Last Modified: Tue, 25 Jan 2022 00:25:41 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4f0142a531080d3cdd361b20a567e22b32ff1d924d1a50b764de7f45da8f99`  
		Last Modified: Tue, 25 Jan 2022 00:30:24 GMT  
		Size: 242.4 MB (242366157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d6b4e5a8e8c5ce0640af0c2ef9e27dba5e17c76c7c72f772e2f9083a28d5b6`  
		Last Modified: Tue, 25 Jan 2022 00:25:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da0b5622544ad540b4a32b0969d57bddb5762b5f48617a35378ab3142cf9eb2`  
		Last Modified: Tue, 25 Jan 2022 00:25:41 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f202201c5a55d0f398c7a144cd0ecb268a9e385f777e58c58f5ed9ab92759`  
		Last Modified: Tue, 25 Jan 2022 00:25:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
