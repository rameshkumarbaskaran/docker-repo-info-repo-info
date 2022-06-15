## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:051633d62987825556ba1761f1f0bde71e0668dd2ac9a5f9d76f0024a38fc0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull mongo@sha256:9c663b8c43bfae4c8847b43a9e51d8261e579ef9d52711beb6c2140df89a977f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2905870000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db92f5535b381375377c66eef9c2d94579a328a822e45f6c00cd0b6a638c9d0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 14:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jun 2022 21:12:16 GMT
ENV MONGO_VERSION=4.4.14
# Wed, 15 Jun 2022 21:12:17 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.14-signed.msi
# Wed, 15 Jun 2022 21:12:18 GMT
ENV MONGO_DOWNLOAD_SHA256=beb8d11bbf2c02142fe774cac16752281a8f0a61788d684a495337e288c63501
# Wed, 15 Jun 2022 21:14:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jun 2022 21:14:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jun 2022 21:14:36 GMT
EXPOSE 27017
# Wed, 15 Jun 2022 21:14:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:14def1e29581c5e5d0af7fdf9ff44ed6536e79561eb0f0cdff89e322fb87c423`  
		Last Modified: Wed, 15 Jun 2022 16:18:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb86d14b8b02e53a2525cc179220f063e3ebc3227f7e6af756e509ffe0cdf17`  
		Last Modified: Wed, 15 Jun 2022 21:59:57 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0572232550bd53d3c82090ace5c1fbe83463cdfcb0d0c409a99fc65140221948`  
		Last Modified: Wed, 15 Jun 2022 21:59:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3304c7962a68403c50c9d9f4704287e81ad82ef2252ca29630464e904828ad2`  
		Last Modified: Wed, 15 Jun 2022 21:59:55 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd59a1536a6954bd61ad472c9c77b0dbad059dc2bd2165b872eec741df4f9f20`  
		Last Modified: Wed, 15 Jun 2022 22:00:42 GMT  
		Size: 242.6 MB (242580136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e336f7308846e8d2bcc33da294b71c492f6f874acc6de4e3f81b67db4ad1e8ec`  
		Last Modified: Wed, 15 Jun 2022 21:59:55 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f12e4917cd523c8a742ca516e5be09692d5f493972c4c213b34d82c55753983`  
		Last Modified: Wed, 15 Jun 2022 21:59:55 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e6164f8ee6667ccbe7849af102b2c849a3f47e152bad01c74922f235ab2931`  
		Last Modified: Wed, 15 Jun 2022 21:59:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
