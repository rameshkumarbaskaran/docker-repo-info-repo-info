## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:29ca3bea646a83d01e3e25e0046a5c18fe594e2ee511c7dc50a489e282582d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
