## `openjdk:19-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:095f40be2bfbc89f66d5634f1614ac1f2c8c74a20faed75fab7fd3160e11b8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64
	-	windows version 10.0.14393.4825; amd64

### `openjdk:19-ea-windowsservercore` - windows version 10.0.20348.405; amd64

```console
$ docker pull openjdk@sha256:52ab992501daf66de3328152be5bfb9948e73bdb1adc28ecafea134d6ab84e18
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377279807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcc9efec8857bb309ebe2673bc98676a86369600531c1265574244c6b1fe5b0`
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
# Sat, 18 Dec 2021 06:52:32 GMT
ENV JAVA_HOME=C:\openjdk-19
# Sat, 18 Dec 2021 06:53:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 18:59:56 GMT
ENV JAVA_VERSION=19-ea+3
# Mon, 27 Dec 2021 18:59:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/3/GPL/openjdk-19-ea+3_windows-x64_bin.zip
# Mon, 27 Dec 2021 18:59:58 GMT
ENV JAVA_SHA256=f36c3877bce15485798362efa5043564eda9265027dfb7b42a219fa5659ecda3
# Mon, 27 Dec 2021 19:01:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:01:14 GMT
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
	-	`sha256:af418b5be8b1aed475657e98454850f5f8c5c731d3a5a481ca2618df77df647a`  
		Last Modified: Sat, 18 Dec 2021 10:51:30 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e19ac6575c209170fa57470a8b18a8200a0e0fed6de37f997e0245e535a62c9`  
		Last Modified: Sat, 18 Dec 2021 10:51:31 GMT  
		Size: 544.3 KB (544334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf6d13b2b491799b27e0101eee603b9bc661f7d50ae7f414771754be02ea5b9`  
		Last Modified: Mon, 27 Dec 2021 20:21:12 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e9624ea69e0703322711e14d21dc930064b98ddcf7b79df6eef12572ab10f0`  
		Last Modified: Mon, 27 Dec 2021 20:21:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c29f71d7d5f2bc9e64249b2b9351fbb68e0abaea1c7a110fc85ca84e55d6c0`  
		Last Modified: Mon, 27 Dec 2021 20:21:12 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7a62e0dd608daaa3d0cfcc4f8224ea0171e5f43be3a54c921ac4e4d1b1e1f6`  
		Last Modified: Mon, 27 Dec 2021 20:21:33 GMT  
		Size: 185.3 MB (185320257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88969e95213468ff3800adda2bf7c0d188446ed76bd189eb2d4eb3e270b64816`  
		Last Modified: Mon, 27 Dec 2021 20:21:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-windowsservercore` - windows version 10.0.17763.2366; amd64

```console
$ docker pull openjdk@sha256:b8e9a0e754849511694f27130c05cd3d129cb59c2972651bb70d8a1ca774a92f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2894459213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29b7c584469870aa5623bfc4e5e7327f1e09e3d8ce23f9e4d3431fd0c5a031`
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
# Sat, 18 Dec 2021 06:56:02 GMT
ENV JAVA_HOME=C:\openjdk-19
# Sat, 18 Dec 2021 06:57:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:01:23 GMT
ENV JAVA_VERSION=19-ea+3
# Mon, 27 Dec 2021 19:01:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/3/GPL/openjdk-19-ea+3_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:01:25 GMT
ENV JAVA_SHA256=f36c3877bce15485798362efa5043564eda9265027dfb7b42a219fa5659ecda3
# Mon, 27 Dec 2021 19:03:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:03:24 GMT
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
	-	`sha256:722566196914616db325d809813c0dcc367bc0f1d3817cf9ca1aecc00149f573`  
		Last Modified: Sat, 18 Dec 2021 10:55:12 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9627e17296876a2afba0e659d2768d968e84a571748a059b8d6a645eab7dba`  
		Last Modified: Sat, 18 Dec 2021 10:55:13 GMT  
		Size: 337.0 KB (337032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057a788057a6da30c6dcb1acbb54e9f6b5b9d0ac72c8b9ed5da4ffae7b330f51`  
		Last Modified: Mon, 27 Dec 2021 20:21:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca40700475ffbc90b98bce35ff0ec264277157fb455ee1a3875b62a37b3b0a0`  
		Last Modified: Mon, 27 Dec 2021 20:21:54 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e4329843f83f9745924f51332cd1255d0bc0ae1b4877a82bcc261ee4c969c3`  
		Last Modified: Mon, 27 Dec 2021 20:21:54 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9061798cbe9f311fd934afd27bfa6ff78e03e07afce2fc71b2ccb1799d0e15e8`  
		Last Modified: Mon, 27 Dec 2021 20:22:15 GMT  
		Size: 185.1 MB (185135084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1291a905931b4b5e00464e327f1b552c740b994ceae4701dce55a10b67aa0d`  
		Last Modified: Mon, 27 Dec 2021 20:21:54 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-windowsservercore` - windows version 10.0.14393.4825; amd64

```console
$ docker pull openjdk@sha256:bd168d30936e1d90bfcdd3c7613a45b439c04c46d8bf830bf2b8da977b41f7ba
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6460495478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929bd24df10911641c6167c530855e8f893ea6175e079ab1b49681e6cc340630`
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
# Sat, 18 Dec 2021 06:59:58 GMT
ENV JAVA_HOME=C:\openjdk-19
# Sat, 18 Dec 2021 07:01:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:03:35 GMT
ENV JAVA_VERSION=19-ea+3
# Mon, 27 Dec 2021 19:03:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/3/GPL/openjdk-19-ea+3_windows-x64_bin.zip
# Mon, 27 Dec 2021 19:03:37 GMT
ENV JAVA_SHA256=f36c3877bce15485798362efa5043564eda9265027dfb7b42a219fa5659ecda3
# Mon, 27 Dec 2021 19:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Dec 2021 19:05:44 GMT
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
	-	`sha256:156b98596a6a205c44cb60ec59ad014ee89440f058f3461f521ffc899670dc95`  
		Last Modified: Sat, 18 Dec 2021 10:55:53 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52478147df3d18fbcb95a25b68742ff25cdb15025a1d754d61d54486c9151339`  
		Last Modified: Sat, 18 Dec 2021 10:55:53 GMT  
		Size: 329.4 KB (329409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699ba066a89da3636f9f02637973f5c39d8360bde81a064b8b394d22ef059afd`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e097e7dbc349aa35b784b37ca72ffa42a57b0b5abb2b7a50c9d08b34963ba5e`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5d79ab6adc5753acbee7f04c2a1cf08803bddde9f2bcb9762188b262f8efa1`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c937be2e7a816fa747caa5d9a0eb73f3593ad7aea97a7982b287df50de56a368`  
		Last Modified: Mon, 27 Dec 2021 20:25:51 GMT  
		Size: 185.1 MB (185107033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a0e3c56868ab16447c718131e63ed616a222d5f3cc4cc64bc507871623ca9e`  
		Last Modified: Mon, 27 Dec 2021 20:22:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
