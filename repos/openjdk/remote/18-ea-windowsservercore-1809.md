## `openjdk:18-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a94395b4f0e18758da6a521177d6db6e0662130c9de654b7100ed48b66c2fe1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2458; amd64

### `openjdk:18-ea-windowsservercore-1809` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:cbdcfdeb103d46035e7d1ed61e431e278952b708a54305cfae2f036c53ba2efd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2898336131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740e5f248a6564ac54d6a04881a01e1a37f6d97bf7da937c66bb80450320c24f`
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
# Wed, 19 Jan 2022 23:27:05 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 19 Jan 2022 23:28:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:22:45 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 02:22:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_windows-x64_bin.zip
# Tue, 08 Feb 2022 02:22:48 GMT
ENV JAVA_SHA256=116c696ad08d6eee42a25ff414aedc31b9b6b88e237b03896da9ce2f1f144475
# Tue, 08 Feb 2022 02:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:24:47 GMT
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
	-	`sha256:0172c57785f787b33a69547a8cd17a42a8e99d7eeee9b34f192106f04e3d1283`  
		Last Modified: Thu, 20 Jan 2022 02:25:45 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc472f96d3f77466132b90c0d35c65ef0ad21d331ad9a1317f54076aae9e6aee`  
		Last Modified: Thu, 20 Jan 2022 02:25:45 GMT  
		Size: 310.6 KB (310626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef69d9e83664902133d20be896bdf3ae596dc66878ca019552c1773625ed28c`  
		Last Modified: Tue, 08 Feb 2022 03:35:31 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94999ea114d04830ef0e251410b882d352c1bdcdd5d305f5f128b34df0237021`  
		Last Modified: Tue, 08 Feb 2022 03:35:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643aa2fb64d068a97b4b59549aa9b0598b1e1603c6a69a0726eb22a5e412fb12`  
		Last Modified: Tue, 08 Feb 2022 03:35:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e987b0e3f04554d8e5cf83891de9c2bcb5aba5be4ae47f03a5f4bb55039d39c9`  
		Last Modified: Tue, 08 Feb 2022 03:38:55 GMT  
		Size: 184.3 MB (184338213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc2d461e84a3025ce0732f38bc04977c582d0cfb3fe73752165a57089a7a394`  
		Last Modified: Tue, 08 Feb 2022 03:35:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
