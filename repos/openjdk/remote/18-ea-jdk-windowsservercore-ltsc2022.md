## `openjdk:18-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:00309068ce698b3506871ff2175c2a8d6786f1609ccd5261556675fcdf16f35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.469; amd64

### `openjdk:18-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.469; amd64

```console
$ docker pull openjdk@sha256:6231989d45d3b49fd49958304814931339c1ee06d12f958812e8dccb13749830
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2393425065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d809def908e7294a0b4beb71087082972562af39806f6ff78ba56e66da3bad84`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 06 Jan 2022 03:56:33 GMT
RUN Install update ltsc2022-amd64
# Tue, 11 Jan 2022 18:59:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:09:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:21:09 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 12 Jan 2022 05:21:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:21:32 GMT
ENV JAVA_VERSION=18-ea+30
# Wed, 12 Jan 2022 05:21:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/30/GPL/openjdk-18-ea+30_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:21:35 GMT
ENV JAVA_SHA256=57e77e09ea1801bd17d69a31b973074ea5bfeafdc150ca0376b7df8f593629f3
# Wed, 12 Jan 2022 05:22:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:22:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b593686e27e7562a5b0696823307ffa822214cee8bd2eec1075eadad4cb9712`  
		Size: 956.0 MB (956001983 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:99e0b71ede60d3b2c5b9053bf27e47c0875590991eede49813d849cc660c7551`  
		Last Modified: Tue, 11 Jan 2022 19:32:06 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42ce1d7b7857ac1eb8d4fbf9579f07cf6a89ed47f3a0979451365d92324f699`  
		Last Modified: Wed, 12 Jan 2022 22:55:59 GMT  
		Size: 644.8 KB (644784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcdfa2da65ea1a1d06b424da27e67263157b1e5a0cb8cf1a5ea3abede1a4007`  
		Last Modified: Wed, 12 Jan 2022 23:02:11 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d4d837417b9f24bd4783e24e7885836d5bbbccd2a465481dfb85aef6cac6c`  
		Last Modified: Wed, 12 Jan 2022 23:02:12 GMT  
		Size: 551.5 KB (551542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748080050c60eaa9f3140b41c6bd630a27a6b7124a6400786af351d904f8524e`  
		Last Modified: Wed, 12 Jan 2022 23:02:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845352c55222ce1d4da98d5d9aeb4560b39fe26e780810f207c7beae16ecb07c`  
		Last Modified: Wed, 12 Jan 2022 23:02:09 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9938c512137d258605deda56fa17013707713090d27391d3bc66c164ca795c22`  
		Last Modified: Wed, 12 Jan 2022 23:02:08 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1293b9a0c00deefb06ed91cb7ad6c727249dbc78c16f51df2c7580d2819632d`  
		Last Modified: Wed, 12 Jan 2022 23:02:29 GMT  
		Size: 184.5 MB (184519311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d43a192a8ed40a247395cff1cf54d39d29f6e3b244d86952cf5dd894e4235d`  
		Last Modified: Wed, 12 Jan 2022 23:02:09 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
