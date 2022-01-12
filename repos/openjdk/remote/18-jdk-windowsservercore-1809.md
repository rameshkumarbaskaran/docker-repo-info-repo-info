## `openjdk:18-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:1ed2b5a173e6526ff0c9ad9e40aaf42ca6113d342bdd9486aad213dc10e31f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `openjdk:18-jdk-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull openjdk@sha256:13b85a8e5214fba258ffb63543befa3c485a88219fe0ae07bbc7ebbfcf16a9b2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2897158462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a13b4ec2f4384760d59d1a5f7b823e7b740d2ada76db8b6b73dd66bd14d3810`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 05:12:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:22:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 12 Jan 2022 05:24:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:24:11 GMT
ENV JAVA_VERSION=18-ea+30
# Wed, 12 Jan 2022 05:24:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/30/GPL/openjdk-18-ea+30_windows-x64_bin.zip
# Wed, 12 Jan 2022 05:24:13 GMT
ENV JAVA_SHA256=57e77e09ea1801bd17d69a31b973074ea5bfeafdc150ca0376b7df8f593629f3
# Wed, 12 Jan 2022 05:25:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 12 Jan 2022 05:25:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3a70d5fd54e2005efbf590b48700ed40509210354a0d8f3f18c3b444a5325896`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74f00c66c11971de2e35204e3f42aca9ac77b3dba4dcd545130bea41c91fd27`  
		Last Modified: Wed, 12 Jan 2022 22:56:55 GMT  
		Size: 346.0 KB (345951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5ef5c6a221a0976ffb06a622ddbeb928e23f646d54ec24e713534a432fd788`  
		Last Modified: Wed, 12 Jan 2022 23:03:02 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1738ecfeffa0ad0e4c36d0a2110a8003421d56cec36f4a31c700953c0bc6bc7`  
		Last Modified: Wed, 12 Jan 2022 23:03:03 GMT  
		Size: 303.1 KB (303067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c62b5744eaef65206df9ca7a42d3d440570ad8131b93cfced7004be36c59db`  
		Last Modified: Wed, 12 Jan 2022 23:02:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85ad761c2b0483cac1059235b6181bf1a7d964bf07e9036022ed45e984fc662`  
		Last Modified: Wed, 12 Jan 2022 23:02:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa30ea07b77bbedcdbcf9626bdedb35d681aac64bfcbc773a6304c0c899f20a`  
		Last Modified: Wed, 12 Jan 2022 23:03:00 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc41987746763078deae6d29239f68758b8e9aef2094c3f8a1dd12c751f4dd3`  
		Last Modified: Wed, 12 Jan 2022 23:03:24 GMT  
		Size: 184.3 MB (184270030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff25853a3e9481526295980e759afc1c7ee7b40da144fe3ba4fb3edc1bdd41fc`  
		Last Modified: Wed, 12 Jan 2022 23:02:59 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
