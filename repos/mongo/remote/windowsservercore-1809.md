## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:e33ee1340178d116377b7c156cc66c16d3042148099805a8cd911595258c7677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull mongo@sha256:b3673afc8d2ac6a3e4cc47f8b56d56175fd85d8e4ecb468a62819bb20bbbf120
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3008359249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85d3f6b2fad62aa880cb15f268e45bc410c542e20dd2f509134cb8618d53514`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Mon, 24 Jan 2022 23:18:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Jan 2022 23:18:12 GMT
ENV MONGO_VERSION=5.0.5
# Mon, 24 Jan 2022 23:18:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.5-signed.msi
# Mon, 24 Jan 2022 23:18:14 GMT
ENV MONGO_DOWNLOAD_SHA256=a791d7197849516381b3dc5b2ebb988432b95b52e347a3ce3d70d026d108886a
# Mon, 24 Jan 2022 23:21:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Jan 2022 23:21:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Jan 2022 23:21:51 GMT
EXPOSE 27017
# Mon, 24 Jan 2022 23:21:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1e63a09e013659f9cb51a44694cf1487fd0ea2ae5528ca387357386508f2b93c`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c48d051dd16471a0816c25274185f26a59275331e3db0a935a4b345e30aa076`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418a5b30b187b4e3b16adcc39b8d3b8d24497158ca115a1357e29a7b230c900e`  
		Last Modified: Tue, 25 Jan 2022 00:07:22 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2271700cb1ae5eb2824a1afd826e2386c1d3b927ec24a41fd0cf159b53f7b69`  
		Last Modified: Tue, 25 Jan 2022 00:07:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe8a27163aa447ec423a9b0afdc4f866a2509b684fa326a0dd9d4bb8f130867`  
		Last Modified: Tue, 25 Jan 2022 00:13:06 GMT  
		Size: 295.0 MB (295027877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e98a3339ea3647335cbbbcfc77e4c26b28e1659595d9b485e6c1a373c2554f`  
		Last Modified: Tue, 25 Jan 2022 00:07:19 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012eab6931802a0d985e4a2187b656996827f015c17569aea5615842da276e3d`  
		Last Modified: Tue, 25 Jan 2022 00:07:19 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14d6dab973c4e39575aba2f6f370a7e55994600418b2f7bec71445e0df969d2`  
		Last Modified: Tue, 25 Jan 2022 00:07:19 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
