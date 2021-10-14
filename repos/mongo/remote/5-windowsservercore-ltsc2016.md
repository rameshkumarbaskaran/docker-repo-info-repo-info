## `mongo:5-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:5dc5c786041bd35a6549d06d21fac363ab4c4477995b979c7243221b69689358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4704; amd64

### `mongo:5-windowsservercore-ltsc2016` - windows version 10.0.14393.4704; amd64

```console
$ docker pull mongo@sha256:5aa1e501fdf40a5b943041a7c76b98e5eb36453475d222f22d2f7ecb7c68040a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6570428452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa652834c2451f4d3fdfeef337e698fccc2a69bed8550c93fa12d4769f726d2b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 06 Oct 2021 21:16:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Oct 2021 00:39:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Oct 2021 01:37:38 GMT
ENV MONGO_VERSION=5.0.3
# Thu, 14 Oct 2021 01:37:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.3-signed.msi
# Thu, 14 Oct 2021 01:37:40 GMT
ENV MONGO_DOWNLOAD_SHA256=ed1cc2eee23f4fb9cc7f70867e29d7c9a1e1af1d9b4aa917d247a4921c4ffd7e
# Thu, 14 Oct 2021 01:40:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Oct 2021 01:40:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Oct 2021 01:40:08 GMT
EXPOSE 27017
# Thu, 14 Oct 2021 01:40:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0c776a8e8e3c02d360995b7fa26a3fd7c0928965795fac57b69ff07418ab07bf`  
		Size: 2.2 GB (2202780626 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d3c52a3fe41298469bd9ca8471cd22a349f75bf82b049e968c97dd7cbf538b9`  
		Last Modified: Wed, 13 Oct 2021 00:44:16 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026fa80ac8ef8a7f950cb3273ddbdfea355144ec3e61cecc6b41eefcbbdcf02c`  
		Last Modified: Thu, 14 Oct 2021 02:13:33 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02845091172815e9e6943dfa2c88c656ad80313fb7efb0da2ef810eec120aeac`  
		Last Modified: Thu, 14 Oct 2021 02:13:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2b50335afc1b22c1071610521067d3372df20bf6d29dd1caf9abd8251ac67a`  
		Last Modified: Thu, 14 Oct 2021 02:13:31 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb2e5dc23b57a70c519fae7e3501305a9c9af6f2e454c7197634835eae46327`  
		Last Modified: Thu, 14 Oct 2021 02:19:01 GMT  
		Size: 297.7 MB (297652044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9a4a355fd7a90856553ea198dc91afe423683f53e764a04fe792646249be02`  
		Last Modified: Thu, 14 Oct 2021 02:13:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d1efcb2961b1f99dee8b381f05dce8d1a18733bf7148227277c74e4a582946`  
		Last Modified: Thu, 14 Oct 2021 02:13:31 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4978e2dae55b23d4f58b6f36a52b8f5e82f0d2975c8b7fe370e425ba3e196977`  
		Last Modified: Thu, 14 Oct 2021 02:13:31 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
