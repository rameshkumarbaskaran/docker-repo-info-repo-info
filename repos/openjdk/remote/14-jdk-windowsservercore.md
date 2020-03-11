## `openjdk:14-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:10120908d6f6bd2a924834088a3f417e9d95258a6eac84d22e0090ad4b512b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3506; amd64

### `openjdk:14-jdk-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:58924ebfcc31a28418f245561d84cd118d57d490ba17b0a9d40240469fa6749b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2464563818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d9f0a66f1e2d8810776460ae0239e8b52fc7ea766c8ea234212b31c64df5c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 14:53:20 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Mar 2020 14:58:25 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Mar 2020 14:58:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Mar 2020 14:58:52 GMT
ENV JAVA_VERSION=14
# Wed, 11 Mar 2020 14:58:53 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14/076bab302c7b4508975440c56f6cc26a/36/GPL/openjdk-14_windows-x64_bin.zip
# Wed, 11 Mar 2020 14:58:55 GMT
ENV JAVA_SHA256=6b56c65c2ebb89eb361f47370359f88c4b87234dc073988a2c33e7d75c01e488
# Wed, 11 Mar 2020 15:01:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Mar 2020 15:01:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4f86b1e9c271e3e0e37ceb96d7c9042f35b463aef0323a7ca7d3166be8163b`  
		Last Modified: Wed, 11 Mar 2020 15:25:11 GMT  
		Size: 4.7 MB (4659035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69933867a6dc7c01fcc9afb37acbdad733d9faf8d1261f8d7e8117543d4900f`  
		Last Modified: Wed, 11 Mar 2020 15:27:12 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed8e73af81f31273693a0f5f0af35d77288bd22ca618e1645cd292b289d1bb2`  
		Last Modified: Wed, 11 Mar 2020 15:27:13 GMT  
		Size: 289.5 KB (289492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051088fde6ef464d261c16434e97f55003f3877a6605264b4d490772ac036567`  
		Last Modified: Wed, 11 Mar 2020 15:27:04 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58f21d00fc9a6c2daf61a3cd528a42452451d6f4fd316b06a59625fedbffc21`  
		Last Modified: Wed, 11 Mar 2020 15:27:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83fcfc609b62fd8ec56380ef28a1d1295532478a595fda2cb252d33aaaa5067`  
		Last Modified: Wed, 11 Mar 2020 15:27:04 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178001346a3a8ae2dc9abe2afda7537b488de39ce7b8205a543fc36142b140c`  
		Last Modified: Wed, 11 Mar 2020 15:27:41 GMT  
		Size: 194.3 MB (194271805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd81c8ca6745c669aa3d85479691773678e75180bd147e85ca4bf355cb091971`  
		Last Modified: Wed, 11 Mar 2020 15:27:04 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:14-jdk-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:47fd67d28aa3a22452cc521298ec7f7e727a0e5492834a0c079cbefa1084b6d6
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5941584721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d6eccead84bc0618b889768b75f94b2cc68513176ec4f7c61679f1cbb02b78`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:49:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 02:19:58 GMT
ENV JAVA_HOME=C:\openjdk-14
# Thu, 20 Feb 2020 02:21:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:21:39 GMT
ENV JAVA_VERSION=14
# Thu, 20 Feb 2020 02:21:40 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14/076bab302c7b4508975440c56f6cc26a/36/GPL/openjdk-14_windows-x64_bin.zip
# Thu, 20 Feb 2020 02:21:42 GMT
ENV JAVA_SHA256=6b56c65c2ebb89eb361f47370359f88c4b87234dc073988a2c33e7d75c01e488
# Thu, 20 Feb 2020 02:24:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 20 Feb 2020 02:24:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6eada8556f1688b8cc14a7529ed2bd5822b6570a73c142f15a023eda1563d9`  
		Last Modified: Thu, 20 Feb 2020 03:04:58 GMT  
		Size: 5.4 MB (5361808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cf1cf13a0f872534773883f750773098929a143642bee7a87b3338c63efd00`  
		Last Modified: Thu, 20 Feb 2020 03:08:32 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3993d5da2646e2991c26a90059ec5c8efbe7c00f55ba360d423943d74633423f`  
		Last Modified: Thu, 20 Feb 2020 03:08:34 GMT  
		Size: 5.3 MB (5341725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cabfd64be778a30ae7f36eba718f27cf7dc8086857cfd086b944b39fedf440`  
		Last Modified: Thu, 20 Feb 2020 03:08:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e2a1d8c4da4c268fb31a1c36d75160847a88c71fda16024d545d0c2770d014`  
		Last Modified: Thu, 20 Feb 2020 03:08:30 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b5204b5d0e5810a1cfa5a710cca646f5f64972ad259d98bc4e4a5124babdbc`  
		Last Modified: Thu, 20 Feb 2020 03:08:30 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357e54992e2f070af2421c9018816176b46b2b9cf68446d442f530c5e56477f`  
		Last Modified: Thu, 20 Feb 2020 03:11:58 GMT  
		Size: 203.8 MB (203809012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e28a125793c821d91072f8e6c18fbebcb0da7339bca04598e1203cd0140039`  
		Last Modified: Thu, 20 Feb 2020 03:08:30 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
