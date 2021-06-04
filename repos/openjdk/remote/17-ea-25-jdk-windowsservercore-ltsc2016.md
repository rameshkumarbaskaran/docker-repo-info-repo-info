## `openjdk:17-ea-25-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:1b97a9f0ecc273eb835c926f2b68fcfb66bd0cd77e1c521b84cab539ebcac9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `openjdk:17-ea-25-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull openjdk@sha256:556ff328d6c77f9a6098f338e0699fd5e789100632702bf51c9592afb2b45305
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5998265434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f636f87ba5722e4840c2dab48414eade5a8a291f91906aed479d7ebbd0b6dc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 May 2021 12:29:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 May 2021 16:38:48 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 May 2021 16:38:49 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 May 2021 16:40:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Jun 2021 20:36:16 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 20:36:17 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_windows-x64_bin.zip
# Fri, 04 Jun 2021 20:36:18 GMT
ENV JAVA_SHA256=b1cf7a899b6687db3553770a0ec1a6e17c5c357d44d2bf0c5845251c32e2d659
# Fri, 04 Jun 2021 20:38:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Jun 2021 20:38:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a280ee47051c0dfafc65e567f555ec59b7415288f965b44cf55c9187407d4248`  
		Last Modified: Wed, 12 May 2021 12:55:16 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e207924c83ffdb1664a8c8f2d8914f8ac2d146d0a5eec997b2c359ff33d928`  
		Last Modified: Wed, 12 May 2021 17:15:54 GMT  
		Size: 5.7 MB (5704156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a2dd60a2ba0434a7771edebc5672a533b07697e2e838edf0a81b78018a9b7e`  
		Last Modified: Wed, 12 May 2021 17:15:51 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a8ab2abad565743f1605667a5a908cdf299295c156e49d7fd0af878b56920f`  
		Last Modified: Wed, 12 May 2021 17:15:53 GMT  
		Size: 5.6 MB (5647985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0813d962cc3312b439a96f81797acf16c8eb74148b7c0e6afc2e462b6fc03f`  
		Last Modified: Fri, 04 Jun 2021 20:44:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1083fc8d75b1ac408dcd515c7ca32ad4190b5723698e8e4cb936d412d0795126`  
		Last Modified: Fri, 04 Jun 2021 20:44:50 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444dd8015f4cb2ed0685356ba770beecc1d8e11c7acdcf5e15a3c6dc31acfc9d`  
		Last Modified: Fri, 04 Jun 2021 20:44:50 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca0474118dc60154df9d6c9da9f585f5985e0d8da6c9788240af47e1f7ff028`  
		Last Modified: Fri, 04 Jun 2021 20:45:12 GMT  
		Size: 191.1 MB (191127393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010b4dfc6f866b5e7794b421b7a3032240f09093000c4620210bf90f8d363227`  
		Last Modified: Fri, 04 Jun 2021 20:44:50 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
