## `openjdk:19-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:b26c72a38a481cf09e101525f6470cd688900bc8535034ca7669f31476096bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `openjdk:19-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull openjdk@sha256:52ab992501daf66de3328152be5bfb9948e73bdb1adc28ecafea134d6ab84e18
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377279807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcc9efec8857bb309ebe2673bc98676a86369600531c1265574244c6b1fe5b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Sat, 18 Dec 2021 00:09:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 06:52:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 18 Dec 2021 06:52:32 GMT
ENV JAVA_HOME=C:\openjdk-19
# Sat, 18 Dec 2021 06:53:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 18:59:56 GMT
ENV JAVA_VERSION=19-ea+3
# Mon, 27 Dec 2021 18:59:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/3/GPL/openjdk-19-ea+3_windows-x64_bin.zip
# Mon, 27 Dec 2021 18:59:58 GMT
ENV JAVA_SHA256=f36c3877bce15485798362efa5043564eda9265027dfb7b42a219fa5659ecda3
# Mon, 27 Dec 2021 19:01:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:01:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5bc74beb7593c703ac99379d225f3a9a445549cc06a3fe18f44e356a45f225f3`  
		Last Modified: Sat, 18 Dec 2021 01:18:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf6738034b8742c8193d3db825f75f650b85ef03ad87a2f9e6d91f195c38d2`  
		Last Modified: Sat, 18 Dec 2021 10:51:31 GMT  
		Size: 635.1 KB (635126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af418b5be8b1aed475657e98454850f5f8c5c731d3a5a481ca2618df77df647a`  
		Last Modified: Sat, 18 Dec 2021 10:51:30 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e19ac6575c209170fa57470a8b18a8200a0e0fed6de37f997e0245e535a62c9`  
		Last Modified: Sat, 18 Dec 2021 10:51:31 GMT  
		Size: 544.3 KB (544334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf6d13b2b491799b27e0101eee603b9bc661f7d50ae7f414771754be02ea5b9`  
		Last Modified: Mon, 27 Dec 2021 20:21:12 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e9624ea69e0703322711e14d21dc930064b98ddcf7b79df6eef12572ab10f0`  
		Last Modified: Mon, 27 Dec 2021 20:21:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c29f71d7d5f2bc9e64249b2b9351fbb68e0abaea1c7a110fc85ca84e55d6c0`  
		Last Modified: Mon, 27 Dec 2021 20:21:12 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7a62e0dd608daaa3d0cfcc4f8224ea0171e5f43be3a54c921ac4e4d1b1e1f6`  
		Last Modified: Mon, 27 Dec 2021 20:21:33 GMT  
		Size: 185.3 MB (185320257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88969e95213468ff3800adda2bf7c0d188446ed76bd189eb2d4eb3e270b64816`  
		Last Modified: Mon, 27 Dec 2021 20:21:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
