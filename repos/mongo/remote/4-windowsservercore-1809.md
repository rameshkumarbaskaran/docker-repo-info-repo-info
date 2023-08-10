## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:79de9012fba2109a26e8530bdf05ae696889ba9274fdaf17eaa1ad4c933b7c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:125968fabf7c9b78f08ad682f16fac404f1ca603f3658dff54712eafe71f0f45
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242102838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53383492d64e7e5b05f8b395afc46fee49573c52aba136b1146a34fe4443504b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Thu, 10 Aug 2023 01:11:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 01:49:47 GMT
ENV MONGO_VERSION=4.4.23
# Thu, 10 Aug 2023 01:49:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.23-signed.msi
# Thu, 10 Aug 2023 01:49:48 GMT
ENV MONGO_DOWNLOAD_SHA256=cc0c9055c5a8cb43bb51c14d5447f358be717f63ebd9b9774ef923289170393a
# Thu, 10 Aug 2023 01:52:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 01:52:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:52:08 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:52:09 GMT
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
	-	`sha256:6ee4ad53a2524bc233ff5074bbbe4d6515b6d6dc90c4414df3c2a2ea65802a74`  
		Last Modified: Thu, 10 Aug 2023 02:27:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d817f9bf0404a4b420034b10bd862e088ec70d965d1dca55df402f756d3044`  
		Last Modified: Thu, 10 Aug 2023 02:27:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d827f1c95ba23a5585bbd325fdec7867e9dd20b341ba2258f1fcbcefdbf7fe09`  
		Last Modified: Thu, 10 Aug 2023 02:27:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04227c8bfb3b72bb03622f066f6533f3c974d8c97f83f4eb64b9d41ab7a53e57`  
		Last Modified: Thu, 10 Aug 2023 02:27:57 GMT  
		Size: 246.1 MB (246138272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df55d7ab0b68ff6f282e11a0d83d546cbbc39e7794aebe3c73a087d8700135b`  
		Last Modified: Thu, 10 Aug 2023 02:27:14 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f053d79933f58dc4cce56e628ac8a4fe5ec54c3b8368ccd25906bde8f0e44647`  
		Last Modified: Thu, 10 Aug 2023 02:27:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc01e4a66562811953a2f1f357eb0b0d9a10f601aeeed7c426ffed0f5e754845`  
		Last Modified: Thu, 10 Aug 2023 02:27:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
