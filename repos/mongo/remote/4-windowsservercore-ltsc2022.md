## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:3b3afaad222606ca9ba182df110df2558ec93b030312ca3a08f043a6d9e340a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:2b3f1edff447e065f8cb94aeb37d424683fb16835278b310fd96fc5189045ca3
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2134878920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6eaf52dd76d5792359dc4fda3a19e99fd4b8365e4f63ce535e6ad4b2fff366`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Fri, 15 Dec 2023 22:54:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 15 Dec 2023 22:54:32 GMT
ENV MONGO_VERSION=4.4.26
# Fri, 15 Dec 2023 22:54:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.26-signed.msi
# Fri, 15 Dec 2023 22:54:33 GMT
ENV MONGO_DOWNLOAD_SHA256=9ba4bc737c4ed037b9ae59d13917a3dcfe4a63035213614bf1fccda0c3f6fbdf
# Fri, 15 Dec 2023 22:55:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 15 Dec 2023 22:55:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 Dec 2023 22:55:23 GMT
EXPOSE 27017
# Fri, 15 Dec 2023 22:55:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf7ae00299fd8377216c746c233521a9d89a7ad07ac62e32c7bb5f542de588c`  
		Last Modified: Fri, 15 Dec 2023 22:55:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f7c6a0a7cf55f6f38f548f85d791d0d5d25f8e66e8a0b8238fcd1dd2d98fe`  
		Last Modified: Fri, 15 Dec 2023 22:55:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a629ea4057ff06d724908bd63f77844b18a3e9a942ee1659e11ef33f1637fe`  
		Last Modified: Fri, 15 Dec 2023 22:55:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978c307fbd2508a48f0d096c87579f553eab47758de1463ce0a3055fc6e755a0`  
		Last Modified: Fri, 15 Dec 2023 22:55:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0672d1f0cc453c57ea88ca45f8da476fd1ce7023a4c292865eff7ce7029e4`  
		Last Modified: Fri, 15 Dec 2023 22:55:55 GMT  
		Size: 245.6 MB (245596253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a5cfc5e9f158f230fcb94b14039543a7c5c1648c71c34178aae11a07af74f`  
		Last Modified: Fri, 15 Dec 2023 22:55:29 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ec944fb4966552a8e2a633600d03285c0372708aff39f449e69e4b35227d8e`  
		Last Modified: Fri, 15 Dec 2023 22:55:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995554cd6fefd4a97a7eb97558b1ac216dc101945c59dd7f6772858da3665195`  
		Last Modified: Fri, 15 Dec 2023 22:55:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
