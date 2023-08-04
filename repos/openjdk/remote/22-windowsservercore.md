## `openjdk:22-windowsservercore`

```console
$ docker pull openjdk@sha256:a0f0883c15f78191acb5055fdb69ecc2a1da6dca31497210b0813409d7d4a59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `openjdk:22-windowsservercore` - windows version 10.0.20348.1850; amd64

```console
$ docker pull openjdk@sha256:da59548c3724108cb29f41279e928d52e4d223bb803a5322eaef53420de0be8a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1937275100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143cc7da8ced07037b938787db65ced82f4b8496913db44da60ac8063a889768`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:09:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jul 2023 00:09:40 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:09:59 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:15:35 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:15:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_windows-x64_bin.zip
# Fri, 04 Aug 2023 00:15:37 GMT
ENV JAVA_SHA256=86de3956f3cf843d68c473831181e873e8f4ad3aad53db980302ee94bc62ae5e
# Fri, 04 Aug 2023 00:16:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:16:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1ec6968defeeb9b60629b6fa28ca8f8abfc69ddcc9e2f6480bed84ea25681b`  
		Last Modified: Fri, 14 Jul 2023 00:21:41 GMT  
		Size: 454.6 KB (454587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055eae92651e772da902f668e71180a641b6ba052887a985152bf509f6e5a90a`  
		Last Modified: Fri, 14 Jul 2023 00:21:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935ebae1fa003b7dab4fc2aceb56090efbf4f8547f35020dd20ccd0318d2709`  
		Last Modified: Fri, 14 Jul 2023 00:21:41 GMT  
		Size: 261.4 KB (261435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339aa2beb9c217902d227fc6b73ddfaddf55456d6ce435f3dcf692af99bb72bc`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a342a1f0b9341a5f88d08089de423b3e98e306172137e49935b72d5fd61293b`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede346d16e2168b9175eae572b97545280216a01c562e2add214ed58d25bbd0`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c748313a953537b9e1ca54ac4ac17b4cdd74bde7a3592cd55bbec87d64b43b0e`  
		Last Modified: Fri, 04 Aug 2023 00:24:38 GMT  
		Size: 199.2 MB (199185662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a30f30e4e6b1faf56808004eb4b34e0f4bf1ff4bad701d351e69e38d7c4a2b4`  
		Last Modified: Fri, 04 Aug 2023 00:24:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull openjdk@sha256:7939d2f46f741d4f70149157cb805ec97ffd6e1041d41d6159c72188ef3e0e9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139524655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8db1b8b5a30853d29ed19219fd781ff270efaf95a80ee832403e7e21f80b87a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:12:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Jul 2023 00:12:12 GMT
ENV JAVA_HOME=C:\openjdk-22
# Fri, 14 Jul 2023 00:13:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:16:49 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:16:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_windows-x64_bin.zip
# Fri, 04 Aug 2023 00:16:51 GMT
ENV JAVA_SHA256=86de3956f3cf843d68c473831181e873e8f4ad3aad53db980302ee94bc62ae5e
# Fri, 04 Aug 2023 00:18:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Aug 2023 00:18:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b927162ea448e018f1bd7dfb1a2bc55bf21cf56e2e9a32f46a821cc0e30dd9b`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 232.6 KB (232553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d4e9000a3e1d4472b65f93e8d52e1ab6810d932dec9367b0bdfbcd62f895ab`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f41cc8383e028a5579a8b1df7aef79a0d3783865d9d1eb5182a4ab3a8f448`  
		Last Modified: Fri, 14 Jul 2023 00:22:20 GMT  
		Size: 233.2 KB (233206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167c9d941e8b7c1018bc519231019bb983722a20d56669503100e2aef003252`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb40540c37776dbeacf9ade12a8908c2d80d307e8b20232d57db57d66fdad22a`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c83ee63d905994640ffc1acb0103d126548910b05eaa3f00cd47f2c34d5dea`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c046f978f15edd6c849c1c8007be2ecac8a8a905bdfc20a8441936430bf1d8d`  
		Last Modified: Fri, 04 Aug 2023 00:25:19 GMT  
		Size: 199.4 MB (199361487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359f606ebe408270a38a3335a4797aa3d486f0891f1552d9a7812e99c7693398`  
		Last Modified: Fri, 04 Aug 2023 00:24:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
