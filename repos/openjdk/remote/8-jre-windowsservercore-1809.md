## `openjdk:8-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:993a3eaf54f283953dcdc4e3c14058747ead79c8fbd701616088a5a088c03bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:8-jre-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:53af757c0f9f5243a79f84c78ed14a17a0a63e62ab3e87eaf03251ac7457090a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2307597437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc553dcad264ae4647265122200e64cef49b66c61c334200e0dfeb4bbaa73d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 15:15:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Mar 2020 15:15:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Mar 2020 15:15:56 GMT
ENV JAVA_VERSION=8u242
# Wed, 11 Mar 2020 15:19:33 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Wed, 11 Mar 2020 15:19:34 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 11 Mar 2020 15:20:25 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:c328b573f3e398453e572874382c213e2b06ad5b473132297152b58a91945ab5`  
		Last Modified: Wed, 11 Mar 2020 15:36:00 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e655f31a6f9ddf4f0b988abd6bcbb53b6ae8fedc8f709ac9eb57e6c2190a705b`  
		Last Modified: Wed, 11 Mar 2020 15:36:00 GMT  
		Size: 4.7 MB (4655781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08d9dbfabbfefa47b090e230c3b7044a9322879e941c98f448ed9619b9cfa44`  
		Last Modified: Wed, 11 Mar 2020 15:35:58 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f543e7d4ae8d7cf364bb0e646f0598e73c3f36d606cc571ef060df6f5adc7ce`  
		Last Modified: Wed, 11 Mar 2020 15:37:27 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df3d92c951917345da6f9c8138e674c79e90011a4e104d9ed81e4115c437f73`  
		Last Modified: Wed, 11 Mar 2020 15:37:27 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0436c5262eda2d4f8b497018545ffe9256f0e8e9b8957de58e0e43dc32c4401`  
		Last Modified: Wed, 11 Mar 2020 15:37:35 GMT  
		Size: 37.6 MB (37599335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
