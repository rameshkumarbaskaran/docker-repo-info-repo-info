## `openjdk:19-ea-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:af2a351d67b5165afc663761c881c8c50ab6a18f6d3b2be0998f2c528ba9fbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `openjdk:19-ea-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull openjdk@sha256:3920e8839ddaaf93223b4dba04bb3570507ca8fd48a5822c7162c9a9afc978d2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6458938279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96e52ba3ab04578c5adc14c434dd6d80fc06410c1d3f53a59e3e9f1361a4b77`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:29:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:22:21 GMT
ENV JAVA_HOME=C:\openjdk-19
# Tue, 14 Dec 2021 01:23:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:23:43 GMT
ENV JAVA_VERSION=19-ea+1
# Tue, 14 Dec 2021 01:23:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/1/GPL/openjdk-19-ea+1_windows-x64_bin.zip
# Tue, 14 Dec 2021 01:23:45 GMT
ENV JAVA_SHA256=2964c4ea8952f33b7d853c7e8c7a7535fc2b6ab560815bbd4befd0581708b944
# Tue, 14 Dec 2021 01:25:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Dec 2021 01:25:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f998978d6856e995f1d9c4942941c32a17a4d88aff023bd7b9c78fc2a16c252e`  
		Last Modified: Wed, 10 Nov 2021 21:07:51 GMT  
		Size: 355.7 KB (355709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b20d7d9b219732793c0c2ed8c965396357456bda3484682d91f704d45d7ca9`  
		Last Modified: Tue, 14 Dec 2021 01:34:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a7d95b5fa9aa0bced88444707c4297d68405015305f1ac437f10ca0855568a`  
		Last Modified: Tue, 14 Dec 2021 01:34:02 GMT  
		Size: 367.5 KB (367504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e2ffe7cfaf80dd0f9595ba14ba77dc24252d86eb5a49d8d3144de461835fda`  
		Last Modified: Tue, 14 Dec 2021 01:34:00 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95bacdcc7d3992d1e49493fbc942df50e554d0f8e576fd232c1453342fa4f70`  
		Last Modified: Tue, 14 Dec 2021 01:34:00 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42da4dfe0584d7e51669bd5071d9ce50cfa576a3e6a64decea8565d565c9979`  
		Last Modified: Tue, 14 Dec 2021 01:34:00 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435f2cf70bddcb9cd858667af177ce7f2b40eab77e4c8929d08560f1b8deac4f`  
		Last Modified: Tue, 14 Dec 2021 01:34:20 GMT  
		Size: 185.1 MB (185115652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4a384503b174e9ddd6c9c54a7db3c4ddbe8e81c9fb675268ec258b64bb2e35`  
		Last Modified: Tue, 14 Dec 2021 01:34:00 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
