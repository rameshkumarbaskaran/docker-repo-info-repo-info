## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:a2d0926d8887c48a6751c7021be88d1fa45423e3731807b689ba5dc012a514c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull mongo@sha256:d14f41cc0ffe4e027c8ce3f0592e293d4abd4178a506119d7124958f8903a782
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2076409370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09803dbff2a867e80bf2771f78bef544928d95fd250bb0de1203c03ef45b1448`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Wed, 12 Apr 2023 00:15:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 00:25:37 GMT
ENV MONGO_VERSION=5.0.16
# Wed, 12 Apr 2023 00:25:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.16-signed.msi
# Wed, 12 Apr 2023 00:25:39 GMT
ENV MONGO_DOWNLOAD_SHA256=2319542cffb08c1375d90189ba2eb90dc1a0e28bb88989af79c3a661bf1c499a
# Wed, 12 Apr 2023 00:27:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Apr 2023 00:27:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:27:17 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:27:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3664aee9b0b3199a388e1a7d17e99ada617d122d6a2572b0c40140fdea31a3`  
		Last Modified: Wed, 12 Apr 2023 05:57:17 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff280eda58baab9301b21c05c9b425dead06b679aaf92aa13d5f1a97dd441f8`  
		Last Modified: Wed, 12 Apr 2023 07:27:32 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb0a01e3a56a507badf6c5d2d21b748ed5a1657e3aa84a86583b01db826f064`  
		Last Modified: Wed, 12 Apr 2023 07:27:32 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a845cff211c27a57bc41ffb5e9e76cef4d2825951831004aa8a43b0d3b9fb11`  
		Last Modified: Wed, 12 Apr 2023 07:27:30 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e196ce47a143e27131fdd851c62b4dca1eaffbc7442b36ad8f4d882cbbc5cb`  
		Last Modified: Wed, 12 Apr 2023 07:28:27 GMT  
		Size: 313.8 MB (313797400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e3e0bd3108f92fecd12ec16df87b371d62f68f27169806bffbc446624ea34c`  
		Last Modified: Wed, 12 Apr 2023 07:27:30 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9727b04ca1166b0dd6e6fbbc2a04b8ee703ba10447d6320e82ec2c351afb6ea7`  
		Last Modified: Wed, 12 Apr 2023 07:27:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c61caf1ea51e6fff66f36f25630252f9aa2f2740b5cf6bce449067a5a40212`  
		Last Modified: Wed, 12 Apr 2023 07:27:30 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
