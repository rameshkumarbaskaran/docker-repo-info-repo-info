## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:73e0085caeca324c06ba2f8b48256c4571862a0da2bde9f76356117294f543d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:622c67051745f0690da415286db5b36221418445bb093afe55db4da2d0a7b2ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111384903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9209327599aebb5af316022e6ee8fc7723ec62824487fa7b82a7796df4bc285e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Thu, 10 Aug 2023 01:08:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 01:37:47 GMT
ENV MONGO_VERSION=5.0.19
# Thu, 10 Aug 2023 01:37:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.19-signed.msi
# Thu, 10 Aug 2023 01:37:48 GMT
ENV MONGO_DOWNLOAD_SHA256=85c99b0b7ddeded924cb937d48fcd1b14c7c43b35c39fbd4d6961d6940f4b538
# Thu, 10 Aug 2023 01:39:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 01:39:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:39:09 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:39:10 GMT
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
	-	`sha256:b8cdfc52c20855423271692de232edfe066b74d5f7f13a4e6cfbfedeb1b3739c`  
		Last Modified: Thu, 10 Aug 2023 02:18:26 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cecd203700de8d74a4ab744bd08d3b9ce3299dd839cc8d50b2ee288916541d7`  
		Last Modified: Thu, 10 Aug 2023 02:18:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72eebd26bfc4f92ca412fd49aa6e59d094355916a408ca6ec0caa39f867c2b48`  
		Last Modified: Thu, 10 Aug 2023 02:18:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1273a13c4c610a300e93444c4747aa8aa635dc63a177004eeb5d5e6b34b8341f`  
		Last Modified: Thu, 10 Aug 2023 02:19:18 GMT  
		Size: 314.0 MB (314011627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34627b28841fb5a049b0ff4de89267d6396b16aeff41811c5984f6d5dda8bbb1`  
		Last Modified: Thu, 10 Aug 2023 02:18:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd0a580edbd21a44e8fe5a3efd51dd2488271f8d98491f2a485e1725fcae73e`  
		Last Modified: Thu, 10 Aug 2023 02:18:23 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0768f956b0761162c632e985665462e3595992185a9cded6ad9da5d5c4daf3c`  
		Last Modified: Thu, 10 Aug 2023 02:18:23 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
