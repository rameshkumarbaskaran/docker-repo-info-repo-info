## `openjdk:17-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c5990ff5ece757a9ddf49f7a424539632cbf49e6cf53119a01c0d5673ee463f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:17-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:dff4874a6fef351576bdd1e10a3a88fc5e702fd88e999078c043fa6a29771374
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2824731226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc235aaa05b621fde20aa068525c6d7656704e6fbc5d1ba02e69a21d10e91fa`
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
# Wed, 09 Jun 2021 16:45:17 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jun 2021 16:45:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 22 Jun 2021 21:23:12 GMT
ENV JAVA_VERSION=17-ea+27
# Tue, 22 Jun 2021 21:23:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/27/GPL/openjdk-17-ea+27_windows-x64_bin.zip
# Tue, 22 Jun 2021 21:23:18 GMT
ENV JAVA_SHA256=1aa47b9df08e6b04f434d89908516c4a54d6fd058c8c9bdaef2b492dab6a8a50
# Tue, 22 Jun 2021 21:24:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 22 Jun 2021 21:24:29 GMT
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
	-	`sha256:580f726be9e9223f5fbe72ec77a450134c84e6501882795e77ae88e34b87949a`  
		Last Modified: Wed, 09 Jun 2021 17:24:01 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6098af536049b2e7b8c27707faac52e3ac75b37f3ba29e5543ea2f149e8ce501`  
		Last Modified: Wed, 09 Jun 2021 17:24:01 GMT  
		Size: 310.1 KB (310100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096448d5d0f5d5dbac82ac686b53ad52cc8c1a01d6a7f3eb539cca03a8abbc05`  
		Last Modified: Tue, 22 Jun 2021 21:38:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b88a0a735b630685285c96a242fec689e36180df5b668b8a81d460c552b4e4`  
		Last Modified: Tue, 22 Jun 2021 21:38:10 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1df35326107b71cf307f88a103c0e9f87f664081e4f3190580f5faa1fe5189a`  
		Last Modified: Tue, 22 Jun 2021 21:38:10 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3da06b28041b4ce018a3a54608a62cd13406eefb85249bf9b6e174c114e6e2`  
		Last Modified: Tue, 22 Jun 2021 21:38:30 GMT  
		Size: 182.5 MB (182475539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402bdc1fa53aa3788b07767b864a81888e9ed224d53aa5b87f7684e75bd9253`  
		Last Modified: Tue, 22 Jun 2021 21:38:10 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
