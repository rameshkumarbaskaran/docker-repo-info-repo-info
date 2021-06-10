## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:2b59aa4314ce6c20d927c198de339152510b0dc18acb28e17fe4e8088dcd1e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull mongo@sha256:b01b78e78ff15717c569d71b13f27bad07e0a54b9f22b7d338992aab78a52095
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6501876232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbf1160505acb0d2b0e89f9a079acda8bbcbedd1ce856ce14483d8e4e73a49f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 13:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Jun 2021 20:40:35 GMT
ENV MONGO_VERSION=4.4.6
# Wed, 09 Jun 2021 20:40:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.6-signed.msi
# Wed, 09 Jun 2021 20:40:39 GMT
ENV MONGO_DOWNLOAD_SHA256=ede50e8f8d8c9d23a8ca2cc1c96cdb9bcc1f617930e8bd1d46f21d95d0b555f8
# Wed, 09 Jun 2021 20:43:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Jun 2021 20:43:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Jun 2021 20:43:44 GMT
EXPOSE 27017
# Wed, 09 Jun 2021 20:43:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fa4e6085e5538e957ef06561fe1e62dff898da7f4bb577e81da74323aecab2d7`  
		Last Modified: Wed, 09 Jun 2021 15:28:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6562d39fa84cb30abdaf8ba85c49633fe3dbbbb574b420d3d6f0b6dcd84612c`  
		Last Modified: Wed, 09 Jun 2021 21:06:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632dffa8911cfd4ce0e581711217246f0acb2c9aa23c00d1665325ca9d01474d`  
		Last Modified: Wed, 09 Jun 2021 21:06:20 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d1a10881159fec53a734a20335f669c66ec8fad205ff18837714b08a2e57eb`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fea5282878f8bceeabdfa4eee9a3b15fa82046d07b73acc8bede72ed373e6eb`  
		Last Modified: Wed, 09 Jun 2021 21:10:53 GMT  
		Size: 236.1 MB (236139160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37d1edadef24c3d2d47473839335006c5e263b365ed3421f7da2ac8cf8d87db`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11529cee90aaa262ba14cbf27ff16a20766bacb7c7c673522446ebf8ae34b949`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c741f47ea5e251f30ac58630bf0c9d48dd7a1cc68e6394f1ad1c5dfe0aed50ed`  
		Last Modified: Wed, 09 Jun 2021 21:06:18 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
