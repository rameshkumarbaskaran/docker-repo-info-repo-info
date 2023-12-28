## `openjdk:23-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:94edbecbd008212b0d81e04f40b6cda4e40ea1aa288a83358babee4fdf3628ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:23-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:aad4cf3a495bf31cf138a267ea89a30e1143ea34635b8b946c8b41edf4061bf7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2258429232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939f3e01f56dc2bf9b60c63620cc552e6b38c966bd2f638acb591bf4ffdd458f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Wed, 27 Dec 2023 21:53:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Dec 2023 21:55:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:10 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 27 Dec 2023 21:55:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:34 GMT
ENV JAVA_VERSION=23-ea+3
# Wed, 27 Dec 2023 21:55:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_windows-x64_bin.zip
# Wed, 27 Dec 2023 21:55:35 GMT
ENV JAVA_SHA256=540333ea6c1ebfa807c83b9b95584a6bf796924d9e2dd3731975515cb9875fb1
# Wed, 27 Dec 2023 21:56:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:56:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77098b0536f5a2d877c48c7dcbdd815790a6741522d13e52b92b71464815a61a`  
		Last Modified: Wed, 27 Dec 2023 21:56:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91f80f2590b37b763c8adba77643c4068516f7699ed0cc17ace96a0b8b4daf9`  
		Last Modified: Wed, 27 Dec 2023 21:56:33 GMT  
		Size: 522.2 KB (522161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53feafc5903179892c4cb7322ea53eeb16efdcf03cd45d523f30d6149a45451c`  
		Last Modified: Wed, 27 Dec 2023 21:56:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd783287696032e21a7c4804900f8771c11af88acb8856a5fed8479f7835aac`  
		Last Modified: Wed, 27 Dec 2023 21:56:33 GMT  
		Size: 366.3 KB (366321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba95a7b808eb39a08e40a75a4ee19a9298158909b9d1b020c4b1b3bfbbb0f13`  
		Last Modified: Wed, 27 Dec 2023 21:56:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdfeb81a237dbdaacad5d17da46be70fa3db3fe2d917dd016a703dac1161656`  
		Last Modified: Wed, 27 Dec 2023 21:56:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3ee45705d658e21a1df57603c1e7336cbf92e3e6cb8eda9309c376fb7ffe05`  
		Last Modified: Wed, 27 Dec 2023 21:56:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48f0f7cafba7e31d955e0a660c31e4b0bc862855fd25c390887e4c0c6511ee3`  
		Last Modified: Wed, 27 Dec 2023 21:56:41 GMT  
		Size: 197.8 MB (197823990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18114926ff88280588844632e0c9e40629bf8e4452866334cebb54f108514ca`  
		Last Modified: Wed, 27 Dec 2023 21:56:31 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
