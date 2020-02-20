## `openjdk:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:0ea23b1a88ac922db8f2f6df671735bd9cbb7a77c6f04fa9ce5c751855f55534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `openjdk:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:eda2b174892e5f803fd278b221ceecdf99c9c0e0ece582aaffc4a021e36cf700
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5776889659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1a9e56407ca7fe0d21db148c6b9aa9156c19c341195954e1e2c8e236bae936`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 02:38:44 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 20 Feb 2020 02:40:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:40:02 GMT
ENV JAVA_VERSION=11.0.6
# Thu, 20 Feb 2020 02:46:09 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Thu, 20 Feb 2020 02:46:11 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Thu, 20 Feb 2020 02:48:04 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
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
	-	`sha256:bfcf3424a320410f249390ab52fa09ffc886410dccc7770759a3aa4cd299b885`  
		Last Modified: Thu, 20 Feb 2020 03:25:46 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7492d02370e1c6ba6870acde102d5f53309dd4541f277591b665728d2cf4d19`  
		Last Modified: Thu, 20 Feb 2020 03:25:48 GMT  
		Size: 5.4 MB (5360717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c67a0189bd700086f4f831f5063f88529f8814dd92abd08777c57c964bde`  
		Last Modified: Thu, 20 Feb 2020 03:25:43 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ad1ed1fcabc624ba834374c12af8e473f44d3075d4ca175164083b9447b9b9`  
		Last Modified: Thu, 20 Feb 2020 03:29:39 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3b07e00c853f89877a73d47ba245eda4c1bd4c0b468c73ad7913f41ccae418`  
		Last Modified: Thu, 20 Feb 2020 03:29:39 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc819241299b638cf6f2e38094b9236b4261e2abe8fd84b4befa1d2d0c6beec3`  
		Last Modified: Thu, 20 Feb 2020 03:29:50 GMT  
		Size: 44.5 MB (44458008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
