## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d9902a2ba410ee6374ea05c74f3d34aa7bc3f2cd0fd6472e64e9991cdef43b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:fe9103cc75f9f202718d1a09c66e2e79904ac9ccd9de2df2a51c49c20bfa0f22
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896809760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59328c0c0d829441188bb700337779f9d1e6aacb402dc1487262b24196a107bb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:47:17 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 02:28:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 24 Jun 2023 02:55:54 GMT
ENV MONGO_VERSION=4.4.22
# Sat, 24 Jun 2023 02:55:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.22-signed.msi
# Sat, 24 Jun 2023 02:55:56 GMT
ENV MONGO_DOWNLOAD_SHA256=95a021db597790008f2e7070fab4a7c3e0d30262f2305c615b95cb7b8afb4eed
# Sat, 24 Jun 2023 02:57:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 24 Jun 2023 02:57:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:57:23 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:57:24 GMT
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
	-	`sha256:37528efaa97cd491d0c598ce3489dd3c3ae33fcbc2b22736d07d3dcd4cbd86e6`  
		Last Modified: Sat, 24 Jun 2023 06:52:24 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827b73a780fb73a363e3254b51d025b9a0db507d4248f33cedd648ea46ec73e7`  
		Last Modified: Sat, 24 Jun 2023 06:52:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712b1c63094b072181958752d47f8b2d1e2d7adddbd96fe9ee63505c70423ac7`  
		Last Modified: Sat, 24 Jun 2023 06:52:22 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a5f6482f1ee08e518a8981f0693b0a4870ad3607feb7156ef90d79c8fa63ae`  
		Last Modified: Sat, 24 Jun 2023 06:53:06 GMT  
		Size: 246.1 MB (246063105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fb7b65b83dc77ca69f2f937e849f4840224c92b08e52f7cd2fdfde0676ebfc`  
		Last Modified: Sat, 24 Jun 2023 06:52:22 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa49a083152346c742e9048e225d983913f898170611b51e2f48487f199a6c2`  
		Last Modified: Sat, 24 Jun 2023 06:52:22 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df60da52769820c2a05ee909c664de76b3b8a8604961f1410da59fb198d80e9d`  
		Last Modified: Sat, 24 Jun 2023 06:52:22 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
