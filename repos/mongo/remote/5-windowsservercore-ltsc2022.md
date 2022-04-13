## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:622ddfb2e9ac6277889afba0d5659526610e65a9e5f8afcd6dd5e56d093b3e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.643; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.643; amd64

```console
$ docker pull mongo@sha256:c551917cd7b27ab5d0cac9e87fd504f95ca06ebf2610b6c56e6386060f7499d1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2533895103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac90c1acdfdaba1bb473c3770aaeec1f112740703d2e7198934a6b7b5949c356`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 12:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 17:30:03 GMT
ENV MONGO_VERSION=5.0.7
# Wed, 13 Apr 2022 17:30:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.7-signed.msi
# Wed, 13 Apr 2022 17:30:05 GMT
ENV MONGO_DOWNLOAD_SHA256=3d9eee63d56ff75176cf03308274a29c9e385704e21a26f5864cfe1357ca3cf7
# Wed, 13 Apr 2022 17:31:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 17:31:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:31:31 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:31:32 GMT
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
	-	`sha256:1e8f4da1c3ac9a9cbd52543f5061c6fbc24a8980cd9411d4c625e91284f5b288`  
		Last Modified: Wed, 13 Apr 2022 17:54:38 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98bbc2ba4f98de333dcd6e5061d585a325577094c32c28c1d4ed43033083828`  
		Last Modified: Wed, 13 Apr 2022 17:54:38 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c35fca65cba01d939edbc701a2c58410b94e430bf93350d54c5abfcffc5409`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69d1ed8b2315a6126b58e0d3151aa9ac27ebe1ce7fb5ca243afb444bf5be36f`  
		Last Modified: Wed, 13 Apr 2022 17:59:50 GMT  
		Size: 306.9 MB (306930393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e21e42a9a082d8988a908b45e9b1dedfb7e7d70199a134f3a0c327e068b3f37`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eded7b672fbe2a2927fd581a459e220208a0a649acf8a7ebc9da0878f1895c`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553d324af8f0d9738175edafbdc297be5a0e884bdb80cc169f549247a9ed59a4`  
		Last Modified: Wed, 13 Apr 2022 17:54:35 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
