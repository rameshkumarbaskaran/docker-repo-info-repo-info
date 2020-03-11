## `openjdk:8-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:475115640a80e153e13daf8853112025a6f78f9e149ab3aef9c895bd4cf12982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:8-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:c0f1fb392be26ac85ed627a38c7a4da466e62180f6b56e899ec26060c7519056
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369779329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7061b077f71568628dd25fd61684ff48929a4c34f132bf6477aff183b08025fd`
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
# Wed, 11 Mar 2020 15:15:57 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_
# Wed, 11 Mar 2020 15:15:59 GMT
ENV JAVA_URL_VERSION=8u242b08
# Wed, 11 Mar 2020 15:17:27 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:7e8944910e6bc460ef86d4e92b4dfb29b8d124503e9d221cc8aa507380e2ccdd`  
		Last Modified: Wed, 11 Mar 2020 15:35:58 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12344e6de864a04bcd97347d6542f9f7c8ceb3a634aceb840609a4cf574bce1`  
		Last Modified: Wed, 11 Mar 2020 15:35:58 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259079f1f94fb4d019f1d89fd968500ee84009bdb44dd04c49e8c48b6dd22708`  
		Last Modified: Wed, 11 Mar 2020 15:36:18 GMT  
		Size: 99.8 MB (99781215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
