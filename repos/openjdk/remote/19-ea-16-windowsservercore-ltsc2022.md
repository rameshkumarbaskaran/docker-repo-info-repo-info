## `openjdk:19-ea-16-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a98b56dd710cb89636209b206905cfcf03c1f1b0978a19d98fe4bf82e720dda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.587; amd64

### `openjdk:19-ea-16-windowsservercore-ltsc2022` - windows version 10.0.20348.587; amd64

```console
$ docker pull openjdk@sha256:9d2ecdacd2f0c003fbe9ab8f1906ddf3e8fa342bcd56fa6dc22de024161bc00a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2411137752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9779c58c429f4bb45fb067b35952cb1edff1a98a4d27f54c09e9c2909e16898`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Thu, 03 Mar 2022 05:02:11 GMT
RUN Install update ltsc2022-amd64
# Tue, 08 Mar 2022 19:26:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:08:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:08:44 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:09:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 07 Apr 2022 01:15:42 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 01:15:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_windows-x64_bin.zip
# Thu, 07 Apr 2022 01:15:45 GMT
ENV JAVA_SHA256=cb08aa89c98f4ec7c774554bf081cd7830b4e3f14760b32da5f77669ece2bbfa
# Thu, 07 Apr 2022 01:17:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 07 Apr 2022 01:17:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:037d5740b40414bc505c21324142a1cd3eab10c176189a9a74d1a90354ac7cd4`  
		Size: 969.5 MB (969547968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d58ba398110c3f761c6307a5621ec218b8593ba8b07b734436bcdd8d07a23e08`  
		Last Modified: Tue, 08 Mar 2022 20:00:31 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536e5c64699fc55f528fe9ed2ca2c4088a1b329a50236ef20b400958daadc725`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 600.0 KB (600021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242a279bb38e5c0949759b401e7be86d7f899c9457fba0eeabdef0fec92f6682`  
		Last Modified: Wed, 09 Mar 2022 17:40:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f4c6cacc278c66995aee924b612b9af7a269c23ba83a9f7d62e975c98e167f`  
		Last Modified: Wed, 09 Mar 2022 17:40:56 GMT  
		Size: 510.3 KB (510254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58f5589d061ed52422a48576b3455691c9e525eb16f156baa7f0857c9855b15`  
		Last Modified: Thu, 07 Apr 2022 02:20:32 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede5d066fcc61641fbb8c588e98c12a7675acb751a1e029bba643b968fbd6d69`  
		Last Modified: Thu, 07 Apr 2022 02:20:32 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ce491b2bf8b330a27ae19796e5196dcf5a4e9440dc9d806dc1714b8fb72d1c`  
		Last Modified: Thu, 07 Apr 2022 02:20:32 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd8167266b5f27a6951440d8e4497ad8b971438c2e3e05ebcf550178fc45bfe`  
		Last Modified: Thu, 07 Apr 2022 02:24:02 GMT  
		Size: 188.8 MB (188771964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df8a52ca5762e017c400971a39d7a1dd3fec20599d22e8e84dca6fcbf71d811`  
		Last Modified: Thu, 07 Apr 2022 02:20:32 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
