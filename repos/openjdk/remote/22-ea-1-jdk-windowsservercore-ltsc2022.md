## `openjdk:22-ea-1-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e84d9df681a1027c1615b2a4706b63fbeba886df2acd39f45b332a3375edcf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1726; amd64

### `openjdk:22-ea-1-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1726; amd64

```console
$ docker pull openjdk@sha256:e6e33a3fa0de28e4bfbba484b83750306fabf0503ef20d700375e81f89a94a1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1974831011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fbfcf710ee042c2b3748736a7ba418fa524b66eb63e44104171351792bbc08`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:50:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:15:18 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Jun 2023 22:15:38 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:15:39 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:15:40 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_windows-x64_bin.zip
# Mon, 12 Jun 2023 22:15:40 GMT
ENV JAVA_SHA256=9348aa2fc8344b25baad9b614627983b4e900ab0293ecfa3ec7f9b5d911a90a7
# Mon, 12 Jun 2023 22:16:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Jun 2023 22:16:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500851308f2a80744cfa1cca578e46041bad797f47ea2d8c83f894349fac438`  
		Last Modified: Wed, 10 May 2023 03:00:03 GMT  
		Size: 448.7 KB (448735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1b04d8e86e4fc820778c292565a927a7c0b8ab6e1485798be522acb1563f99`  
		Last Modified: Mon, 12 Jun 2023 22:21:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aa27f4debf297ef66d2791e5d0af76f9dc4fcac1d414654f55c9b39cb94a61`  
		Last Modified: Mon, 12 Jun 2023 22:21:54 GMT  
		Size: 277.5 KB (277469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38bd61921c415cf3c98572bb9bc5439936ca29afde180c04aa52ca52a7ab19a`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45407f149dbf3373d601485ca6637450b7723ecc4a1a073606db489cf06bc78c`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cc61bf231d80c6aba410b215c5b6ae89436263117e417e953502921f3c38c0`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2723c53892b2a4204019188c3cf473db6debd89ad87b02ecfeebcb54c03308f4`  
		Last Modified: Mon, 12 Jun 2023 22:22:12 GMT  
		Size: 199.1 MB (199114912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92b36563970ba8c57a18a3f8fef1ffd9244fe979ebc049fd31ce9f68e214cd1`  
		Last Modified: Mon, 12 Jun 2023 22:21:52 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
