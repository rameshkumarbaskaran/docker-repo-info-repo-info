## `openjdk:18-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:df6e011535a67bdf9e7b8a338b4de10a657ef3dcba91a6c3c83fb9b574ba4265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:18-windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:aa1557863d05a5cbe7bb28824da00a495ee10abb16180f67f053619d0f2279bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869197385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad11ff148a7ef430719dc76e39515659c2b0c1fb941b6ac0b8203a8e6957dc2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 02:41:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Jul 2021 02:43:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Jul 2021 02:43:13 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 14 Jul 2021 02:44:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 15 Jul 2021 22:14:36 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:14:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_windows-x64_bin.zip
# Thu, 15 Jul 2021 22:14:41 GMT
ENV JAVA_SHA256=05254fd4e51bded07325d499c7c3cf001a8e4e088f682883884d7a49575c4683
# Thu, 15 Jul 2021 22:16:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 15 Jul 2021 22:16:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dd3b24b55401566ea01a5005138a23766b6b6408c2276b7ebd097da01de80897`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60588ed228454a5b9a3ebf90d5ae7109392676a95ebab716cf7bd486f4e257ae`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 365.3 KB (365286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2121b14e07fe4c6047b3da990c93bc98e05e8e5a6585d81ef2973841ca2eb183`  
		Last Modified: Wed, 14 Jul 2021 03:38:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23d09b9f1f97d76bdf221736fe3eea41783f3969bb3ae0601b6f159915c839d`  
		Last Modified: Wed, 14 Jul 2021 03:38:04 GMT  
		Size: 323.5 KB (323485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6071f8296cbc5c4c423479a3fa86e7dd96f1451e38a68c53d7d375bec8e297d5`  
		Last Modified: Thu, 15 Jul 2021 22:29:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49d42f3b4b81a37d2922f2b8bcb73c862c79d81f6c22fab59ac686c41be3644`  
		Last Modified: Thu, 15 Jul 2021 22:29:28 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf43f815b8f29405f12daf0c7aa79a242452fc59fa60c359e34adb483314a4b`  
		Last Modified: Thu, 15 Jul 2021 22:29:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdc4cddab8a0e914dc6177bc0be72a059ecd47272872cf20e989dc83ce444e6`  
		Last Modified: Thu, 15 Jul 2021 22:29:48 GMT  
		Size: 183.1 MB (183053689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aee1e38eae0df3cccaf6cd94fdd9a6cb3d97a8f20fb548293abe3bc3b4da32`  
		Last Modified: Thu, 15 Jul 2021 22:29:28 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
