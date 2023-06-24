## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:26ccd24ac40272f5e951f271070f1c750f51ecb0f1c1b492d95b5ab11b6203b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:48e29412a1c1543459aacaa534986a080c3fa1d1f501226d7534d45ee7f291fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166885517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719cce80785572bcd4a78ace717429e7f6dd9894b9e539303316813e53910183`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 02:28:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 24 Jun 2023 02:44:10 GMT
ENV MONGO_VERSION=6.0.6
# Sat, 24 Jun 2023 02:44:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Sat, 24 Jun 2023 02:44:11 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Sat, 24 Jun 2023 02:46:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:46:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:46:19 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:46:20 GMT
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
	-	`sha256:1c04e4c66f0c316991c767cd8487be1bb833ecf0dd8279b4b8948d35d9843944`  
		Last Modified: Sat, 24 Jun 2023 06:42:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5f68f9c3242e0657f0fbf3db30792de8615254c08280dcfa455f81a824be36`  
		Last Modified: Sat, 24 Jun 2023 06:42:34 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebbaad2c5797ad4eadd71cbb3941fd5cac755880687b8ba639394508e9cd0ac`  
		Last Modified: Sat, 24 Jun 2023 06:42:33 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1a97bcdadd53b96a0f2559bb23b822d66cf6a04fab66d8ff1e768c53c923c2`  
		Last Modified: Sat, 24 Jun 2023 06:43:49 GMT  
		Size: 516.1 MB (516139075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1886fa5089512d8d071df8e085375c686307f3f09e3e91c0e538b53c6c94d1`  
		Last Modified: Sat, 24 Jun 2023 06:42:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80eb6181dade42d5056178a8e4c4ce0694c7bbb545ab7997b4f8ace7dd76ef0`  
		Last Modified: Sat, 24 Jun 2023 06:42:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bd3182693c9af3ad026603416d9859c81cc6f8cc4b575d851ee96bd7e5cc01`  
		Last Modified: Sat, 24 Jun 2023 06:42:32 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
