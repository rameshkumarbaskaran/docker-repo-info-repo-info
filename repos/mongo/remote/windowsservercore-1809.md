## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:0b0d23cf2ee18aea4b2fb97822bb4525e2ec25f9b883bbe2dfc915e0aaa1c4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull mongo@sha256:e2747a08b689a3b97a4d09929a097dbee0f6bca563ff022f104a13142e2c262e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2979520355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579f3eb8ee743f4d6188a27507b0c99918ca88f64701c91ce3e827d6841901ae`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 00:34:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Oct 2021 01:34:40 GMT
ENV MONGO_VERSION=5.0.3
# Thu, 14 Oct 2021 01:34:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.3-signed.msi
# Thu, 14 Oct 2021 01:34:42 GMT
ENV MONGO_DOWNLOAD_SHA256=ed1cc2eee23f4fb9cc7f70867e29d7c9a1e1af1d9b4aa917d247a4921c4ffd7e
# Thu, 14 Oct 2021 01:37:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Oct 2021 01:37:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Oct 2021 01:37:18 GMT
EXPOSE 27017
# Thu, 14 Oct 2021 01:37:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55c74bf8af074a49872e1e0411ac5572625083d17cb1100c5cade611deeb92ff`  
		Last Modified: Wed, 13 Oct 2021 00:43:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b2385e226e317a6557eaceb5c6dc1c367964183df6748248f8af5921c23462`  
		Last Modified: Thu, 14 Oct 2021 02:12:20 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08208875db9c78866fea34cdc6dc4d3963a8dc959f4ec4e00de909d304d47c43`  
		Last Modified: Thu, 14 Oct 2021 02:12:20 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffaedd446f56ec6d6ec35fca8ceed8e8ed372f2cde489271ff057fdd964f54a`  
		Last Modified: Thu, 14 Oct 2021 02:12:18 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d465b78d6d6813f216b6b4d6ab90ef93e13f6b08e8ac5e0832822e32ed53d561`  
		Last Modified: Thu, 14 Oct 2021 02:13:16 GMT  
		Size: 293.2 MB (293191826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571d9235cdda81b5cd4c0793bf5f049574bd1127ad9013174679b2116b4394e`  
		Last Modified: Thu, 14 Oct 2021 02:12:18 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef366eda8992bb91d0b5e1da4d6655e0d78447b8e6c02ad9c2e6d8d909064c4`  
		Last Modified: Thu, 14 Oct 2021 02:12:18 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f9c42f83c400061de870926fd0203a5ad3a1e1b57dbc203c78d25236edb40`  
		Last Modified: Thu, 14 Oct 2021 02:12:18 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
