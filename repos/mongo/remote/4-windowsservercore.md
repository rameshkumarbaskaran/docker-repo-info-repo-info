## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:054da40353496c22bf25509f395f9e30e42f7801558686cd4e86289194e54bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `mongo:4-windowsservercore` - windows version 10.0.20348.473; amd64

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

### `mongo:4-windowsservercore` - windows version 10.0.17763.2458; amd64

```console
$ docker pull mongo@sha256:712dbd5333953d5b74debe8d19041c3fc431ef7ef6c7dcbca4f1751779bc48a0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2955476979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da63b9e9622f36596a1ed63b229f8f079d0cb32572585719c0a2918f3be80501`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Jan 2022 23:29:20 GMT
ENV MONGO_VERSION=4.4.12
# Mon, 24 Jan 2022 23:29:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.12-signed.msi
# Mon, 24 Jan 2022 23:29:23 GMT
ENV MONGO_DOWNLOAD_SHA256=a46ddabb46813c509555bdb012e34f0aadd12b5348a23ad7206fc18ac5a2fcd0
# Mon, 24 Jan 2022 23:32:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Jan 2022 23:32:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Jan 2022 23:32:24 GMT
EXPOSE 27017
# Mon, 24 Jan 2022 23:32:25 GMT
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
	-	`sha256:1f8fc59dea26dcd79aa9300b96d09191806232095228475e2be55d0d8e8b973c`  
		Last Modified: Tue, 25 Jan 2022 00:30:41 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14a91f132b86ff33b416730da108f8a7d2c5c5d6215bd15dfa058bbf1d86cd9`  
		Last Modified: Tue, 25 Jan 2022 00:30:41 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b8ce51b6e31176c522fc2281f166a46a22db919f7ba76bc60a52efe684b1c6`  
		Last Modified: Tue, 25 Jan 2022 00:30:39 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1997681adf8987cd085d157496e356f49d96ca71f52c9d3023972bf4ef89d154`  
		Last Modified: Tue, 25 Jan 2022 00:31:25 GMT  
		Size: 242.1 MB (242145525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802de83baf8a5c9322c59a80a53d38649f0f0750c5be3579d1e1401cb6500926`  
		Last Modified: Tue, 25 Jan 2022 00:30:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350533b670c8790eb9fc52c31301e3290100faedb8e569ec899b3ec1e267af08`  
		Last Modified: Tue, 25 Jan 2022 00:30:38 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923c6cc339d00b7ce7af1d007ab4df5dd5cc597f700f8afdfea1800236e84e3`  
		Last Modified: Tue, 25 Jan 2022 00:30:38 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
