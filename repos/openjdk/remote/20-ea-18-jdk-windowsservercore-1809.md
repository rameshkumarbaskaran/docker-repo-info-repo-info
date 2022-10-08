## `openjdk:20-ea-18-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:fc68462f23b14ebe38c202a829e9d8ff064412253e5e612e753f36f5b2cc253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `openjdk:20-ea-18-jdk-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull openjdk@sha256:14628403e212b37b2d4d19c79e3298e7b6491d4343d450fabb3298fe9d58c86c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896512103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887ee3b16f1a0bfdcd7fd6dcde9ce90026e05fa62f99773a2557b0467b725908`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:06:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Sep 2022 17:06:14 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:07:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 07 Oct 2022 23:16:22 GMT
ENV JAVA_VERSION=20-ea+18
# Fri, 07 Oct 2022 23:16:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/18/GPL/openjdk-20-ea+18_windows-x64_bin.zip
# Fri, 07 Oct 2022 23:16:24 GMT
ENV JAVA_SHA256=2957954de0bb9cde44f6893f02d9a175cdcbb470cd3650080bf53f05472fe6b5
# Fri, 07 Oct 2022 23:18:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 07 Oct 2022 23:18:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58648929570c8439cbc01e98ebc75618cbe96e946d332763402b53d89cc5639b`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 349.5 KB (349457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69dd72d8573f685284949ad83177bf75e72c3d8275d35aa6b4d21f5a480f2b9`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bfc5f723418de82847d7f0e86272a0dc2ec14263a42be94649cbc3d219420b`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 311.8 KB (311834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9838c7526c92db5e3ba2658add9e839b496a22ee8a2621df62590d2de1e7b`  
		Last Modified: Fri, 07 Oct 2022 23:21:58 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcabfb47061b1bb13a55cc7e91fe108e187a4bd98182c73d5ec170627257a2e`  
		Last Modified: Fri, 07 Oct 2022 23:21:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b3ff9dd2b8cbf5534a695d068677ded271da1e6c29bdf73db84c0515d7dcca`  
		Last Modified: Fri, 07 Oct 2022 23:21:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c5bf29daed2a7b5ec97278bce51a68e3c5295b9cacc46052fb483c3a724067`  
		Last Modified: Fri, 07 Oct 2022 23:22:17 GMT  
		Size: 192.3 MB (192277536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533c5d7ceda688e5ca96b0856ec84e8a41691b8e943145e7218631e1ddf8d9da`  
		Last Modified: Fri, 07 Oct 2022 23:21:58 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
