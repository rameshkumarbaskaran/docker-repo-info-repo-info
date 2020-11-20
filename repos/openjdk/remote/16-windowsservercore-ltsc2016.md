## `openjdk:16-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:871f94b4bbb1c9c3cf8c6a7bc906b1144bc2ffef2f1b6b7b6b35b971ba58a28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `openjdk:16-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull openjdk@sha256:33a99fece8e5359a497f8b4e8a0d965b6be749a32d6fddaf4133fdc16c4de47b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5975375901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30b2aa324933a557b2a04ee87080cf0bb657e4f47414c7e5daba2cf0e7e4161`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Nov 2020 17:49:02 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Nov 2020 17:50:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 20 Nov 2020 00:17:12 GMT
ENV JAVA_VERSION=16-ea+25
# Fri, 20 Nov 2020 00:17:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/25/GPL/openjdk-16-ea+25_windows-x64_bin.zip
# Fri, 20 Nov 2020 00:17:13 GMT
ENV JAVA_SHA256=72ed2ed1b3f001fe8a57a3d23f236248fab03f80130624e7f837d5c5a072dfeb
# Fri, 20 Nov 2020 00:19:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 20 Nov 2020 00:19:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1222181efe25bb0d500f320707eb7dc24e576749c0897042ae1f3b8116e87990`  
		Last Modified: Wed, 11 Nov 2020 18:26:42 GMT  
		Size: 10.1 MB (10078764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715e1a3de99f869c8010907852bce9306cb6693a16fc9fad69ea0bb744446cdc`  
		Last Modified: Wed, 11 Nov 2020 18:26:29 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd970ee1e99b8801c2230b471ed6d4dc79d30324c882f32ae8efb05d8be0d34d`  
		Last Modified: Wed, 11 Nov 2020 18:26:31 GMT  
		Size: 5.5 MB (5511761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490f4770b5a73ef61af9705cb9777bf1c5f2967fe5cdf1f95ce4cd469ef41330`  
		Last Modified: Fri, 20 Nov 2020 00:28:48 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae9de20b00ff707f05fae7f5f934c77326a85223ff6fec4d87d0ce91c8c10f2`  
		Last Modified: Fri, 20 Nov 2020 00:28:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f246c4c46a748f5113aaf52620b9342215be215109d76db9e5e7ffae22e72d59`  
		Last Modified: Fri, 20 Nov 2020 00:28:47 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0751ad23e58d08992f027acc53b3e0ffa2196641f3aeb6bb338dc437673e16b`  
		Last Modified: Fri, 20 Nov 2020 00:29:07 GMT  
		Size: 189.2 MB (189219680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f8a995097b90fce40043bcbe427230d6fd28011cde4707fe46206b0efbc499`  
		Last Modified: Fri, 20 Nov 2020 00:28:47 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
