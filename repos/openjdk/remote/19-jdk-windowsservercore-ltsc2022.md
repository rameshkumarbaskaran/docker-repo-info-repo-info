## `openjdk:19-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9e1a1d331060ca2b7e57adbc3aacc51a2820d58dbf2240c3c337982131153b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.469; amd64

### `openjdk:19-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.469; amd64

```console
$ docker pull openjdk@sha256:2e1562014fc4c3fed5559daa29936977f8c9e0664dc2423aef30990a61991c87
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394270359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c71647ba6bbe35385b926bac7e138520dffdf92baf9083a40d2f6f0beaf21b`
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
# Wed, 12 Jan 2022 05:09:50 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Jan 2022 05:10:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:10:10 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 05:10:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:10:12 GMT
ENV JAVA_SHA256=d76667c6d142d73576ea27adc9849ccd7f116011bbb4f22c7f0a76635d3a2901
# Wed, 12 Jan 2022 05:11:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:11:13 GMT
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
	-	`sha256:b3aff587b21f31d2c01622cca482ab4ce1034e72ec67fe0a67894e20119fc654`  
		Last Modified: Wed, 12 Jan 2022 22:55:58 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b01c57c266a512234c3cad7efd226645be4c579a3d14e556c78c5aa280c06f2`  
		Last Modified: Wed, 12 Jan 2022 22:55:59 GMT  
		Size: 551.5 KB (551450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39723ecca756aeb7ff1c172bc833a42ee65c24010d6c0395167e777158158831`  
		Last Modified: Wed, 12 Jan 2022 22:55:56 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abaa599120b54bad069c2d33b1fbe0f45fc8b7c7306e6b66fd7dd47a12d14b`  
		Last Modified: Wed, 12 Jan 2022 22:55:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afed6c38928bb44b52e033e7c96d1b575f302bb2f49f07669610c6078abca6`  
		Last Modified: Wed, 12 Jan 2022 22:55:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba3e8fe055e2eca37b02993ae0385d6c878f868991687720ca48e8ad3e5ed0`  
		Last Modified: Wed, 12 Jan 2022 22:56:20 GMT  
		Size: 185.4 MB (185364683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315ad1f1bac7627b5759f0aa8dabba315dabc90c6bbecbcf9bc09f539ad3b2e`  
		Last Modified: Wed, 12 Jan 2022 22:55:56 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
