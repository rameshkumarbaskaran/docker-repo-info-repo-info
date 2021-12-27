## `openjdk:18-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b4f8327a31fcd39b15f499f3769952483cc1dea253bf96996279d2cfce4d6032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `openjdk:18-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull openjdk@sha256:a4869d24127856958198d5229514a7ad07277c702bb940029ecb336e7b936e39
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2376444110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf9dfb2ed99668ffc8e44d05bd4747bc1b7e7af035204656652441fb0905005`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Sat, 18 Dec 2021 00:09:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 06:52:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 18 Dec 2021 07:03:46 GMT
ENV JAVA_HOME=C:\openjdk-18
# Sat, 18 Dec 2021 07:04:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:07:04 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 19:07:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:07:06 GMT
ENV JAVA_SHA256=7ce8c0466233333b8ca3dfa4da6c9e122b8c7a7b4322141c2961921fb32e873e
# Mon, 27 Dec 2021 19:08:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:08:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5bc74beb7593c703ac99379d225f3a9a445549cc06a3fe18f44e356a45f225f3`  
		Last Modified: Sat, 18 Dec 2021 01:18:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf6738034b8742c8193d3db825f75f650b85ef03ad87a2f9e6d91f195c38d2`  
		Last Modified: Sat, 18 Dec 2021 10:51:31 GMT  
		Size: 635.1 KB (635126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33616cf8971399858dc392d3e603c9a6c4eff8c6054af2d8492d250b300756b9`  
		Last Modified: Sat, 18 Dec 2021 10:57:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d1a684c0e994a86f11bcc0f30830fad11b052093f81257505ce6a25ecac099`  
		Last Modified: Sat, 18 Dec 2021 10:57:14 GMT  
		Size: 544.5 KB (544523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d5fdaabdfcacf664c3b2b3be6e76384006e36c76a1c9bddb18a16c7de4c1ae`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5768682fffa60d9adeed2d76c30e51565e52a9424f82baa0bc7d9aa2ececabd8`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194328d1856f5c3f1e13e5a50e7b4d0969b3c710bf2c4a011f1acea130b5fea`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23080ebc1b7cfc8f3c2422d3b7ab2067d48a090587b6206bba94b1db6a47f7f4`  
		Last Modified: Mon, 27 Dec 2021 20:30:14 GMT  
		Size: 184.5 MB (184484399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c915a6a780a2c8e906fe0e6045465b6358da69950161816f59865c656b01266c`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
