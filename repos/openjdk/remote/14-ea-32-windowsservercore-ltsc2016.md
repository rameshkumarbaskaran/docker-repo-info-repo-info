## `openjdk:14-ea-32-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:a648e0b5bd843d3047e3778faa19d5f363a9e1f714ef6a5f3c8d88989c349c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `openjdk:14-ea-32-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull openjdk@sha256:a3206a8f1821b246ed000bf0e9f8d04080dcde672a344787e63466ded9e08219
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5934613793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7696ca2edf096857f02eafb4f73d48f27ab8efec77e0ddef4fb4f5a630a3f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2020 23:51:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 15 Jan 2020 00:01:19 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:02:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 18 Jan 2020 00:26:14 GMT
ENV JAVA_VERSION=14-ea+32
# Sat, 18 Jan 2020 00:26:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/32/GPL/openjdk-14-ea+32_windows-x64_bin.zip
# Sat, 18 Jan 2020 00:26:17 GMT
ENV JAVA_SHA256=78b427c850c1245fb056a26b40e7edbd9cea01ec5aad8d70bfc2e53a540f7860
# Sat, 18 Jan 2020 00:28:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 18 Jan 2020 00:28:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59f69707d10b5be4e5c56881ea890fd476325bea3b16b5a7e7c56a1d8b3f056`  
		Last Modified: Wed, 15 Jan 2020 01:46:54 GMT  
		Size: 5.4 MB (5386027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40fa392055162d8b62010b964933f208b474a495503491293e2990c429114a1`  
		Last Modified: Wed, 15 Jan 2020 01:56:53 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa76c12f7c4dc8568e6a71fb5adf4fd6a8c29f7eeb6d4ffe9c361967e5eb82d`  
		Last Modified: Wed, 15 Jan 2020 01:56:56 GMT  
		Size: 5.4 MB (5368309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4ab3e079f0b30c6ca111db65769d2d14e9da0544de881f7ca6e1166ac4eb10`  
		Last Modified: Sat, 18 Jan 2020 00:43:21 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd6d7c40df58cd57dc5aa48b1aa8563c672d86cce6b5cc5840834de59c3b93d`  
		Last Modified: Sat, 18 Jan 2020 00:43:20 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8af5ee206f926788d43b79ca812192f20ee09a3d838da7b3a264dcc891deb7`  
		Last Modified: Sat, 18 Jan 2020 00:43:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b856ccb546b4d3931360d0c3db588530a4d2e9ac46a7957795974dc2eb5a412b`  
		Last Modified: Sat, 18 Jan 2020 00:43:58 GMT  
		Size: 199.3 MB (199253035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489a1ed9a79c75a489667c99d9d57aabcba94158dd23285d2425cd20cdb25e1`  
		Last Modified: Sat, 18 Jan 2020 00:43:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
