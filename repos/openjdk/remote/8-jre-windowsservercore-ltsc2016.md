## `openjdk:8-jre-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:a51f78f065f6be855308c0f58bd7d3dc431dddb94712e885d16721b75fb34e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `openjdk:8-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:a664f5e098b450611ea8443dcee087f9384afe19c26665424fc48f2f866c7b5c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5775095570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4fe3d6030cb181a9bf5cb57487bd3f42505f0cd3772e0bb2d150edb859ba69`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 02:51:33 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 20 Feb 2020 02:52:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 20 Feb 2020 02:52:54 GMT
ENV JAVA_VERSION=8u242
# Thu, 20 Feb 2020 02:58:19 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_
# Thu, 20 Feb 2020 02:58:21 GMT
ENV JAVA_URL_VERSION=8u242b08
# Thu, 20 Feb 2020 03:00:05 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:a4c80f33a584cbc53fbd9fe1daa6a94e9068ad4d5b13cb5797895f8a79809da4`  
		Last Modified: Thu, 20 Feb 2020 03:31:58 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df64bd24d9be59a0607c2bb2592b8410b4b97a21d26de10079673be9f8e4d0e0`  
		Last Modified: Thu, 20 Feb 2020 03:32:02 GMT  
		Size: 5.4 MB (5360283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453dea9fc2efa53923c60ee91cf838329be9ad62a4524609fdb995f0b77bc210`  
		Last Modified: Thu, 20 Feb 2020 03:31:56 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24824c05bf4272f6873f49471562f4508a12cc5f65fa378ccc2485ffbf7f1430`  
		Last Modified: Thu, 20 Feb 2020 03:34:37 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf419d27952872fa80c71eb20f0db45debaf725bacea00ac865155622634c905`  
		Last Modified: Thu, 20 Feb 2020 03:34:37 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708cd13e51cee894cddd18a50e1b963a2af30ef1c826deb23d38e77db0c0fa7f`  
		Last Modified: Thu, 20 Feb 2020 03:34:46 GMT  
		Size: 42.7 MB (42664318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
