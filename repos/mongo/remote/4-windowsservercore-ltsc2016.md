## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:5178545dbe86fb2495b61af75feb648d0b3b36b670a0f714cb2e14e47b62d2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4283; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.4283; amd64

```console
$ docker pull mongo@sha256:b1d9775d7d5f80d2d0b22618ddc7388c511c21622d58b41de953aae71e307780
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6038355370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde3668b909d674f994001d3fc27c77141c8374e1cd54bbc2021212b48fefea0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 14:25:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 08 Apr 2021 19:18:13 GMT
ENV MONGO_VERSION=4.4.5
# Thu, 08 Apr 2021 19:18:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.5-signed.msi
# Thu, 08 Apr 2021 19:18:15 GMT
ENV MONGO_DOWNLOAD_SHA256=1ef4f41cfaf3b91dc34543186b0b02ea2756075f4df822180b1fb46602604fd6
# Thu, 08 Apr 2021 19:21:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=ServerNoService,Client,Router,MiscellaneousTools' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 08 Apr 2021 19:21:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 08 Apr 2021 19:21:12 GMT
EXPOSE 27017
# Thu, 08 Apr 2021 19:21:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5205e01a19ce3835a7f1caba14b71dbbcae05a77274c60358d9794ee0e2a3e65`  
		Last Modified: Wed, 10 Mar 2021 16:23:35 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa4e11364998da972964e67c94beeee43be3a7088613e19dead49070dd3bfc4`  
		Last Modified: Thu, 08 Apr 2021 19:27:30 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3452caacb1f048c352a58cdffd2d9058bfcd61a4b75c4b293923a51a42e6a9`  
		Last Modified: Thu, 08 Apr 2021 19:27:30 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074c879b23990ce21cef6e9ad82de20e430fe8aad5dbd60f3230cc6c261b76fb`  
		Last Modified: Thu, 08 Apr 2021 19:27:27 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dbea578da467e77e96388eb9db8649df817ddaa05136cee6e674f914a7be59`  
		Last Modified: Thu, 08 Apr 2021 19:28:14 GMT  
		Size: 241.4 MB (241434953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eff97b9a6f604792d176680e92a9a2ac828556d5c63e44157a679cefcae8940`  
		Last Modified: Thu, 08 Apr 2021 19:27:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33634c8bc969a1e26e02bcbc9edbc929f7edcdfd4987ce552d01e65466b1d607`  
		Last Modified: Thu, 08 Apr 2021 19:27:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90120f89f9457a7d3733f50e06bc1886fe14c59153272c9dcd299ece852d22da`  
		Last Modified: Thu, 08 Apr 2021 19:27:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
