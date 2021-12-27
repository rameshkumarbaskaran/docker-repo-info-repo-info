## `openjdk:19-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:344630d8e21d75121f8dc6db0e2fc4da4be0fe53e8aef3dcb7dc32a7af80d400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `openjdk:19-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

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
