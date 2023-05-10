## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:86459df090cc0b96a5254d7aa14a966f3690d986b2ffc481462f6043d4e864ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:c78ec9b420d5ea9a3c9fa9b24c185a4b9b823f45e8e4c6b38faadb93dc162782
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2290455758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a3dedc65f02d67eba8013aa0d0eabce4752830e23241dc4ab2b40be0967eec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 01:53:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 01:53:48 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 10 May 2023 01:53:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.5-signed.msi
# Wed, 10 May 2023 01:53:49 GMT
ENV MONGO_DOWNLOAD_SHA256=79327a9901a39182dee2d74f84e46b4c6b1416cfc2c0cee791322ea82dce0388
# Wed, 10 May 2023 01:56:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:56:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 May 2023 01:56:12 GMT
EXPOSE 27017
# Wed, 10 May 2023 01:56:12 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae2b2372db6d2d1ac04a5297e71fc9a798a078f7d1a0bcccae77193e8b58b2`  
		Last Modified: Wed, 10 May 2023 02:22:13 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d8a5310741ea68484152379f8a7db78235d02e0bda545aeedea5c7da2aba0f`  
		Last Modified: Wed, 10 May 2023 02:22:13 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8e416a78891cc23d12b7d8642a5da790f8dffa8905279754a636b2ee775139`  
		Last Modified: Wed, 10 May 2023 02:22:13 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147a51bbbf8dd6f7a3966d5630af4daf8d8461dd8375566277d8fb21d246aef`  
		Last Modified: Wed, 10 May 2023 02:22:12 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895dbc047d08011adc7797e31b49ff4dfb3c9b978563b254600b197b95217733`  
		Last Modified: Wed, 10 May 2023 02:23:21 GMT  
		Size: 515.5 MB (515464412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c3db7f25cb9062a8ed0af7a72f9b4451f8f2d30ad6d9f1d27fcec13363be79`  
		Last Modified: Wed, 10 May 2023 02:22:12 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22de57bda76613e4a378d0dcb755fad43b44ee530fdf59ab6ff1f6a4d0b87ad0`  
		Last Modified: Wed, 10 May 2023 02:22:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ebdc9bd1cbedc6e8a1aa538f0a364cb222b6873470258aa07c43d606aa610a`  
		Last Modified: Wed, 10 May 2023 02:22:12 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
