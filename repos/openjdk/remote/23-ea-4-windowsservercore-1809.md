## `openjdk:23-ea-4-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fffedc7915d7242084454477bf94175d36ea6294a3bbb3f95f7e9c2bf52e4cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:23-ea-4-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:163b71778a07dbcf560fae7a1de11ffa4693232ebfa624f02647281ef003d47a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258330362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fd90ca9612b019f9021724e44805626b98a2db2b2871f298bf49de2a33bcc1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 09 Jan 2024 00:54:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 00:56:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:56:08 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 09 Jan 2024 00:56:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:56:30 GMT
ENV JAVA_VERSION=23-ea+4
# Tue, 09 Jan 2024 00:56:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_windows-x64_bin.zip
# Tue, 09 Jan 2024 00:56:31 GMT
ENV JAVA_SHA256=14230e6d57a3b39a3b5e232e7095fe1821a48197f75b68ae0f09db29e5391216
# Tue, 09 Jan 2024 00:57:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:57:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeaf6a5261dcaacb8d6d772731ae526ae12424323a8be24219b6883bde20b250`  
		Last Modified: Tue, 09 Jan 2024 00:57:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7beb7f7c7ca187eeeb29db762db78f6778132ba483d3ab14c11dd20c669ba2`  
		Last Modified: Tue, 09 Jan 2024 00:57:26 GMT  
		Size: 486.9 KB (486932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9a39ac7d5aea0f6e2ff179e0960737af1cadaa43593071851438e03f0d1896`  
		Last Modified: Tue, 09 Jan 2024 00:57:25 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316458f549aa61850b14920580c760663f85e6b3f601182f3272e6f67379a1aa`  
		Last Modified: Tue, 09 Jan 2024 00:57:26 GMT  
		Size: 331.2 KB (331185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb84c2e16a3ee58c2134e1d7f2289811faf35ff9a458bd91569b9358e80c43af`  
		Last Modified: Tue, 09 Jan 2024 00:57:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0ee55c7fc4ab889e7bedf148153c4cd44d78e2bd23f46c094ab05ad7952b77`  
		Last Modified: Tue, 09 Jan 2024 00:57:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff24412bddf2440970e21f58e1863f034d144ade0e308f612dba9f381e83538`  
		Last Modified: Tue, 09 Jan 2024 00:57:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48686ef3474e821acf6d09486a6f188ac7cae8ef97e2501a58a7aa7e10b157f5`  
		Last Modified: Tue, 09 Jan 2024 00:57:34 GMT  
		Size: 197.8 MB (197795478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d42d67ab941be0d8291271900a6784d434ecbe30da2b6211c0477b7c433d82`  
		Last Modified: Tue, 09 Jan 2024 00:57:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
