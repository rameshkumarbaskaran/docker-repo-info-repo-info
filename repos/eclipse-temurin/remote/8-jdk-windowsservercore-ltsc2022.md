## `eclipse-temurin:8-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d54f0b0bbd823ac311f90695623b1223c323d92630b71dc1942e15877bb24ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `eclipse-temurin:8-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:f7a770055d8a626156c4067e22fa38f2aa9fed290b85ba052fb7ce83a7fe22fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2537536963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac9718575a440bac745d25d0cecd898554ec5103a200ee8263d3ce397899fe9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:58:35 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Wed, 14 Sep 2022 15:59:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_windows_hotspot_8u345b01.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_windows_hotspot_8u345b01.msi ;     Write-Host ('Verifying sha256 (a19b85fedcc830aa81c6aeb07449905032b7b391c033a1647639486b25f2e1f3) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a19b85fedcc830aa81c6aeb07449905032b7b391c033a1647639486b25f2e1f3') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 15:59:56 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01ab8db53a5453998abd5ddd4d7f2c5af26995f59fb92fd627164cc9eeaecdb`  
		Last Modified: Wed, 14 Sep 2022 16:46:10 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a1aee914014d9b00f75f47124f28af0b4622ef057453ecf564176038b99085`  
		Last Modified: Wed, 14 Sep 2022 16:46:28 GMT  
		Size: 190.0 MB (190046483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87db099869380d363d9f8d601302da0e9453cd2db41c821ad249969e39f43d7`  
		Last Modified: Wed, 14 Sep 2022 16:46:10 GMT  
		Size: 538.0 KB (538022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
