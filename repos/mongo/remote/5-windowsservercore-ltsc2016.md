## `mongo:5-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:60f78f0b566a4e64b7e23b325ac8c533d8dbdd78a21cdf01c56496e814382a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `mongo:5-windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull mongo@sha256:b67a198b2b0a08dce57873b457c011e55d8058d8260488e7e0c276029e26e780
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6564408574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b26df23c222d16647045cb3d79985c18ad2b8dfbc014a2885eb9ebacea216`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 Jul 2021 22:18:48 GMT
ENV MONGO_VERSION=5.0.1
# Thu, 22 Jul 2021 22:18:51 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.1-signed.msi
# Thu, 22 Jul 2021 22:18:53 GMT
ENV MONGO_DOWNLOAD_SHA256=c0476ee7f9c28547fa60db24fe44ef61fa9c18b0951d9b2ce99727a69b254244
# Thu, 22 Jul 2021 22:22:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 22 Jul 2021 22:22:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 22 Jul 2021 22:22:12 GMT
EXPOSE 27017
# Thu, 22 Jul 2021 22:22:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b0dd1e685128a4f306d8b641f920031316432abc3fd963c00bc1e583c68982`  
		Last Modified: Thu, 22 Jul 2021 22:27:28 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c647aefb6262461a140f17b4b95f3c6d21c6594012ce2093e7db39ebb3becf`  
		Last Modified: Thu, 22 Jul 2021 22:27:28 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae6699eb45256548509e871c67a239ba8fdb5de1de1981a692a87a523566bf5b`  
		Last Modified: Thu, 22 Jul 2021 22:27:26 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6d75d62666d72ca2ca8933bab2d3e4cffc3bb538bea05d9a555c3b64745cd4`  
		Last Modified: Thu, 22 Jul 2021 22:28:20 GMT  
		Size: 294.8 MB (294766909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcc0da8a37107edf565b16c768e26a649550b31cbcd31336fe95d1fd7632980`  
		Last Modified: Thu, 22 Jul 2021 22:27:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1060f6477d49856b5a8c6c192ef62845188b106c0cfc0394889ef563fef50fd6`  
		Last Modified: Thu, 22 Jul 2021 22:27:25 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2a14eb59f1ad591b8faa4844429d0fc5067253f4685cf118c4f0b3a4c7130f`  
		Last Modified: Thu, 22 Jul 2021 22:27:25 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
