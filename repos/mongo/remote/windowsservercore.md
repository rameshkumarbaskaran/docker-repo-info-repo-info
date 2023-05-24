## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:e27d1d22730198a5809a9440385e8dc94f47255cdd1befa2b1b854f696e33ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull mongo@sha256:a2f69ee6120c8a6a8aecfb8b549a6908b487b1e60f091defdb089abac37a865c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291249118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f69c64675d1a5b1fb32837234214a489c9cf662056000b942410123b5aa9a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 01:53:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 May 2023 01:15:18 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:15:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Wed, 24 May 2023 01:15:20 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Wed, 24 May 2023 01:17:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 May 2023 01:17:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:17:23 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:17:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ae2b2372db6d2d1ac04a5297e71fc9a798a078f7d1a0bcccae77193e8b58b2`  
		Last Modified: Wed, 10 May 2023 02:22:13 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d831657b6564663196da33c47e5fa0f92a4e6b78e4a96b9cbc1ec1bf946ac8`  
		Last Modified: Wed, 24 May 2023 01:36:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672c5d119420c2b20df34efd39c415c938b2db3d4dcdb592264506f5cfa6ec97`  
		Last Modified: Wed, 24 May 2023 01:36:41 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fdb8bdf3d875e92884eaabbf6b06a6496e13831133251a53af8ef37e21807`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a552c02ac76991f000d7287a801bcfc2bad41959603f378a52ada85ebe4bd263`  
		Last Modified: Wed, 24 May 2023 01:37:52 GMT  
		Size: 516.3 MB (516257735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b5e8f7877f1db588fc2aca5f97f743d8fa294704483f477087ac48ca10727f`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ba9687f93d1fca18db83236308825e8a2da391a369922a050920b18c05c1e9`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d671a02933775a0a5d518cfcd7a98aece04846819091f0feeaeae05f1bcc7459`  
		Last Modified: Wed, 24 May 2023 01:36:39 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull mongo@sha256:095a6ea5ce5ab252da3482e9473e849f9df5d94fe24e97a72392e6cb7048615f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2588350793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a95a1c92ed7b9c11f977baff37067a95367b36e465c3ce408f33b5d97de5cf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 May 2023 01:17:31 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 24 May 2023 01:17:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Wed, 24 May 2023 01:17:32 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Wed, 24 May 2023 01:20:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 May 2023 01:20:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 May 2023 01:20:23 GMT
EXPOSE 27017
# Wed, 24 May 2023 01:20:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81422d35aa8341bef06d995d7408b001c17532ac305453ae0624a5fe5e5e6657`  
		Last Modified: Wed, 24 May 2023 01:38:08 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701a81d477339f7560020a3830e02d167506aa5d802fc0b2760d0f4b94db5cc8`  
		Last Modified: Wed, 24 May 2023 01:38:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54657ad5e91207bfa9bebbebee13cf435d661b2582babb24ce1836f591edd41`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddcc78b8d32e33da88a9fe23fd9f9dab4a91f107b829263619cf23424e801bb`  
		Last Modified: Wed, 24 May 2023 01:39:23 GMT  
		Size: 516.3 MB (516305726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f04476c99fec34f432553c85888a9d9f7bf5a96fba998745250a25c6212815`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da05dabf67ce090785770af822f43b188c4bdef6e4b536387bae97abd6e65516`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e117fdef73bdf4e0a5707103633f94f2eb79a4ec5da4a5c53cde435bf9b86e1`  
		Last Modified: Wed, 24 May 2023 01:38:06 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
