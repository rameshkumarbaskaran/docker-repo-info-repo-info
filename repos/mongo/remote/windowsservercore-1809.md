## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:281ab52fb2a57db81fd7000c8965b9c0f11a51fadee6e18c9b4e1955c903137a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull mongo@sha256:864e9d191cc7398fc1599e3b134c6e10a1af8338a06efb98e22bf509e42b56a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2586866179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325c4e5499aabb460e2e1f3524c6e6bc3624d2cbca8ac01d4b9aafb671843d8d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 00:18:39 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 12 Apr 2023 00:18:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.5-signed.msi
# Wed, 12 Apr 2023 00:18:41 GMT
ENV MONGO_DOWNLOAD_SHA256=79327a9901a39182dee2d74f84e46b4c6b1416cfc2c0cee791322ea82dce0388
# Wed, 12 Apr 2023 00:21:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Apr 2023 00:21:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:21:52 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:21:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ae6da7d6748862e5d09551159383d071c1f6f7fe426ee2189596832e33516`  
		Last Modified: Wed, 12 Apr 2023 07:22:54 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2f95871bd19e5289f93313f73bca29f203baaae9fdb86477a3eb76a1af02e3`  
		Last Modified: Wed, 12 Apr 2023 07:22:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cb5d7e7da55ccd8a8a3e3461bc022f04d9465cd97ae0b078f8eefde8da3aae`  
		Last Modified: Wed, 12 Apr 2023 07:22:51 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ce92797fa498d867595dfcb8cd3937c081eff0654b11a61e05a6c0b75a7e12`  
		Last Modified: Wed, 12 Apr 2023 07:24:11 GMT  
		Size: 515.6 MB (515565032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af8840f6d7fe126cc81bb2872058d38f1799e328c38b5aee6e60d83230c7ce7`  
		Last Modified: Wed, 12 Apr 2023 07:22:51 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579edc7e43d06a72e098bd1c14f42924e622481a0bfaaf10d3e61804eb8d00a5`  
		Last Modified: Wed, 12 Apr 2023 07:22:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58df637564b33be067e9629ff9df76ae5ac28126fc41fb37d244c46a15a61cd`  
		Last Modified: Wed, 12 Apr 2023 07:22:51 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
