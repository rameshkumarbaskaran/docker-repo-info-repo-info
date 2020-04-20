## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:a14620e311ff3a231892aeb35aa5b8ec88c6ab01ffda9a0941c4159344f999e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1158; amd64

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
