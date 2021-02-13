## `openjdk:16-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:8265af3cc08d02e996b2355ddf68849c0ec5c4439801040afa8b75465b8cf6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `openjdk:16-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull openjdk@sha256:9b2c66dfbaf216be3c376089795ef87269b963cc9af4fd5998512867916eed47
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6000989590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c21c6811a673b28a28b86a887a82ab0492bbb6f54b0d5130b1c1dac9aab56d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Feb 2021 13:17:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 16:42:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:48:06 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 10 Feb 2021 16:49:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Feb 2021 16:49:11 GMT
ENV JAVA_VERSION=16
# Fri, 12 Feb 2021 23:21:18 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_windows-x64_bin.zip
# Fri, 12 Feb 2021 23:21:19 GMT
ENV JAVA_SHA256=a78bdeaad186297601edac6772d931224d7af6f682a43372e693c37020bd37d6
# Fri, 12 Feb 2021 23:23:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Feb 2021 23:23:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c03f1c41641d4a4cf6906dee9a590ee67135d926dddab80cfef993cae745a38a`  
		Last Modified: Wed, 10 Feb 2021 13:41:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852b6d2d8c5b49e04837d97a06dfd545d620e2355d40bc0014a563f58a5c11c2`  
		Last Modified: Wed, 10 Feb 2021 17:16:55 GMT  
		Size: 10.2 MB (10165560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf33ff9974a77a6927bbb405c259aff07f6466966e1ca770886fefed9b3df4e`  
		Last Modified: Wed, 10 Feb 2021 17:25:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfaf5e25eb465503b52f34a88c18a5dfdf062df7eada05aba2d62994635eec`  
		Last Modified: Wed, 10 Feb 2021 17:25:16 GMT  
		Size: 5.6 MB (5618488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7dd1d6ef80fc195bf837372cbba0657490bfe9e2c1b28193bc07f8a9bea7a57`  
		Last Modified: Wed, 10 Feb 2021 17:25:11 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b5072edd632042dcde9e92f4fdaf65167e9f4d83af3921d3fe37f25aa5b0e1`  
		Last Modified: Fri, 12 Feb 2021 23:34:41 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a9c8d5dc203ffa6863eb51fe5e0e23e5ae68b5428b20f524b1b3483fcb7a55`  
		Last Modified: Fri, 12 Feb 2021 23:34:42 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ac70b13b9dd7adaada85c6756f954518e3047dded85a7caca0c96ce8ad2c00`  
		Last Modified: Fri, 12 Feb 2021 23:38:18 GMT  
		Size: 190.2 MB (190184347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f56503fc4c326221ccffc276a34aada4775df47db8cadcb68a1f6b82382d45`  
		Last Modified: Fri, 12 Feb 2021 23:34:41 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
