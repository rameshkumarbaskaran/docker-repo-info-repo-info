## `openjdk:15-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:464f25380aa84cda6e5385e7dca484a40ff324a3c55b10c497533143cbd656ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:15-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:deedcf54e127bbac00478f010b489887e05e3ff15aeef2099e0ab8aaf105e5c7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416533115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71085bc8fff486f39c40da4b5417777b93c52e1ecfbda3786f0422ea25c4edf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2020 23:47:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Jan 2020 23:47:08 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Jan 2020 23:47:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 18 Jan 2020 00:16:03 GMT
ENV JAVA_VERSION=15-ea+6
# Sat, 18 Jan 2020 00:16:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/6/GPL/openjdk-15-ea+6_windows-x64_bin.zip
# Sat, 18 Jan 2020 00:16:05 GMT
ENV JAVA_SHA256=986c4c7238ce3c186819a7441292bdbaa4627567bb6a6631bf20ec40e93e31ed
# Sat, 18 Jan 2020 00:18:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 18 Jan 2020 00:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe8a4080f0d1077681de059bc8597064c929d967b370eac061cacf38283adfe`  
		Last Modified: Wed, 15 Jan 2020 01:45:23 GMT  
		Size: 4.5 MB (4547614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999496898b39d56596bc2d3245e819970ebe69da77cf3fe1f27527f01cd6428`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369268aba26b31281a3faa935154fe9feaf8ee03872fea566a30dc11dafbd2e0`  
		Last Modified: Wed, 15 Jan 2020 01:45:21 GMT  
		Size: 289.6 KB (289641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94ce55be42f762ec5b3e350103ee26e1130ac00b024039493c8d0158d44787e`  
		Last Modified: Sat, 18 Jan 2020 00:34:19 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc9377c1a8590e44ed98c397df9e35e0ab025767724ce4f1115cc63fdfdbb9`  
		Last Modified: Sat, 18 Jan 2020 00:34:19 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcb4935b2b15fdc8be1861d1eeccd9919b2f4bac0389f57065d172b8ef8d11`  
		Last Modified: Sat, 18 Jan 2020 00:34:19 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a795dc2053473ad7490d7aeb0c868a833257c6e4e496845331e815a72491d9b`  
		Last Modified: Sat, 18 Jan 2020 00:34:47 GMT  
		Size: 194.3 MB (194277527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13cfb718797a35808ff782198a8bb4e8c756b001eec61400c5324a5c2e6afc8`  
		Last Modified: Sat, 18 Jan 2020 00:34:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
