## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:f50351e91123a76d636525f587874b77e2b55b8ade680cf8444453b440c52a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull mongo@sha256:1cb1b18208d508154add1608056a1a4546ae301c7d994de856b22e4657b1aaf8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479878766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afea52b7f966738ece844c76a9d1ef9d89341c0d8dcdd97fec682ac1bdbe9f4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Thu, 09 Dec 2021 02:15:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 09 Dec 2021 02:15:02 GMT
ENV MONGO_VERSION=5.0.5
# Thu, 09 Dec 2021 02:15:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.5-signed.msi
# Thu, 09 Dec 2021 02:15:04 GMT
ENV MONGO_DOWNLOAD_SHA256=a791d7197849516381b3dc5b2ebb988432b95b52e347a3ce3d70d026d108886a
# Thu, 09 Dec 2021 02:17:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 09 Dec 2021 02:17:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 09 Dec 2021 02:17:35 GMT
EXPOSE 27017
# Thu, 09 Dec 2021 02:17:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ac50d042e82656322dbab3f037f6b059dd9bc2c3f1f3d5b8b47a3a22630e539`  
		Last Modified: Thu, 09 Dec 2021 03:18:55 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2acf076ecffdd1be5063fda64c5fcb40fde5d36553e04cae12a707596648f7b`  
		Last Modified: Thu, 09 Dec 2021 03:18:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00aa03e3612ae28acfe686e0181e045be178abdbe329c4e83bb3d3f366c46bcf`  
		Last Modified: Thu, 09 Dec 2021 03:18:54 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea643e46800a0e67d021d25f82327d15f9c180b06fdc0cc7f8c750a50da51dd`  
		Last Modified: Thu, 09 Dec 2021 03:18:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c906bbe511e04cac036ced6677943acec005842dc5116125e3660d22b029daf1`  
		Last Modified: Thu, 09 Dec 2021 03:23:57 GMT  
		Size: 295.3 MB (295261877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e1722dc6ab288fccc019f130b110aa71b87041cdc67aee36d6eb45a5efb099`  
		Last Modified: Thu, 09 Dec 2021 03:18:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861fa4bf1a1ddb5b3cdb94c83b89f937735beb8fe89ba7576a0a375e45013cfc`  
		Last Modified: Thu, 09 Dec 2021 03:18:52 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f3fa7c47e44b62e45fbcbf0a2d24b2ad4e1db879677907c07d4388b3afeff7`  
		Last Modified: Thu, 09 Dec 2021 03:18:52 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
