## `openjdk:8-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:473278d65d3d7c65ec29a89da20140cf2a5327b826c4c9ed2720530a7c9d9b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `openjdk:8-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull openjdk@sha256:c97da5d8034c364a3cc5ef02b6ca32febf4c777e42e5b1291079fe3271e4cff7
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5837277432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f296f1902b6bcdd1030d13b976efa31eb0ecac6fbb1053d0e055c19d2fe668`
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
# Thu, 20 Feb 2020 02:52:56 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_
# Thu, 20 Feb 2020 02:52:57 GMT
ENV JAVA_URL_VERSION=8u242b08
# Thu, 20 Feb 2020 02:55:21 GMT
RUN $url = ('{0}x64_windows_{1}.zip' -f $env:JAVA_BASE_URL, $env:JAVA_URL_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
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
	-	`sha256:c160f48fb4e8a07dc3f0a5a30f44d95493da8911d2ff4b24fdc35388145feb64`  
		Last Modified: Thu, 20 Feb 2020 03:31:56 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7349b2e5544f09062633be7f2d3c7b40da5ddd3011d2ead0ce8be14215d824b0`  
		Last Modified: Thu, 20 Feb 2020 03:31:56 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6841d50e2fe28233eac0bf2357b6b479d870318c94034aa4d73273549e78c2`  
		Last Modified: Thu, 20 Feb 2020 03:32:25 GMT  
		Size: 104.8 MB (104846186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
