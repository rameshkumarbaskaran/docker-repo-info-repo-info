## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:ff58ef6f07de1f251dbccead1949f582e75519bfd18b82cd6dd03f46f53784e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64
	-	windows version 10.0.17763.1339; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:e378006e45e49f266b38af941f1c35b49f16f0241ab2700f9b06f6a0cee63d7d
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6196396127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a6f08795360aa1f59022178a8fcd071881a88a76caf19400af577189aeb467`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:10:59 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:11:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:11:01 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:29:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:29:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:29:37 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:29:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:802c4beb8b091968ccf1bb4a853ded7955ddb79e6f8775a5155cb5ed07dcbcab`  
		Size: 1.7 GB (1667476199 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3393eecaf56a66035ab178b379bacf81d30373b630b34b2973501f259aadb0f6`  
		Last Modified: Wed, 15 Jul 2020 14:32:38 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3dfe0de5cab41c554134849cf768de5c5dc8e13bddcf1ad0fc806b09b09d9`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c61e46b189dea42061aaad9e57cc266bac76e45d084c7c5dbb4297275420d4`  
		Last Modified: Wed, 15 Jul 2020 18:25:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d3c72aca4ce3e1adac36ace31ec90c5136bdb62d68e7df1c995930d7675d3`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dee039fb33fb8009e470967c7f2cf4c736eb740d2b0983a30bae8346e90ea`  
		Last Modified: Wed, 15 Jul 2020 18:26:40 GMT  
		Size: 458.9 MB (458926051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8b55963ce51d78169778f3087da2e01a1676f02722a908557d54928ad92bb8`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34948740dadb9eda10312ccff609b4ee18103654693c22a3f1ffea495f84c7fd`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb880ce8b0f816ef69983d906d0f53ef557cfa76d87920425de41cd8de97ab1c`  
		Last Modified: Wed, 15 Jul 2020 18:25:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull mongo@sha256:3ef879eae3b96926458d249bc739bf61396cd74670ac8914a259ec7e147b8cfc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406176795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdefe5b04b221a1444aad3cc8ad9bd9f6738fd52aef638821add68f900afeffb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Wed, 15 Jul 2020 12:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 17:29:47 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 15 Jul 2020 17:29:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 15 Jul 2020 17:29:49 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 15 Jul 2020 17:45:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 17:45:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 17:45:14 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 17:45:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1cc883a0e3509a474bb32f3c40411bf86219325ae9710e25a5dcce6b44eef357`  
		Last Modified: Wed, 15 Jul 2020 14:32:06 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d87922616041a21a2c523968d7ead4551e32f674e2706918dff806ff719b9e`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e086d89859d6e7aff940ac1b087eaadabe091bf93e43757c70923fa4b65834b1`  
		Last Modified: Wed, 15 Jul 2020 18:26:59 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c34a6281d2c7a72f4123d137a924c221dc35f5f5b76b3bf2f6fb7d61cf4ba60`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f539c8a8292df269f2f6ca500c34f7b2a25b96805f841dea8f0ab7b8f7d9cb`  
		Last Modified: Wed, 15 Jul 2020 18:27:17 GMT  
		Size: 96.0 MB (95976559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707d8b6fd30a84d3b12f4998e64302f7f1234fa3fcf5c713a8013a3463de914d`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9581635ab009c29efefd72e8d20ce852c94a715a623b5152c0f816eac7b083b3`  
		Last Modified: Wed, 15 Jul 2020 18:26:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584c85cdcb3e27d0d74dfcb2b1a509ee9a9f2462e30f30fa7f3508705a10d30`  
		Last Modified: Wed, 15 Jul 2020 18:26:57 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
