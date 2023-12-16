## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:6f8ba2ef24c40cab86ba07aabb893b1644285b85180e7bbc7e60e975435d59a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:e32c169ac2d53e3b30788ff1268835bf1f35a18f03be5bf0ed9e415a67cf8a55
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2501438557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4532ec38a3673738279ad3f6dfbb605d1a77e0bd8c1d6ba87de5364f9356eb9d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Fri, 15 Dec 2023 22:50:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 15 Dec 2023 22:50:43 GMT
ENV MONGO_VERSION=7.0.4
# Fri, 15 Dec 2023 22:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.4-signed.msi
# Fri, 15 Dec 2023 22:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=86a9ce6ce62c9b6a3fee8739572419b59040fa25c7e07a4d1ce28894670e2a2b
# Fri, 15 Dec 2023 22:51:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 15 Dec 2023 22:51:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 Dec 2023 22:52:00 GMT
EXPOSE 27017
# Fri, 15 Dec 2023 22:52:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d4de95f7e930ee96818ea29e14089ab199182e14448b729ffe6e065c15a9de`  
		Last Modified: Fri, 15 Dec 2023 22:52:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a695c5207d9f79958e35b670c43efdf747cfef124f7e8ed20efa62a0c1bcf44`  
		Last Modified: Fri, 15 Dec 2023 22:52:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554528749a1762637d9d020de52885a61e4c4f7a188059c29ae6cc8e78c3caf0`  
		Last Modified: Fri, 15 Dec 2023 22:52:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2edea773d9cf9deb42c2cb3d71fbc9cd5c07f62b95fc0d2b59eea2bcc06c7e`  
		Last Modified: Fri, 15 Dec 2023 22:52:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ab0278fd0757dcdf12ba49fc88279c09947716060579cf66eff590dca0ee9`  
		Last Modified: Fri, 15 Dec 2023 22:52:58 GMT  
		Size: 612.2 MB (612155903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd88f5c8438c5ad203aea20efccde2f04649fa1938ff5902699d38b6a11bf93`  
		Last Modified: Fri, 15 Dec 2023 22:52:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da15cc0a6a63b65d77f003632523803535a0570981f3cf4abecbe9d543364f9d`  
		Last Modified: Fri, 15 Dec 2023 22:52:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31f5125a8289bffa07e42aadfe9d0beeeed3ebce484f6f9eb27d4293b7ecb79`  
		Last Modified: Fri, 15 Dec 2023 22:52:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:4693309422274c117c5f4cb772bebfdb659938f97b3bfcc2e8a63cb46b6a3e78
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2671841316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5193f29ccea91ec6681f8be8613a368605e998bf843b088a6ad39509fb3ac8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Fri, 15 Dec 2023 22:16:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 15 Dec 2023 22:16:12 GMT
ENV MONGO_VERSION=7.0.4
# Fri, 15 Dec 2023 22:16:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.4-signed.msi
# Fri, 15 Dec 2023 22:16:13 GMT
ENV MONGO_DOWNLOAD_SHA256=86a9ce6ce62c9b6a3fee8739572419b59040fa25c7e07a4d1ce28894670e2a2b
# Fri, 15 Dec 2023 22:18:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 15 Dec 2023 22:18:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 Dec 2023 22:18:19 GMT
EXPOSE 27017
# Fri, 15 Dec 2023 22:18:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3743769affa9f6000eef4287a52250fc420d80acc4116558347cf762f6ff89`  
		Last Modified: Fri, 15 Dec 2023 22:18:24 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f6bd2a58ef0d458960c601ea019f847f7f0e5239e38ef17bcb4b82696965b4`  
		Last Modified: Fri, 15 Dec 2023 22:18:24 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983225a8bdf022a3892b463a21b58ae0660d68a34f14a1b2ab8b9ea64759a30`  
		Last Modified: Fri, 15 Dec 2023 22:18:24 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb38b3951182812b58cafe999ff41bc9e1c607df62e898a2ef73973b16f5d1be`  
		Last Modified: Fri, 15 Dec 2023 22:18:23 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a26e2322bf7ddaa9c4b20b05c80302d14023495069f590c9b3502f608bdc8c8`  
		Last Modified: Fri, 15 Dec 2023 22:19:16 GMT  
		Size: 612.1 MB (612122693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78daf21d1b77ae44dd1b5525e33a9c246dfc1396523c54c4725f80406b7de65`  
		Last Modified: Fri, 15 Dec 2023 22:18:23 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec1eb096b25fc3013f5af866be7e3c26828169f42197d08f60b78a93e6d2469`  
		Last Modified: Fri, 15 Dec 2023 22:18:23 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b50cd2eae76507352d0dc0046a4580f40c8223f8f63879f76cad32ab2c68c0`  
		Last Modified: Fri, 15 Dec 2023 22:18:23 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
