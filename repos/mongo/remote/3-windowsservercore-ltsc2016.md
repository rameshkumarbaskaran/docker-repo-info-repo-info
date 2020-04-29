## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:1c041ecefccd929dd54691dc1bb1c302fd9920aacecb63f26d8ea8ec2fc83c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:bb7f637eb4e591cb7451ce57983470a1b5c70da0f02ddaebc184984c31e921ce
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183931146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50ce0ea0d77fa23432496130c213beccceaee5cb8f3073fb22ce9e26d1ce2d5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Apr 2020 17:31:25 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 29 Apr 2020 17:31:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 29 Apr 2020 17:31:27 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 29 Apr 2020 17:47:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Apr 2020 17:47:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Apr 2020 17:47:57 GMT
EXPOSE 27017
# Wed, 29 Apr 2020 17:47:58 GMT
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
	-	`sha256:617eb631432c8da59417956e59fa89dd9499287bb1e03a57242771d87b134fff`  
		Last Modified: Wed, 29 Apr 2020 18:04:39 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48015d36dfae02f45da1718c72ec7194820de15474bb77b30c0fefadc57f76b3`  
		Last Modified: Wed, 29 Apr 2020 18:04:39 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca9bf120c5c0dd2f76889a932591cdc8dc9e50e0c3dc970b56f488fad7251e3`  
		Last Modified: Wed, 29 Apr 2020 18:04:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205639b7adc30f1271385cc1e100b49085241ed06b0853342285a65c607ce98`  
		Last Modified: Wed, 29 Apr 2020 18:05:44 GMT  
		Size: 455.9 MB (455855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c287078686d900479f28ccfab01cde3a23a8e340c204208747b2675ceec9a4a`  
		Last Modified: Wed, 29 Apr 2020 18:04:36 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfe54729a98b104e02e0db211f932317d90d16a60e7c96134388d4abf2aff3f`  
		Last Modified: Wed, 29 Apr 2020 18:04:36 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5482588ddeda18c03bc1734f18e3ad57df444c95c2ad5fb8f8a2378a13a356`  
		Last Modified: Wed, 29 Apr 2020 18:04:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
