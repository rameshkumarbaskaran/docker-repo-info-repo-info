## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:3faf713e5c7fc32e27859e1cad4b8a3ebaceb1827a32f1e6e76451fc6f2abdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull mongo@sha256:1e1b651813f94379a4316613fe77fe28fdc846da5c5c45aee65d3e919b1fe07a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2970448499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001dcc170f3d92d18de8e2b2a6bab235c10629cac7e2a7062e33e54004f956b8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 14:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Jun 2022 21:04:49 GMT
ENV MONGO_VERSION=5.0.9
# Wed, 15 Jun 2022 21:04:50 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.9-signed.msi
# Wed, 15 Jun 2022 21:04:51 GMT
ENV MONGO_DOWNLOAD_SHA256=0e8032c352253173e9d1683ac7b39c79a4eaed0682e8c0655ca0b3ebd6b11d74
# Wed, 15 Jun 2022 21:07:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Jun 2022 21:07:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jun 2022 21:07:16 GMT
EXPOSE 27017
# Wed, 15 Jun 2022 21:07:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:14def1e29581c5e5d0af7fdf9ff44ed6536e79561eb0f0cdff89e322fb87c423`  
		Last Modified: Wed, 15 Jun 2022 16:18:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc9ca475d8722699c1ef7ca986dd6b071385c494c894ab1bc3cb247cc9d0bbc`  
		Last Modified: Wed, 15 Jun 2022 21:46:23 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6907f5f220a4a7b8f159b7b3181573949ed823b2091b58a872fb32b668e4c276`  
		Last Modified: Wed, 15 Jun 2022 21:46:22 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495893f783b391eb45a628f64f30b0709b31e2b586e4ebc3d06bcc1c14a117dd`  
		Last Modified: Wed, 15 Jun 2022 21:46:19 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712e5c7ee2ddd6410e84a47a86b9a354fd97ad6c456c7d9c6f986d6a8b8ad702`  
		Last Modified: Wed, 15 Jun 2022 21:47:20 GMT  
		Size: 307.2 MB (307158629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021068a19ce66ba648c0ca7bdb6ce87fb2171ebbc03cb375be91b3488e58ac9f`  
		Last Modified: Wed, 15 Jun 2022 21:46:19 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a0acf48295984c224e2ce7c813167dbb2610cc48f31f945b9c21ead54a4eb8`  
		Last Modified: Wed, 15 Jun 2022 21:46:19 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177fd6f39f15f4ef990e0eff49921ed6c53fac851295be30ed2c00d5cb9d97af`  
		Last Modified: Wed, 15 Jun 2022 21:46:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
