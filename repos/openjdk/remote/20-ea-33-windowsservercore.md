## `openjdk:20-ea-33-windowsservercore`

```console
$ docker pull openjdk@sha256:62d0e315e271531c35ffea6e3f04ad2edc9dc0feca8afe8d240e9fa1aed0723b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `openjdk:20-ea-33-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull openjdk@sha256:146a3cbf41613ce1fa128ab9d5b8a286b7bed324be06d220e9ed36e177175c49
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1580855247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e28249edf3b784043ef74be7863b2895f1111a0291c9807e1433c3231bd2a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:07:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:12:21 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 12 Jan 2023 05:12:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:20:21 GMT
ENV JAVA_VERSION=20-ea+33
# Mon, 30 Jan 2023 19:20:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/33/GPL/openjdk-20-ea+33_windows-x64_bin.zip
# Mon, 30 Jan 2023 19:20:23 GMT
ENV JAVA_SHA256=3f6dc47894bb015995e890761fdb61cf403893c312d59048ea3b9db78f78f490
# Mon, 30 Jan 2023 19:21:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:21:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa8e5b91e3c425a756945d0dec251c1595992592fd0dcf4df0ec0a7962717eb`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 614.6 KB (614563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e473ae08f0a0a264ab6f873890549b89c65b8bdb708438338c229d6bb80f4084`  
		Last Modified: Thu, 12 Jan 2023 05:24:23 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6f6e1b656f7612da0ef96aa76c88ddb66ccc536e23899b449c43784f4ba0bd`  
		Last Modified: Thu, 12 Jan 2023 05:24:23 GMT  
		Size: 552.6 KB (552562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3889378826f57049942c173bf081e57b44ad2a55ccbf9fcb60734e1252101186`  
		Last Modified: Mon, 30 Jan 2023 19:28:44 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bcda7f1be693753085f0503f0af8f01ba26ee0cfcd34f444140a4bd20ba995`  
		Last Modified: Mon, 30 Jan 2023 19:28:44 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4d9f694eede25d0395cf26b4eeed8773c6d63bed7b28eda58f9d6e73a6e46c`  
		Last Modified: Mon, 30 Jan 2023 19:28:44 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4721f1ef99e5ce7a2ee79ce88ba1bcfc40b7fce965e0445fe6ee98fce9fb58`  
		Last Modified: Mon, 30 Jan 2023 19:29:06 GMT  
		Size: 193.7 MB (193650624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a116e4c5377d827a769d12a2d53290100f5d68e19463a768e5f46f569aeeca9`  
		Last Modified: Mon, 30 Jan 2023 19:28:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-33-windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:2a5609be646fd00daa796900acfa79222f08be82c04bfd73917157436935202c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902085621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddc326108f673a185e925dc439e17ee9f093012e62cd0954a4290bf75fff03c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:09:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:13:49 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 12 Jan 2023 05:14:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:21:38 GMT
ENV JAVA_VERSION=20-ea+33
# Mon, 30 Jan 2023 19:21:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/33/GPL/openjdk-20-ea+33_windows-x64_bin.zip
# Mon, 30 Jan 2023 19:21:40 GMT
ENV JAVA_SHA256=3f6dc47894bb015995e890761fdb61cf403893c312d59048ea3b9db78f78f490
# Mon, 30 Jan 2023 19:22:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:22:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fe1d317f0927d209417077d671ba0fb8e3b7ff9c583727da819f0d16252e80`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 367.5 KB (367453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204fb4de92b3c2f3fbd44e35eab6a78c6001ee4da68e9f00b462472e9636c486`  
		Last Modified: Thu, 12 Jan 2023 05:25:04 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b5262ccef5459e1e9f746ac49749d63fee0bb98296c21086879d1d379e8e7a`  
		Last Modified: Thu, 12 Jan 2023 05:25:04 GMT  
		Size: 320.0 KB (319987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0f2a6a8828feb97906b9d0e50cfde234cd0836b9dcd86b643d467dd8af615`  
		Last Modified: Mon, 30 Jan 2023 19:29:26 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d973a84c1ddba22c89af441441eb9a2e9d972c81ed2e634a5774d0176384ed`  
		Last Modified: Mon, 30 Jan 2023 19:29:26 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8bc5fe6787ea8ff47f76d5908b52cde906ab6cf8ef25e251d38e8aa6547cbc`  
		Last Modified: Mon, 30 Jan 2023 19:29:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eda67ac4593a92438543994c3640979ca95c681775c71e4b048fb1646290a5`  
		Last Modified: Mon, 30 Jan 2023 19:29:49 GMT  
		Size: 193.4 MB (193445893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733290e89223a0f095da173c481c3d8d21d43a3aa653729824797150de7c844`  
		Last Modified: Mon, 30 Jan 2023 19:29:26 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
