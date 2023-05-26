## `openjdk:21-ea-24-windowsservercore`

```console
$ docker pull openjdk@sha256:5607b6c846cd15e7309ef963414a5a8aa89d7dac2fb54684aed116759491960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1726; amd64
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-ea-24-windowsservercore` - windows version 10.0.20348.1726; amd64

```console
$ docker pull openjdk@sha256:287367fbe875baefa760ee4e1c39358faf875d594ba7d66995b6bf3806379e70
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973332703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d69e1271131032e07867d7b1c528255a1ca58dbd8fe264156db8cc0e2d77c59`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 05 May 2023 13:22:05 GMT
RUN Install update 10.0.20348.1726
# Wed, 10 May 2023 00:35:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:50:46 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 May 2023 02:50:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:51:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 May 2023 00:15:18 GMT
ENV JAVA_VERSION=21-ea+24
# Fri, 26 May 2023 00:15:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_windows-x64_bin.zip
# Fri, 26 May 2023 00:15:20 GMT
ENV JAVA_SHA256=94a6c75c97d125c5c258fce73749b367c9ee4791ce77d625585e5ac2acdae6e8
# Fri, 26 May 2023 00:16:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 May 2023 00:16:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5829cfc8807e3c8e6f804ec45e3696c2b2e76cd39141b9c20486f8f070f56002`  
		Last Modified: Wed, 10 May 2023 01:46:28 GMT  
		Size: 389.0 MB (388952384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d178a10e123ab9f41a66d7e6d8ffca4aab5fba57cf381f48bc0090f603be2d5`  
		Last Modified: Wed, 10 May 2023 01:45:26 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500851308f2a80744cfa1cca578e46041bad797f47ea2d8c83f894349fac438`  
		Last Modified: Wed, 10 May 2023 03:00:03 GMT  
		Size: 448.7 KB (448735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d15d3ceb58f655a9b9e1310abf5e4a03194602c97d6cbdfa450b22ffbc6d0f`  
		Last Modified: Wed, 10 May 2023 03:00:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b424d7445673b30f720a5569aad1a4050cf8a0ad3c7ac1abe1f0576007898`  
		Last Modified: Wed, 10 May 2023 03:00:02 GMT  
		Size: 262.6 KB (262606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce04de762bfcdb3a0c0050cd5b3d2c3e2244338aa5b052c52a12944697ff18e`  
		Last Modified: Fri, 26 May 2023 00:19:33 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e9b690083212b12cc0c3ec504653a1ae94e7ca0887a7cc306920ad38c0fc44`  
		Last Modified: Fri, 26 May 2023 00:19:33 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b553a237a1e4bed24be9454257bc59ced397cc4c74536def0515a70f66c3f4cc`  
		Last Modified: Fri, 26 May 2023 00:19:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019cf3b876d046a7c30ceebf43537679c0c904138b5e8fa0c7c3d9db99decac2`  
		Last Modified: Fri, 26 May 2023 00:19:52 GMT  
		Size: 197.6 MB (197631390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e9f0b0f74cc56c16f332e74446af69811e603d096cb74c4a76b4d35f4b2f72`  
		Last Modified: Fri, 26 May 2023 00:19:33 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-24-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:897b875e1ee62dbfb736482e07d489cb93a57928516f7e1b50ed6539745e6892
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2270378646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad5bc3f998f8ae2723c9b794cd828cd2b2015f2da7021bbd3ceb0961f03f39b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:54:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 May 2023 02:54:19 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:55:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 May 2023 00:16:20 GMT
ENV JAVA_VERSION=21-ea+24
# Fri, 26 May 2023 00:16:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_windows-x64_bin.zip
# Fri, 26 May 2023 00:16:22 GMT
ENV JAVA_SHA256=94a6c75c97d125c5c258fce73749b367c9ee4791ce77d625585e5ac2acdae6e8
# Fri, 26 May 2023 00:17:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 May 2023 00:18:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8712378a27a3538d7991a50dcb72abb565959575008a538c012500547b6acf3a`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 441.2 KB (441178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34b75cb4c34981b4a471f423e801ccecb0e509ef934ebed87377603d134a0b0`  
		Last Modified: Wed, 10 May 2023 03:00:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0267ca94f1356d921f0a3b30e5336c9c1c0604b0f3cb81963ab715ba48ff81`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 259.9 KB (259927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c9a824d0f58905ef61ad7aaa689ea71fba4274b547d627861d6f8317b62b93`  
		Last Modified: Fri, 26 May 2023 00:20:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e5e6363fa5c53fc642e857d92949afc11ccd0d9898fd5ebf135ac62dbcfe4c`  
		Last Modified: Fri, 26 May 2023 00:20:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a34edc4ee0405aaa415ff2a0029a833bfc167f51000c9fa972591a6125442d`  
		Last Modified: Fri, 26 May 2023 00:20:14 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b85bf68e6a983e9ab05789af2406814864d3005b7eb146d6f2b4cae8f8d6f`  
		Last Modified: Fri, 26 May 2023 00:20:33 GMT  
		Size: 197.6 MB (197633818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad29b8a849de15efff218d4e7fb64e2edf48a85b9e67886f0593b24bc438cdf`  
		Last Modified: Fri, 26 May 2023 00:20:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
