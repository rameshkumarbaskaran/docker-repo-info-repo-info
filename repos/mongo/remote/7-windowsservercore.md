## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:813450a1ded60f3fa72bafb4bc3d78feee5852084f0020875e5a61375d9bb0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:012558ced1778bd01eda56d8975dae28d6e4661e526093273fe6d81737c1b1c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93feb6c8f7d523deb6f4933fae77cbee4476b628f906eea11051331ddc3d19a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Thu, 10 Aug 2023 01:08:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 06 Sep 2023 00:34:03 GMT
ENV MONGO_VERSION=7.0.1
# Wed, 06 Sep 2023 00:34:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.1-signed.msi
# Wed, 06 Sep 2023 00:34:05 GMT
ENV MONGO_DOWNLOAD_SHA256=bcdcdc445e53106f6c596304061529c055cda6f23cc06fe8adcc7f7c41c64d99
# Wed, 06 Sep 2023 00:36:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 06 Sep 2023 00:36:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 06 Sep 2023 00:36:32 GMT
EXPOSE 27017
# Wed, 06 Sep 2023 00:36:33 GMT
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
	-	`sha256:2a492f7d879bd0dc842d771fa6b8ab3999a2836a22112d14589217f5966f77ef`  
		Last Modified: Wed, 06 Sep 2023 00:54:28 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f028ea16c84ee61e565e5c729913f3da1051b13bbc635382dff457d145bf04f`  
		Last Modified: Wed, 06 Sep 2023 00:54:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b011ef0f211d12690abc26ebff1460d17536b93dbe0560e93f076f7a36d571e4`  
		Last Modified: Wed, 06 Sep 2023 00:54:26 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef447b9da2de5d405b825532f4a20bf6f23560c525e2a1625ed8db3eb5cbeba`  
		Last Modified: Wed, 06 Sep 2023 00:55:56 GMT  
		Size: 612.8 MB (612751499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63184375658946c56b5b709242b302b0e77fe3c15055d947ecf4cd3ae69122`  
		Last Modified: Wed, 06 Sep 2023 00:54:26 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b670a0e6b4bab883395e84058a7b4b8807d88783f1da4bc0fb354247770d12`  
		Last Modified: Wed, 06 Sep 2023 00:54:26 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92351fae5b6a700bd62a7b501f2ebb0f1e301b4291218f5c4a8a441129a21e3b`  
		Last Modified: Wed, 06 Sep 2023 00:54:26 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:7c814ca598effcf13d97346868422dbc6a25df32b620c0c5daba47c601cd98c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2608774985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072b9d4a695470aa03dd0e268971861f0c54e5d6413cb3e60f31b39238276161`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Thu, 10 Aug 2023 01:11:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 06 Sep 2023 00:36:46 GMT
ENV MONGO_VERSION=7.0.1
# Wed, 06 Sep 2023 00:36:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.1-signed.msi
# Wed, 06 Sep 2023 00:36:48 GMT
ENV MONGO_DOWNLOAD_SHA256=bcdcdc445e53106f6c596304061529c055cda6f23cc06fe8adcc7f7c41c64d99
# Wed, 06 Sep 2023 00:40:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 06 Sep 2023 00:40:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 06 Sep 2023 00:40:23 GMT
EXPOSE 27017
# Wed, 06 Sep 2023 00:40:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5180b8f5f7c2303ba89717cfa778a2173921ca7efdc058cfd6ed951c6d5ca3`  
		Last Modified: Thu, 10 Aug 2023 01:57:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6ade7345cd37ef77061503d8931877ba649f0377161817f3662627ec28524a`  
		Last Modified: Wed, 06 Sep 2023 00:56:13 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70d878bd5f7d394f317ff85507b322108d6aa2002d5ca795eaa9790c3854a13`  
		Last Modified: Wed, 06 Sep 2023 00:56:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683636b446c2ab58c38a6acb5b4bdf831c0d00960ebc881c0ac6ed3fa455adf1`  
		Last Modified: Wed, 06 Sep 2023 00:56:11 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf4d8fabcdc924a3dca827a96683b04637966a03d991d500d0cd29aa75cf8a`  
		Last Modified: Wed, 06 Sep 2023 00:57:45 GMT  
		Size: 612.8 MB (612809759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98756d14ef40ea4a68a3a2018666413fc3096a33af5706bdcf515504afc08bfc`  
		Last Modified: Wed, 06 Sep 2023 00:56:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dab1d09de9b00f014f0800202bc5121818837523bb322faa4ab0b7a615e661`  
		Last Modified: Wed, 06 Sep 2023 00:56:11 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357b31248c8dac4f2b2d13f09875f5535789b6fcd3fcf4bc8a121acec5c4a01e`  
		Last Modified: Wed, 06 Sep 2023 00:56:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
