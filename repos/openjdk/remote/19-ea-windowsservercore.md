## `openjdk:19-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:793daef5fc0eb97f6bc7977bdb53829c8bab19b574dd4f024fb402ee18c59365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.587; amd64
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-windowsservercore` - windows version 10.0.20348.587; amd64

```console
$ docker pull openjdk@sha256:b76606f12d237f6b29b4522b54b09fd80a7a8aa51c03aec411c7506df0634fe5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2410701081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1034db1af52749c605ef1b879bf61ba8225a77c1a660addcee0834ef3831b1`
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
# Mon, 14 Mar 2022 19:14:30 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:14:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_windows-x64_bin.zip
# Mon, 14 Mar 2022 19:14:32 GMT
ENV JAVA_SHA256=3bc5be203900bba5a006b32c3d4314cf0ab5370439f0493e708589e25bd3fecf
# Mon, 14 Mar 2022 19:15:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Mar 2022 19:15:25 GMT
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
	-	`sha256:94f96c93557c417f0ee8d9746405c4c76e188e22b0694fd531595611299438a9`  
		Last Modified: Mon, 14 Mar 2022 20:20:06 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955589ce40ca1a3ab28cda1a2269189f3c24e5f46211c20856d4295e38599365`  
		Last Modified: Mon, 14 Mar 2022 20:20:06 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83ca570caeadeb46c3a967dff8d286e064f0e290fef09a477a8bd0afa42686b`  
		Last Modified: Mon, 14 Mar 2022 20:20:06 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600c581d4973b3575f46d7ade0fcdf6e22af3cd7d7e8969bfffa1f270a4c4d5`  
		Last Modified: Mon, 14 Mar 2022 20:20:27 GMT  
		Size: 188.3 MB (188335255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edda682b0e61d7e4f24ad58de6d55d1884764f46026cc9a98b57a43722a126d8`  
		Last Modified: Mon, 14 Mar 2022 20:20:06 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:b1a452f84b252ce7c22672a91d0fc5d4cde78f6ea1ca8fe83f4dd73b4e76920b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2904278827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e4ec5b1905b06f052707a3e020aa50f3fe20115bcbf7ee1013ece547efe7e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 17:11:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Mar 2022 17:11:04 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:11:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Mar 2022 19:15:34 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:15:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_windows-x64_bin.zip
# Mon, 14 Mar 2022 19:15:36 GMT
ENV JAVA_SHA256=3bc5be203900bba5a006b32c3d4314cf0ab5370439f0493e708589e25bd3fecf
# Mon, 14 Mar 2022 19:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Mar 2022 19:17:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082ea46951b109a477871d3f8739d105427abdbef68b50e54b54b4ed440f48e8`  
		Last Modified: Wed, 09 Mar 2022 17:41:38 GMT  
		Size: 356.5 KB (356505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c303714362d4354175bfbd60bde4487fb5663326536432755fabbeca5237db`  
		Last Modified: Wed, 09 Mar 2022 17:41:37 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ced75f82f0e7f243af02f1c1abe1b9baafcfd9b31f208d60f85f675e0fb5c1`  
		Last Modified: Wed, 09 Mar 2022 17:41:37 GMT  
		Size: 310.2 KB (310174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2860180fe1f56890e645929465d5c820e7e022db1db70f715ed5a3aa39d35477`  
		Last Modified: Mon, 14 Mar 2022 20:20:49 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcc113711dd2cf68cbd464323c828a75735ee8b772e8aab6b616db5bc46a91b`  
		Last Modified: Mon, 14 Mar 2022 20:20:49 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41002620a51e37525e811ac7d350e1772a3f4ca4e837574d998dca193f2e50ee`  
		Last Modified: Mon, 14 Mar 2022 20:20:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7993878e3468d5d8ffd6b5d60a6b75541bdf62b108dd9c895caec081ce6208c`  
		Last Modified: Mon, 14 Mar 2022 20:21:09 GMT  
		Size: 188.2 MB (188151145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31efaf466f23217a44c3082d664c250d06d0580fdffaacf93c00eea02ff87b48`  
		Last Modified: Mon, 14 Mar 2022 20:20:50 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
