## `openjdk:17-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:c4ecef61e0d5e1bd106dad1e83e3c53db84372aaa6c3eaf627ae347fea7378bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1935; amd64

### `openjdk:17-jdk-windowsservercore-1809` - windows version 10.0.17763.1935; amd64

```console
$ docker pull openjdk@sha256:dcd8a654bec1f1fbe8e7efef300deca5dede5ae706029fffcf5283bcc356916f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2661250118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daa1d3c14ab2d1404113e712922e13390a6e93c24a94c12168d755478ebac2c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 08 May 2021 09:21:48 GMT
RUN Install update 1809-amd64
# Wed, 12 May 2021 12:10:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 May 2021 16:35:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 May 2021 16:35:38 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 May 2021 16:36:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 04 Jun 2021 20:34:47 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 20:34:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_windows-x64_bin.zip
# Fri, 04 Jun 2021 20:34:48 GMT
ENV JAVA_SHA256=b1cf7a899b6687db3553770a0ec1a6e17c5c357d44d2bf0c5845251c32e2d659
# Fri, 04 Jun 2021 20:36:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 04 Jun 2021 20:36:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8116de3c91c3f1ef2d6c09b49ef5407c9b4d672896eb3af5182a997c3c5379c9`  
		Size: 756.2 MB (756156286 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5b8861e3624ab787e21ee36b876b374a3b5ec40eed1621cebfe2f81d1c2cda37`  
		Last Modified: Wed, 12 May 2021 12:20:32 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed0a49f151d983ea76d28f662a09813d5519c713f8356278fc4506a48465166`  
		Last Modified: Wed, 12 May 2021 17:15:05 GMT  
		Size: 5.1 MB (5099027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaa80926e62caa127e4c259e0e5b4ac2701bc636194e0cb724847945fb39a7a`  
		Last Modified: Wed, 12 May 2021 17:15:03 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159e0915c6c5d2d1daba1e45f935dbfd9b5f03a4a0b1b53947ede04b91f41e3`  
		Last Modified: Wed, 12 May 2021 17:15:04 GMT  
		Size: 307.3 KB (307274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aea857da02d96575850976642047742fa3a60ce161078f4b2efef9b416c1c0`  
		Last Modified: Fri, 04 Jun 2021 20:44:09 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a89cfbd8891d4a104f77a4c2d2b456f9d9e16faf7b9332ef76987a1eda0b3`  
		Last Modified: Fri, 04 Jun 2021 20:44:09 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ad1f6457479f04804afbc86e509bd297acad6ed3af9ec8662e8a169ff9ac7f`  
		Last Modified: Fri, 04 Jun 2021 20:44:09 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9130d182977b3e6ad52f0929a04a176c903cbb5c01a8b6f5f73392d7e07f91`  
		Last Modified: Fri, 04 Jun 2021 20:44:29 GMT  
		Size: 181.3 MB (181346145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4968d4ae8d0771897be227c854318f087d1c6bb6725c584b0195ffa122ba262f`  
		Last Modified: Fri, 04 Jun 2021 20:44:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
