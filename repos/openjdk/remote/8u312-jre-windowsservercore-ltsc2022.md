## `openjdk:8u312-jre-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0e0298473368c1f001f670659994c884889b3d2660903ec2076e6d6f552403c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `openjdk:8u312-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:56b886abc1668713d9c747d52e17471aebbf6ee9b7e11144f6e1c20d4ed79fe5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2247375465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce15da322e09d9c92c33122b2180bcc49d57ad34306431f4cbb40512dde78b7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 22:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:37:53 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 19 Jan 2022 22:38:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:38:17 GMT
ENV JAVA_VERSION=8u312
# Wed, 19 Jan 2022 22:40:32 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_windows_8u312b07.zip
# Wed, 19 Jan 2022 22:41:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa436893917b4b24f7020ae30c97fa33ab983d9c24e6fd7534d56f8b19bf786f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 601.2 KB (601200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4e5cb5c1db0f54a5490ae158422cc0b99b83174adf1eea6454b0543c595c5c`  
		Last Modified: Thu, 20 Jan 2022 02:39:49 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83df987ecf41597ac882d38a9c8f6daa4aa6503ebf73f388dc77a6ae9db30c72`  
		Last Modified: Thu, 20 Jan 2022 02:39:50 GMT  
		Size: 506.6 KB (506564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffeb7c5e533c5f3370ac5fa503f0b0e46c5a96ec022983bd774f729f5e3cef8`  
		Last Modified: Thu, 20 Jan 2022 02:39:49 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eec4ba9ee1399cf0e25f71e99fc71bdce5f0b3851af3d2cb43753c2ec0f0f74`  
		Last Modified: Thu, 20 Jan 2022 02:44:33 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344b7858b97805881acfcd1c5a19fe4f29e53eddd6a32a2530a058fc56fca463`  
		Last Modified: Thu, 20 Jan 2022 02:44:40 GMT  
		Size: 38.8 MB (38762191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
