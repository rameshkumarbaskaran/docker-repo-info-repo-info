## `openjdk:8u242-jre-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:544055bf4c0aa0d5a3481349479dd5dd2dd3dd1efa053cc7f246ea9d3c25e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:8u242-jre-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:5aeaf0f09aa0aa55b33cbe4e8f8a7712dcaaadf11f8adeee41ccca101f3fa0da
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2272676100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2786bb2a1c8394077fe56ca663c6cad22fb1adb15259f682d75beb157ba197f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 02:48:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 20 Feb 2020 02:49:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:49:33 GMT
ENV JAVA_VERSION=8u242
# Thu, 20 Feb 2020 02:57:12 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Thu, 20 Feb 2020 02:57:13 GMT
ENV JAVA_URL_VERSION=8u242b08
# Thu, 20 Feb 2020 02:58:02 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67111b100db96f11d25edec248c8d3b4defd4453c41df4b557f7c44d536ee1bc`  
		Last Modified: Thu, 20 Feb 2020 03:30:58 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a90402e852dbb869de7c554f3a93f43b96c6b5acbc1270c802c0a057ff7057`  
		Last Modified: Thu, 20 Feb 2020 03:30:57 GMT  
		Size: 4.6 MB (4565781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c918a91aaa3902ebddc9902bd106fb779ee325b1fc0875a26ef146bfd3047b`  
		Last Modified: Thu, 20 Feb 2020 03:30:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eeac069850900f75dfba502c8aa05208b50e9e23b34f51b87c316c3f4a6ee3e`  
		Last Modified: Thu, 20 Feb 2020 03:34:05 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b423e8b752ddcd3ca5d22415b5cd581d0f24b2f4e137797586d52423f7575b89`  
		Last Modified: Thu, 20 Feb 2020 03:34:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6581b42cd9b72bfa6a4b3c770a0b9f2ba5db45318f13e1b74a461388d01c61d`  
		Last Modified: Thu, 20 Feb 2020 03:34:13 GMT  
		Size: 37.6 MB (37600434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
