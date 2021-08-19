## `eclipse-temurin:8u302-b08-jre-windowsservercore-ltsc2016`

```console
$ docker pull eclipse-temurin@sha256:818d02ca4f4da3ef2da162650848711def797abe2333b15ec3044c2e6fa9b9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4583; amd64

### `eclipse-temurin:8u302-b08-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.4583; amd64

```console
$ docker pull eclipse-temurin@sha256:b1b3be103a39c8ebfd577c947820a0608a3943cad44401a7c2407a06b1f97ed2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6341807673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884b9a193a0b99e3f48380bea9f70f6d7b7ed9d46d3486ec9c530044aedbdd3c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 01 Aug 2021 08:52:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Aug 2021 12:51:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 21:36:03 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 19 Aug 2021 20:20:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_windows_hotspot_8u302b08.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '34e5eea737dfaca57ec5162e6fece5259f403fa419c7bcab572e9cdd2bcf8dd1') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 19 Aug 2021 20:21:57 GMT
RUN Write-Host 'Verifying install ...';     Write-Host '  java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c427f892fe74603ae09d4e49b25f8f7046f957054034dc9f462e0e88d7bffaa5`  
		Size: 2.2 GB (2200980134 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d4b5c087d85e7fbeffd8b282ecd862da1fb7ff00c37657c5712888936292097`  
		Last Modified: Wed, 11 Aug 2021 13:30:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482fe77a1b07de2e3de2d4afb544f5d4e94c199a6882f435600f2884c30be901`  
		Last Modified: Fri, 13 Aug 2021 22:00:39 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665c822e6ce5a88b8719e4854a21652071a8c78119e3edc3510487ee57443e4f`  
		Last Modified: Thu, 19 Aug 2021 20:26:08 GMT  
		Size: 70.5 MB (70525959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b04b3f42ef2dd7b8458619ae9de3bb152ba5bedd0054cce312e4268ee26e8`  
		Last Modified: Thu, 19 Aug 2021 20:25:59 GMT  
		Size: 312.9 KB (312874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
