## `openjdk:18-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:82ddcae807b4421240a768bde52b7bc421515cd66155edf52102aad2cca68c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `openjdk:18-jdk-windowsservercore` - windows version 10.0.20348.405; amd64

```console
$ docker pull openjdk@sha256:a4869d24127856958198d5229514a7ad07277c702bb940029ecb336e7b936e39
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2376444110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf9dfb2ed99668ffc8e44d05bd4747bc1b7e7af035204656652441fb0905005`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 08 Dec 2021 01:54:07 GMT
RUN Install update ltsc2022-amd64
# Sat, 18 Dec 2021 00:09:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 06:52:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 18 Dec 2021 07:03:46 GMT
ENV JAVA_HOME=C:\openjdk-18
# Sat, 18 Dec 2021 07:04:17 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:07:04 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 19:07:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:07:06 GMT
ENV JAVA_SHA256=7ce8c0466233333b8ca3dfa4da6c9e122b8c7a7b4322141c2961921fb32e873e
# Mon, 27 Dec 2021 19:08:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:08:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4d1d74adc6a92e44b3cd592ec9459f1fff926eaf6fc20bb7526360bec71aefc0`  
		Size: 939.1 MB (939072515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5bc74beb7593c703ac99379d225f3a9a445549cc06a3fe18f44e356a45f225f3`  
		Last Modified: Sat, 18 Dec 2021 01:18:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf6738034b8742c8193d3db825f75f650b85ef03ad87a2f9e6d91f195c38d2`  
		Last Modified: Sat, 18 Dec 2021 10:51:31 GMT  
		Size: 635.1 KB (635126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33616cf8971399858dc392d3e603c9a6c4eff8c6054af2d8492d250b300756b9`  
		Last Modified: Sat, 18 Dec 2021 10:57:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d1a684c0e994a86f11bcc0f30830fad11b052093f81257505ce6a25ecac099`  
		Last Modified: Sat, 18 Dec 2021 10:57:14 GMT  
		Size: 544.5 KB (544523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d5fdaabdfcacf664c3b2b3be6e76384006e36c76a1c9bddb18a16c7de4c1ae`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5768682fffa60d9adeed2d76c30e51565e52a9424f82baa0bc7d9aa2ececabd8`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194328d1856f5c3f1e13e5a50e7b4d0969b3c710bf2c4a011f1acea130b5fea`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23080ebc1b7cfc8f3c2422d3b7ab2067d48a090587b6206bba94b1db6a47f7f4`  
		Last Modified: Mon, 27 Dec 2021 20:30:14 GMT  
		Size: 184.5 MB (184484399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c915a6a780a2c8e906fe0e6045465b6358da69950161816f59865c656b01266c`  
		Last Modified: Mon, 27 Dec 2021 20:26:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull openjdk@sha256:ff0fbfc7935295c70cb3b2f95c67b791d8dbd443ff1fea160d10a0ccb376d5f9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2893621729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c4d0ec3836265df02c7aba7c326e2793f6ded4eb5e3759d70b475fb69325d2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Fri, 17 Dec 2021 23:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 06:56:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 18 Dec 2021 07:05:28 GMT
ENV JAVA_HOME=C:\openjdk-18
# Sat, 18 Dec 2021 07:06:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:08:30 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 19:08:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:08:32 GMT
ENV JAVA_SHA256=7ce8c0466233333b8ca3dfa4da6c9e122b8c7a7b4322141c2961921fb32e873e
# Mon, 27 Dec 2021 19:10:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:10:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31b2acce136e44984ba36d64717a6a67fbf1a98ed7ffcf0a14df848c1502a345`  
		Last Modified: Fri, 17 Dec 2021 23:47:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ef2f84414aadaa12189f793787857287076489d28b83d8f44727621fdc6793`  
		Last Modified: Sat, 18 Dec 2021 10:55:13 GMT  
		Size: 374.2 KB (374167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb03ce95f5cb3cf434995496d5e9199741f2e3ff4ebb26880dca6013069e4bc`  
		Last Modified: Sat, 18 Dec 2021 11:00:50 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5741bbbde36f0dd0d1d665d728713acd13cf9f256fdabc6940ed4a6488fc67d7`  
		Last Modified: Sat, 18 Dec 2021 11:00:50 GMT  
		Size: 337.5 KB (337467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2581b23d21180ce85bd61311d299f781a608b036d95d8aec0b006d1db77ed`  
		Last Modified: Mon, 27 Dec 2021 20:30:33 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5f3b48698bd2067d9b0945780851d88ea54549d1d7de9188e3576f3609cd0`  
		Last Modified: Mon, 27 Dec 2021 20:30:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e310e088794cacd37e0e92a6a1b691071ab559405ed3ab4b8610637363b397d`  
		Last Modified: Mon, 27 Dec 2021 20:30:33 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cf3398c9f6b0e7b8d7ca4fc970a4cce9eb52e06103a0f744ca901ad9a08438`  
		Last Modified: Mon, 27 Dec 2021 20:34:03 GMT  
		Size: 184.3 MB (184297068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971a6926177570aaf4946ce89b5a7bf8e07e28f5e6408248aedc8b042c4438fe`  
		Last Modified: Mon, 27 Dec 2021 20:30:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull openjdk@sha256:4db24831fc2f987fc53bc1c96fb3aaf089b419762d3eda3758761e016923b36b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6459651536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf816dc52c7ade9c9fa253d25084db1259fa695fda743e64b707fda97b4881fa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Sat, 18 Dec 2021 00:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 06:59:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 18 Dec 2021 07:08:40 GMT
ENV JAVA_HOME=C:\openjdk-18
# Sat, 18 Dec 2021 07:09:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:10:43 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 19:10:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:10:46 GMT
ENV JAVA_SHA256=7ce8c0466233333b8ca3dfa4da6c9e122b8c7a7b4322141c2961921fb32e873e
# Mon, 27 Dec 2021 19:12:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:12:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7756a7a3024dbbb7cabda3151e8f8461ae808ae2ad3857f0c9235c5908ff7695`  
		Last Modified: Sat, 18 Dec 2021 01:22:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f88306d11f630889687486bb566861161592f87bc40ac9850fce316e5b7780`  
		Last Modified: Sat, 18 Dec 2021 10:55:53 GMT  
		Size: 335.8 KB (335827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b6cd0c0ddb275bff04e82262e96ff042aa7e6340d0b8a3adce915bef0331d2`  
		Last Modified: Sat, 18 Dec 2021 11:04:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311e7beac3446508723ce8cebedd1494521d0143b567d476b6e8ecb9d690d9b`  
		Last Modified: Sat, 18 Dec 2021 11:04:35 GMT  
		Size: 330.2 KB (330217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73b6059936e6fdb97078a1ed56ed4bd6ad7f2aea0b7166c0532edc0935f73c4`  
		Last Modified: Mon, 27 Dec 2021 20:34:23 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8a522e5632087e5d5836d4b5c18d7741727ba8edaf301df9a31dbe42141bb8`  
		Last Modified: Mon, 27 Dec 2021 20:34:23 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c15d6358bf71da02fca16d93e3a98c11cf0de30cda639dd4999c076d107995f`  
		Last Modified: Mon, 27 Dec 2021 20:34:23 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af8183a2d7019eaa12bd3465bcf586092892ab6d33f0c8b5c3ecdaa6e77dbb3`  
		Last Modified: Mon, 27 Dec 2021 20:34:43 GMT  
		Size: 184.3 MB (184262226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a942f70d1f631cfdd1abd5815bd08b5e60e87dbe9a77233dad331f1cb626030e`  
		Last Modified: Mon, 27 Dec 2021 20:34:24 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
