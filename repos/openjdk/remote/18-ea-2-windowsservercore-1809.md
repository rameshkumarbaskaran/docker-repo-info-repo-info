## `openjdk:18-ea-2-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fa697c784c680af57c95c5e0ef8ccbee64d6b2b4a09403cb446c38afa2c76eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:18-ea-2-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:09c07f98cc4344573fff741524fc726606bfa6b63668532890c5bbc287553734
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2825618955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54b029ac566296fe862dd1fbab7b17cdb93ebe7dafc1743cc74e2e2e92f39a3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 16:45:14 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Jun 2021 21:15:22 GMT
ENV JAVA_HOME=C:\openjdk-18
# Mon, 14 Jun 2021 21:15:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 22 Jun 2021 21:17:31 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:17:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_windows-x64_bin.zip
# Tue, 22 Jun 2021 21:17:38 GMT
ENV JAVA_SHA256=4f7a1b71a31a48a04127d3ef3d6838e2316e77a9f70e5aa291b5deeb7f6f2181
# Tue, 22 Jun 2021 21:19:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 22 Jun 2021 21:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f84ebe44976489de74231891a3bceaf046cdaf5d963f8d9785d418863bfd7`  
		Last Modified: Wed, 09 Jun 2021 17:24:02 GMT  
		Size: 352.1 KB (352057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bd075f6a28327feb9e96d70254b0ff44b766a2e56a18072ff163e70ab386fe`  
		Last Modified: Mon, 14 Jun 2021 21:34:37 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa2a31e5867692161ad9dadb7bf7c188d8920e562c457a95645ccb8193bd9d3`  
		Last Modified: Mon, 14 Jun 2021 21:34:37 GMT  
		Size: 339.5 KB (339492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af9cda1954ef873949743bbea2417213439287303b88b5a4eeb931cad8b824`  
		Last Modified: Tue, 22 Jun 2021 21:32:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724d3e1006a3a901de23c9706e1de7240fa353f37d34ae528b708dc275e2e972`  
		Last Modified: Tue, 22 Jun 2021 21:32:37 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca3ff3f976fe9c9a8ccc3a686286db3e6769b0f11e42702eb0ec5400af2c4b2`  
		Last Modified: Tue, 22 Jun 2021 21:32:37 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a91f001393ebef552f1eb1f4fdfec8c6a64b0a996b94ea05dc5043f5f1de42`  
		Last Modified: Tue, 22 Jun 2021 21:32:57 GMT  
		Size: 183.3 MB (183333800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df34eb25169dd3387576a130846cc7160d48eed47caecf692fe5cb30763466d`  
		Last Modified: Tue, 22 Jun 2021 21:32:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
