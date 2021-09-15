## `openjdk:18-ea-14-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:9d7beabc2d6eda31eb09e9bdced33b8fbaae95799de229522ffcee976562a9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `openjdk:18-ea-14-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull openjdk@sha256:961ef0dee1e9f20aba44390f5128f90bbbad400426c2c988550fb3d6a9c631d6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6454931542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c720b5a82a7893a13b106406dea0023f5b0c6320b9ef30195d458bfa3b6596`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 00:35:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 00:35:52 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Sep 2021 00:36:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 00:36:46 GMT
ENV JAVA_VERSION=18-ea+14
# Wed, 15 Sep 2021 00:36:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/14/GPL/openjdk-18-ea+14_windows-x64_bin.zip
# Wed, 15 Sep 2021 00:36:48 GMT
ENV JAVA_SHA256=8351b7f8c8238ed783c357db70d64810a981b4ad4ea22687d9470f8a78809d3a
# Wed, 15 Sep 2021 00:38:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 15 Sep 2021 00:38:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b794d0a07a41196dae8678e4ecbb9a5766d6db31f9729bfe3f1d83963af3e0`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 339.2 KB (339172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d3bfbbd6119f5d4c8cdfa80560f7d1dfa6730c4d5af995fee76f3decd44528`  
		Last Modified: Wed, 15 Sep 2021 01:10:17 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8da815f1cb98dfe565a92045b7ed382138e2c7bbbba2982c14bcecce8161396`  
		Last Modified: Wed, 15 Sep 2021 01:10:17 GMT  
		Size: 335.9 KB (335946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae0fd8c3f15291dc3a0d08caf9444adacdc2478014c26ac4f55257122796155`  
		Last Modified: Wed, 15 Sep 2021 01:10:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67158bded6d4222483c4b14c809fe749bad816733b2d975c42e2dcc36d10433b`  
		Last Modified: Wed, 15 Sep 2021 01:10:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1c5f1349cbd37d7e82d507c3ce1f82e0f863c0930ee8e6547c402ca0675b08`  
		Last Modified: Wed, 15 Sep 2021 01:10:15 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8389dea2f82ed5401c82421e939d32fa047238be2661dd15af45d06ea2c4f4`  
		Last Modified: Wed, 15 Sep 2021 01:10:32 GMT  
		Size: 182.9 MB (182920379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694304d987c32174cb43b96233d151dae6af104812ac367cc7fbde6e2606e8d3`  
		Last Modified: Wed, 15 Sep 2021 01:10:15 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
