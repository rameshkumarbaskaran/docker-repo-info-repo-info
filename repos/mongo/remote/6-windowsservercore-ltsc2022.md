## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:110cab1ba167116aebe14206156dc8db098b8dbbe4c1c41b53e573e4016a968a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull mongo@sha256:e18817b52e0972d4d2aea9f6b4bd050035ca33899e4ff3bd218b49e657699442
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2314973953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04be902de62e1ee906176c8138193f8b9659d97e87d68cdbaae1d567ed0077d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Thu, 10 Aug 2023 01:08:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 01:24:32 GMT
ENV MONGO_VERSION=6.0.8
# Thu, 10 Aug 2023 01:24:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.8-signed.msi
# Thu, 10 Aug 2023 01:24:34 GMT
ENV MONGO_DOWNLOAD_SHA256=06ee15df933f9f76757084c4b226eb06f79ad1471b293d9343484a6bc84e11eb
# Thu, 10 Aug 2023 01:26:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 01:26:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:26:30 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:26:31 GMT
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
	-	`sha256:4b0e0d8911068efc5db16251a7ff33e714540022dec887ba084fda40ce19cd91`  
		Last Modified: Thu, 10 Aug 2023 02:07:58 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4328cc4a81d3be0d7c25420297a9d2781cd25949377448ac721a03bda69e022`  
		Last Modified: Thu, 10 Aug 2023 02:07:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa2a8ad0deec059bfd3cc86a918e1d0c6f2ede30539ec5e6bb26326a7c8ddef`  
		Last Modified: Thu, 10 Aug 2023 02:07:56 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ac2c3603eb451b58c0361717ea104127f03afa6a9d1374b76e5bec2f4c1f4e`  
		Last Modified: Thu, 10 Aug 2023 02:09:12 GMT  
		Size: 517.6 MB (517600158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf7a367221b5f8a5f927f60a38e6f4ebc5664483fb20d834e1c81b272e4d28e`  
		Last Modified: Thu, 10 Aug 2023 02:07:56 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1fc0b470e70a1de627d2bf8a27db8e5f5ba2c3266738f2fdabed8e7bf4d305`  
		Last Modified: Thu, 10 Aug 2023 02:07:56 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e09b3b9e9c8e4cbf06c17772943c312f313aac713e3bbfb18018b48a094921`  
		Last Modified: Thu, 10 Aug 2023 02:07:56 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
