## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:82b75adf88c5ca9cea130c0abe8fe8509c42672eb0e29f40a9d9deca0bc66e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:89c7627968ebaf770c685f715874b046b5f1432fc2ac50e1274406e2e6c7803e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2513634607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9bf185f1a1e67d3370f666c884078e9b90458dd97f073a3651b5d8d43cb613`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Thu, 10 Aug 2023 01:11:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Aug 2023 01:26:45 GMT
ENV MONGO_VERSION=6.0.8
# Thu, 10 Aug 2023 01:26:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.8-signed.msi
# Thu, 10 Aug 2023 01:26:46 GMT
ENV MONGO_DOWNLOAD_SHA256=06ee15df933f9f76757084c4b226eb06f79ad1471b293d9343484a6bc84e11eb
# Thu, 10 Aug 2023 01:29:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 01:29:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Aug 2023 01:29:33 GMT
EXPOSE 27017
# Thu, 10 Aug 2023 01:29:34 GMT
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
	-	`sha256:9c2f1ad1a9aa01ccd818373952a4142f58c7a132b43bc3d528134eff33361f1f`  
		Last Modified: Thu, 10 Aug 2023 02:09:30 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acea3187cf31fd8ea32a0a12a3d37c3631b4f5155ddc0c4ffc2bf24314bce194`  
		Last Modified: Thu, 10 Aug 2023 02:09:30 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7122df860c903e197d936a5b7c73e100a673f75d4528a26ff1ad6eb6709cde2b`  
		Last Modified: Thu, 10 Aug 2023 02:09:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79382d1d00e598eb07b04abb89d1520fa3fb313d1f7be5d118a09563acca890`  
		Last Modified: Thu, 10 Aug 2023 02:10:47 GMT  
		Size: 517.7 MB (517669704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fc6c7adb87806cc18c5236495d6a852e4a063b59e9c4eabc4f95f7986e34cf`  
		Last Modified: Thu, 10 Aug 2023 02:09:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7997ad6bbb30e391dd830aea4efe48c46c0073d62479ec7a6a60f4cb905c00`  
		Last Modified: Thu, 10 Aug 2023 02:09:28 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecec8464f33068d7627491d59c5ada95a0d76a9b0a497dfd2462ffb2f773249`  
		Last Modified: Thu, 10 Aug 2023 02:09:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
