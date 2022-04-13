## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:d21babd6d0b071a7361469abf9ac731d2d9498f0554e54462103c5f84effb9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `mongo:4-windowsservercore` - windows version 10.0.20348.643; amd64

```console
$ docker pull mongo@sha256:7e25d485adb1eec3fc5a6ee85cd63e14f252ce059eb143b17bc8141558b4de45
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2469905145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00466b4e8e7490bdfe3d351743a806f05d7cd6a1157d8553a532c3f69e700757`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 12:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 17:36:30 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 13 Apr 2022 17:36:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.13-signed.msi
# Wed, 13 Apr 2022 17:36:32 GMT
ENV MONGO_DOWNLOAD_SHA256=0eb6e5c43c74a992301529515c52b7e326239cd12649fb6f91e807fcbbf06f39
# Wed, 13 Apr 2022 17:37:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 17:37:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:37:59 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:38:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2a5d28823cc7f2a78cb6b52a2cadb350e978705d7634adbcfbc4bd80d4637c2`  
		Last Modified: Wed, 13 Apr 2022 14:11:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88f4816091580c70a2e7d956f552d7046d7315b8d055eae6afe97d076626dd`  
		Last Modified: Wed, 13 Apr 2022 18:12:39 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf75ee62601c04ba8418e070482647ed7f1053db8bc6a22c9ad32aff56f86e9`  
		Last Modified: Wed, 13 Apr 2022 18:12:39 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b902054b60fc8d4a07bbbd9c8afcea225b1f78b34d0aade7dea945f82c9301b`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f2bbf5932c9d7944fe75ce8cae1f7b1bdb07db3acc38bb4cb9b9652282372e`  
		Last Modified: Wed, 13 Apr 2022 18:16:53 GMT  
		Size: 242.9 MB (242940409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202910162eb1f0313fa93e562bb2ca41aac77416b173b3ae8e5abb051ca1fc16`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38a45180fa43fab88ad9ef517b812132c8178f8f7d118cdc2554b485f75c9b`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86221664f145c9d5df593a0eddab4f09cac704aeb90533a026b500df44f6890`  
		Last Modified: Wed, 13 Apr 2022 18:12:37 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull mongo@sha256:1c225c87adeb87ce65f47d7719e49fae6a5221acdfc495f2d59dfa0f4818bd25
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2958643170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba93fab337cd6bced2dba6cbdecfeb5d09c0389008f3630efa555b05a1ceb9a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 17:38:11 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 13 Apr 2022 17:38:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.13-signed.msi
# Wed, 13 Apr 2022 17:38:13 GMT
ENV MONGO_DOWNLOAD_SHA256=0eb6e5c43c74a992301529515c52b7e326239cd12649fb6f91e807fcbbf06f39
# Wed, 13 Apr 2022 17:40:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 17:40:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:40:15 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:40:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8402025757fbbb34a33341e710285af59eec30317bbdc7e0447de44a5cbbd9`  
		Last Modified: Wed, 13 Apr 2022 18:17:10 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb7be8e1f3a6bf2935158a4ab36ed9a3151b94eb900994b2d749c5cfb73b74`  
		Last Modified: Wed, 13 Apr 2022 18:17:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc0bbba573b29f34722f8359dd80cb0baba380fbc923cc7507b98af0f1e89fa`  
		Last Modified: Wed, 13 Apr 2022 18:17:07 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36417e74845291ca0d668f572c540ac8a4d5237e58438d8b2da226a108d1051b`  
		Last Modified: Wed, 13 Apr 2022 18:21:52 GMT  
		Size: 242.7 MB (242712957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2278b80580e9f5c3c431c6ad4758fbd978e6546419606b1b7944038096afc9c`  
		Last Modified: Wed, 13 Apr 2022 18:17:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35da5067dc022610cb910dad1187f1d8240eacfac237d79c39908a2c2678c6e7`  
		Last Modified: Wed, 13 Apr 2022 18:17:07 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f6c016f081bf50d38722aa3dc2d74c8e02156afd255229efe48fb0443e492e`  
		Last Modified: Wed, 13 Apr 2022 18:17:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
