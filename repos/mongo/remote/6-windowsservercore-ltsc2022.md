## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c257d35e222b2d3407a132d1ca2b033a1992b5a1d168bbc74c8af8674997d8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:4056973ed363c4fc7139e0d3aeb76397164596eca267d61099849e536a324780
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2995066920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c07e57652a9782d664cb537e986d03b202781a96458e930826223be8e12e96`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Wed, 09 Nov 2022 14:41:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 16 Nov 2022 19:15:39 GMT
ENV MONGO_VERSION=6.0.3
# Wed, 16 Nov 2022 19:15:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.3-signed.msi
# Wed, 16 Nov 2022 19:15:41 GMT
ENV MONGO_DOWNLOAD_SHA256=6557ae0360747d348aefdf30d1360f577804c446579c2012e0b04e5ec2489c49
# Wed, 16 Nov 2022 19:18:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 16 Nov 2022 19:18:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 16 Nov 2022 19:18:14 GMT
EXPOSE 27017
# Wed, 16 Nov 2022 19:18:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcc0cd10e58716558145d847bcea390e3840d172df19b8d0f08a57dd985262d`  
		Last Modified: Wed, 09 Nov 2022 19:02:46 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ece0a1889d31de1895fb48f6f37d23fca3a7f73e8b63b6e37ea1a868e7f66d`  
		Last Modified: Wed, 16 Nov 2022 21:18:06 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91609187359c05a5835119c3a1d9f2fff8d4d397e52da17425675df1087983d4`  
		Last Modified: Wed, 16 Nov 2022 21:18:06 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559ae461c4682087af4c74e18ddd8f7274f6b15e4660c44435a82269994377a2`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28c4f5edecc349d7f8990290609bf47befb11c720df04afa49cf40abb1cb5f7`  
		Last Modified: Wed, 16 Nov 2022 21:19:52 GMT  
		Size: 513.3 MB (513288297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34784e2cca2c762ae85677db36f88e17c66ea756c09c19cf6dec5c3de1678b07`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcc4c3a2fc9d68cd21dc03876150493f0d81cc877ffb1fb788da9c1be473a0d`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0caf8a1fc0a90f46855c1e51b85f42551fb4457108fe6bf7df383b6fc2d2fb`  
		Last Modified: Wed, 16 Nov 2022 21:18:04 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
