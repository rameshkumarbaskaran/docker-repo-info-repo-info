## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d991135219490ba111e0a082d4a694e97c3975db58f322ba03a57faab2e0a6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:6df2928d2292698aa55e12ac14666f40cc6b76a1008bb6bc11bf827300b6a9c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1964318656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78f99030e6e9ae192242de6beea42e70e2f415f627b451a76b3a368788fdeb5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 02:28:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 24 Jun 2023 02:50:27 GMT
ENV MONGO_VERSION=5.0.18
# Sat, 24 Jun 2023 02:50:28 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.18-signed.msi
# Sat, 24 Jun 2023 02:50:28 GMT
ENV MONGO_DOWNLOAD_SHA256=369e0cdc34c29290bfcc9d47569e1debad1b86010ea5e00aefd7c670717f434b
# Sat, 24 Jun 2023 02:52:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:52:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:52:06 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:52:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b1471cc22404d036d95728a9c37c1e3f025a1f0a331072c8613e38cf8f7ff1ed`  
		Last Modified: Fri, 23 Jun 2023 02:36:08 GMT  
		Size: 1.7 GB (1650736778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9634b679e6c602a6aaf0bae51625e7ca041489c77150db557640304f51bb37`  
		Last Modified: Sat, 24 Jun 2023 03:01:43 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec30a8834ea5626679038bd00aef7bb3190f9c80ce2457ada4c079de789e27c6`  
		Last Modified: Sat, 24 Jun 2023 06:48:16 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b3b27fb53664dfecebc0a1953dda63476b6abc688a7b6b8746f2f179053be`  
		Last Modified: Sat, 24 Jun 2023 06:48:16 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5389550370e867778e8b9f69341c1016fb3489dbdaa3f39c092e6236eac970`  
		Last Modified: Sat, 24 Jun 2023 06:48:14 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e85fcdfeadc08a7a509da8c1e1077799caa6f1ed5edee99aa0025963db4c9f`  
		Last Modified: Sat, 24 Jun 2023 06:49:08 GMT  
		Size: 313.6 MB (313571930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5dd2a042f612bbbe9c5584f487ba33ba4a43546d09d743ce5e757865f847fa`  
		Last Modified: Sat, 24 Jun 2023 06:48:14 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5124d43b1d2b65fdf583d4f15eb64a9b42aed205ba7e3ea24dc0647a2ac057ac`  
		Last Modified: Sat, 24 Jun 2023 06:48:14 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4bef276911a9221d5834823e930800c053a49c73edab330075325f20f06344`  
		Last Modified: Sat, 24 Jun 2023 06:48:14 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
