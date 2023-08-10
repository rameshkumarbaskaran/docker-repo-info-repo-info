## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:a2979793cf16c4d8eb68184136033a4b5db198a00d9a94301096a94723434401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:32dd026e25b4877109a6de39f90dbdc3001112efb7790170cad25f31910dbe5a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2043471496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189a5b34a6158d35457e3be520da43167a240e737c63c0162552197c9ae2319e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Thu, 10 Aug 2023 01:08:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 01:48:19 GMT
ENV MONGO_VERSION=4.4.23
# Thu, 10 Aug 2023 01:48:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.23-signed.msi
# Thu, 10 Aug 2023 01:48:20 GMT
ENV MONGO_DOWNLOAD_SHA256=cc0c9055c5a8cb43bb51c14d5447f358be717f63ebd9b9774ef923289170393a
# Thu, 10 Aug 2023 01:49:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 01:49:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:49:28 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:49:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b1b41cab0d4b78c8daa50728be89bc3c25ded051cc1e654b316623692507f1`  
		Last Modified: Thu, 10 Aug 2023 01:55:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db88da0ebd4767a511eca37bca6779a43467cf2a22e750bb2648e31b668293ff`  
		Last Modified: Thu, 10 Aug 2023 02:26:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024d22c375b89fd426abb6ec70bfc5945da51c767a98d68c8fd3bcd8f9dcc964`  
		Last Modified: Thu, 10 Aug 2023 02:26:20 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74b7fc3e35084611e0e2fdbea0bdc35e89affa87e03f0db1a3ad35a9a6d4797`  
		Last Modified: Thu, 10 Aug 2023 02:26:18 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651dd55a1f52fcf424979cda203f088a36311d7c38dde71f9d334d7ab4d99395`  
		Last Modified: Thu, 10 Aug 2023 02:27:02 GMT  
		Size: 246.1 MB (246098284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35defe5d30a4f1eb817a165327994f1994bf6e5baa3b5ea40c7e75ff1cb00130`  
		Last Modified: Thu, 10 Aug 2023 02:26:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3801682c7e74de4d80fc1ac8f6a19e08d31ce2f99f13d9eee27d0823b46f82`  
		Last Modified: Thu, 10 Aug 2023 02:26:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526526d6293bd56f51f0f641464a25ff2deeedf1cb24d9b83291eadb6ade10a3`  
		Last Modified: Thu, 10 Aug 2023 02:26:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
