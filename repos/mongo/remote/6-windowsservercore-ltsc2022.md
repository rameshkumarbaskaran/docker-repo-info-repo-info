## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:72b2ec69bee01dceb5e98df0dfcd4acbca7f64a6a37fe22fa6d6a3a3fd0ca21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1668; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1668; amd64

```console
$ docker pull mongo@sha256:84dfac76c86f710c8f73b7e1cf41b48f7ffe53b042fc2232ee02790418f5c7c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2278392015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc70c6f4948bce8295ed3a457af98e1b510ffeb91243c57308df36270fe4d40a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Wed, 05 Apr 2023 00:38:27 GMT
RUN Install update 10.0.20348.1668
# Wed, 12 Apr 2023 00:15:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 00:15:39 GMT
ENV MONGO_VERSION=6.0.5
# Wed, 12 Apr 2023 00:15:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.5-signed.msi
# Wed, 12 Apr 2023 00:15:41 GMT
ENV MONGO_DOWNLOAD_SHA256=79327a9901a39182dee2d74f84e46b4c6b1416cfc2c0cee791322ea82dce0388
# Wed, 12 Apr 2023 00:18:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Apr 2023 00:18:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Apr 2023 00:18:15 GMT
EXPOSE 27017
# Wed, 12 Apr 2023 00:18:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ecfa9c953d28a9da9d422b57cd0361c57c44e1faaaed7e50a2537d1c29cee1`  
		Last Modified: Wed, 12 Apr 2023 00:50:33 GMT  
		Size: 376.6 MB (376573004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3664aee9b0b3199a388e1a7d17e99ada617d122d6a2572b0c40140fdea31a3`  
		Last Modified: Wed, 12 Apr 2023 05:57:17 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f511ab8c1d41f187ed90b2f2e8190065e7201d02bc53977867b58b12378748`  
		Last Modified: Wed, 12 Apr 2023 07:21:18 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc06c5cfec56616612c1e81f10a29220ea311d18a3a84a7e2d0c62f4cd28e53`  
		Last Modified: Wed, 12 Apr 2023 07:21:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72800503d7af7f0ad7c08b79042e01fc0184b61bc705ba5893efa99781501eb7`  
		Last Modified: Wed, 12 Apr 2023 07:21:16 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cca9c8c32549448d6b41a5e6373d4c50c17c096b5d6e889d7e4bdf80d168341`  
		Last Modified: Wed, 12 Apr 2023 07:22:37 GMT  
		Size: 515.8 MB (515780009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaddfa09e2517bcac1838b37267662400812cec5e2f65f327e547b8408966615`  
		Last Modified: Wed, 12 Apr 2023 07:21:16 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84de16ccccb55cdc1a4abbdc2f33736996f2a4cf89254798b5fde9f3fceab7f6`  
		Last Modified: Wed, 12 Apr 2023 07:21:16 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ee52581ee44041dd63eb641d28af98432fa00cef5b6d6fd6a76b0e8250dab7`  
		Last Modified: Wed, 12 Apr 2023 07:21:16 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
