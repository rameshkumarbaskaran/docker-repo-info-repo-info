## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:91345b65920ee6bf2a3c076645d25ebd78007ad4f9797640415ecd9e5e426385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:19881629aedf11ff58a0cedd43d625be1940bc0621cb77e698723e67d8ea320c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242188230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bead239544df70b4b8cdfe0982de418cf1562d41679951e49214ddde3b791e8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Thu, 10 Aug 2023 01:11:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 24 Aug 2023 00:26:55 GMT
ENV MONGO_VERSION=4.4.24
# Thu, 24 Aug 2023 00:26:56 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.24-signed.msi
# Thu, 24 Aug 2023 00:26:57 GMT
ENV MONGO_DOWNLOAD_SHA256=9f9b32cb6e34d2fa0e2843526c7192eac5a07b28f1300455aeb988e33bf9a714
# Thu, 24 Aug 2023 00:28:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 24 Aug 2023 00:28:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 24 Aug 2023 00:28:56 GMT
EXPOSE 27017
# Thu, 24 Aug 2023 00:28:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5180b8f5f7c2303ba89717cfa778a2173921ca7efdc058cfd6ed951c6d5ca3`  
		Last Modified: Thu, 10 Aug 2023 01:57:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82e82c3086e8609c7f48973a7922a3439a701f0ac1a1b3c401078ca2a1f8b72`  
		Last Modified: Thu, 24 Aug 2023 00:40:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36e37a01c8391ed4fd9796376cd3a2808bd2a9cfc93b4752763dcbcc4b5caec`  
		Last Modified: Thu, 24 Aug 2023 00:40:07 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e49265fa8106f34ca467ad39493b88b530fd8dbc271619db795b153d26f6b6e`  
		Last Modified: Thu, 24 Aug 2023 00:40:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1650174062182f8e13c914e12292322bbc2e280ecfa16612d023ab2ac47f79a`  
		Last Modified: Thu, 24 Aug 2023 00:40:48 GMT  
		Size: 246.2 MB (246223657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df7c2ca425a5cda9ea4cf5965e0bf10a81022acaaa53339c69f6ef991bffddc`  
		Last Modified: Thu, 24 Aug 2023 00:40:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370581b8cb8bdb34438de0ca11070290c25a1f1de9bd8f1ecd56e78912868944`  
		Last Modified: Thu, 24 Aug 2023 00:40:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178871f555316aa4218dcdeb7e77bdc4a55145f28d749ce9e1cc069053d213ca`  
		Last Modified: Thu, 24 Aug 2023 00:40:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
