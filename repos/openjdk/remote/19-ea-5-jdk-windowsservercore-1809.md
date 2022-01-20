## `openjdk:19-ea-5-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:b0f6f956df7a3f63deba532d18369c5931e9f85a9dab70d5daf135616f1b93c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-ea-5-jdk-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:086ac9333baa6a4f98696effa9ef688bc2621ac379aa8f293cce9da656420cea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2899183812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927efc65e419ae881333934b6a2d79cbe28c03b241fcf45afd02ad62b7b025fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 23:23:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:23:42 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 23:24:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:24:44 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 23:24:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_windows-x64_bin.zip
# Wed, 19 Jan 2022 23:24:47 GMT
ENV JAVA_SHA256=f26cae210cb484a48c086f2207018482162d2dd793fb69cc5575dc575159ee1c
# Wed, 19 Jan 2022 23:26:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:26:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98c73c8d54eeae51e9c93499966b4413ea63f218bdf175bed7b7d83c76e6d58`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 357.3 KB (357347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64554bb59fd3345200ae4e79426f465295d19e9d1be31e0f5a60f5ddc13af5b2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec53942b6c9dd8e8c55c8a2268d1a09a715d75e3edcf063826fa7462dcdb7c2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 310.5 KB (310471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d141803c8aab02129e988faf86c371d9b668e48eca86018fc286832474e30c41`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb1987e1022766c5d2f165a31c73811ef92d4355641df7c1ddbdcec622af64f`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b640b981a509de2f8f450f072f57ab99586f4006ae9bb091972dddffffab28`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da608d0b4f17679a64e5378495b3e4f43cc83e88714bb05f4eab7c0a39deee0e`  
		Last Modified: Thu, 20 Jan 2022 02:21:01 GMT  
		Size: 185.2 MB (185185994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b539e8137a7eb304fd00a373dda61eeba820ce6e1497f9236a698d64e1691a`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
