## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:1c12e3c303540d84962b5b6fc704be34532344c8c7d789aec776ff43c5500f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1547; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.1547; amd64

```console
$ docker pull mongo@sha256:30be6975d41f91dbe9856096da191631e7bb5a894b01cc4a81929e1d6f34f26d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195137654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9244d902a40c20dbc00742cd2e00dc4ef5bd4138767468fe8bde9b9cd319d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Tue, 07 Feb 2023 11:42:22 GMT
RUN Install update 10.0.20348.1547
# Thu, 16 Feb 2023 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Mar 2023 22:16:14 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 15 Mar 2023 22:16:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.5-signed.msi
# Wed, 15 Mar 2023 22:16:16 GMT
ENV MONGO_DOWNLOAD_SHA256=79327a9901a39182dee2d74f84e46b4c6b1416cfc2c0cee791322ea82dce0388
# Wed, 15 Mar 2023 22:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Mar 2023 22:19:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Mar 2023 22:19:10 GMT
EXPOSE 27017
# Wed, 15 Mar 2023 22:19:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d015a9e7adea898d81486dce8b513b0e9cbeca30904cac18c3ea98ab3be7a6`  
		Last Modified: Thu, 16 Feb 2023 00:28:01 GMT  
		Size: 293.3 MB (293317272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028996d5eeb6d70e4f35b4acb3bafeee3f326bb40438911de597cad432ffdbc1`  
		Last Modified: Thu, 16 Feb 2023 01:35:55 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a776a5ed620f5017bde919327ec721b916b860446c26f8ab9145f49fb6dc61d`  
		Last Modified: Wed, 15 Mar 2023 22:29:23 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9e810e7f0364a0f1200d429b5089ad7e5064bcdda9af646ffa4ae886f21e6`  
		Last Modified: Wed, 15 Mar 2023 22:29:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab39713a0010193bf8abe7216e974dfa4e6e67fb55ca559a567137f6161363b`  
		Last Modified: Wed, 15 Mar 2023 22:29:21 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0346af830a408ecded70ecb5018194cd0e598c4b38fc5161226e6adf2bdb40b7`  
		Last Modified: Wed, 15 Mar 2023 22:30:51 GMT  
		Size: 515.8 MB (515781450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab10e26bbaa1663f2ecf92ce933f0668902f366cf168e05cf8b486ae5f24944`  
		Last Modified: Wed, 15 Mar 2023 22:29:21 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c467e65a71b17714e76b4e450efe28406ad31702a53b14a697ef40d8497f40`  
		Last Modified: Wed, 15 Mar 2023 22:29:21 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4215b2c31b9b9c32e536bc809859c0b3a7035c15086fe1cedd6a0a07d77caafd`  
		Last Modified: Wed, 15 Mar 2023 22:29:21 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
