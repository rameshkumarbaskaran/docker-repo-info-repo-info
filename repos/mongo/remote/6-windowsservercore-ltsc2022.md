## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:df7c0791d0f469b44478f6d2f90c1dede4885e3022b8cfd4e535c7a24a2b7483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:f9c2934c24f81958e6ff8e94f7ebc07614fbe7d46adc015a2ffe09b66a9891fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1942433860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846c5885ea4f61e0da9360c0950e7d571b3ade4ac5d25e80cec445332b94f94`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 02:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 24 Jun 2023 02:41:56 GMT
ENV MONGO_VERSION=6.0.6
# Sat, 24 Jun 2023 02:41:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Sat, 24 Jun 2023 02:41:58 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Sat, 24 Jun 2023 02:43:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:43:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:43:56 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:43:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369acdd1cf7c4d89f87cf3df6c1a935d83dad0afd57c96dcd7251a04481546a0`  
		Last Modified: Sat, 24 Jun 2023 05:25:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5616abab3d9ec61b9b1df568f529e1b8808781676555335fb440cdb2900c39e4`  
		Last Modified: Sat, 24 Jun 2023 06:41:06 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26855da333bfb6c0024c2ecfbdf9ecd4386aedbe614d45df43a3b3e6012934a`  
		Last Modified: Sat, 24 Jun 2023 06:41:06 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078351807daa9e213d7711f44fcfc076a0914ad18b779dc41e684da8c71e62a4`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1d354bf30584043d8664975ab49662239980f869a62a3320bb23af279aef1c`  
		Last Modified: Sat, 24 Jun 2023 06:42:18 GMT  
		Size: 516.1 MB (516125356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353e77fd5dc58f4c913da69987f385306cce1e9180fa1c860e840f450146729`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456f218ea7df8a7cdf57e10f1e780fb24b3c51c9972c7d5bee6feef9eeb8583c`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b22add58e900b33dbeada7c0a536e51370158424492b9f68a28049416d561fb`  
		Last Modified: Sat, 24 Jun 2023 06:41:04 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
