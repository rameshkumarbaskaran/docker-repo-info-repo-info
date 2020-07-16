## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:05a334cc34d584668c6ec7b5d38a63c3d93e670e4dc59807d4d822705d40d7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3808; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3808; amd64

```console
$ docker pull mongo@sha256:16b2447316d53cd5236246d57bb91a33c05b4d2b26c564c84123a6149d2abc35
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5831030715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb57a1541fba3249da08b64a291672b5b90ddff06228b4c36c159d04a6f8f85`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Jul 2020 21:05:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Jul 2020 12:24:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jul 2020 16:11:34 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 15 Jul 2020 16:11:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 15 Jul 2020 16:11:35 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 15 Jul 2020 16:25:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jul 2020 16:25:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jul 2020 16:25:23 GMT
EXPOSE 27017
# Wed, 15 Jul 2020 16:25:24 GMT
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
	-	`sha256:9fd8daf6ced592ebbb1f3bdd46dffbae65454d6f40f3090dae6bb01615d2c742`  
		Last Modified: Wed, 15 Jul 2020 18:23:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ad4ae9b1028038586d8efe0c63a7d09199f67a47c039fcbf5a19891a23654`  
		Last Modified: Wed, 15 Jul 2020 18:23:32 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db3484a811b8bc81c661b43389dfd857641d07c157f5e875884f7151a908b92`  
		Last Modified: Wed, 15 Jul 2020 18:23:30 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb574ada0a2f25713005c9546f76680f96672221b3f5ab6317e6d10811c54f2d`  
		Last Modified: Wed, 15 Jul 2020 18:23:50 GMT  
		Size: 93.6 MB (93560647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec7596bd09552af536f7173900eded30c4f60ed26bed62d010550b977f78cf7`  
		Last Modified: Wed, 15 Jul 2020 18:23:30 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6445eee1e3992f481011f0b05451a38102cf592835f3011e3f2577c8abd7ee05`  
		Last Modified: Wed, 15 Jul 2020 18:23:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d968dde3cd279d33700c077e1702b7b37254d269b6cdfdc300e2adef36656a`  
		Last Modified: Wed, 15 Jul 2020 18:23:30 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
